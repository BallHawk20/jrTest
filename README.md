```
using UnityEngine;
using UnityEngine.Purchasing;

public class IAPManager : MonoBehaviour, IStoreListener {
  private IStoreController controller;
  
  //The following products must be added to the Product Catalog in the Editor:
  private const string coins100 = "100.gold.coins";
  private const string coins500 = "500.gold.coins";

  public int coin_count = 0;

  void Awake () { 
    StandardPurchasingModule module = StandardPurchasingModule.Instance (); 
    ProductCatalog catalog = ProductCatalog.LoadDefaultCatalog (); 
    ConfigurationBuilder builder = ConfigurationBuilder.Instance (module);
    IAPConfigurationHelper.PopulateConfigurationBuilder (ref builder, catalog); 
    UnityPurchasing.Initialize (this, builder); 
  }

  public void OnInitialized (IStoreController controller, IExtensionProvider extensions) { 
    this.controller = controller; Debug.Log ("Initialization Successful"); 
  }
  
  public void OnInitializeFailed(InitializationFailureReason error) { 
    Debug.Log ("UnityIAP.OnInitializeFailed (" + error + ")");
  }
  
  public void OnPurchaseFailed (Product item, PurchaseFailureReason reason) { 
    Debug.Log ("UnityIAP.OnPurchaseFailed (" + item + ", " + reason + ")"); 
  }

  public PurchaseProcessingResult ProcessPurchase (PurchaseEventArgs e) {
    string purchasedItem = e.purchasedProduct.definition.id;
    
    switch (purchasedItem) { 
      case coins100: Debug.Log ("IAPLog: Congratualtions you are richer!"); 
      coin_count += 100; 
      Debug.Log ("IAPLog: Coin count: " + coin_count); 
      break; 
      
      case coins500: Debug.Log ("IAPLog: Congratualtions you are richer!"); 
      coin_count += 500; 
      Debug.Log ("IAPLog: Coin count: " + coin_count);
      break;
    }
    return PurchaseProcessingResult.Complete;
  }

  public void Buy(string productId) { 
    Debug.Log ("UnityIAP.BuyClicked (" + productId + ")");
    controller.InitiatePurchase (productId);
  }
}
```

<a name="ImplementingAds"></a>
### Implementing Unity Ads
You must also [initialize Unity Ads](https://unityads.unity3d.com/help/monetization/integration-guide-unity), whether or not you use the Codeless or manual IAP initialization method. The following code sample illustrates an initialization method to invoke:

```
using UnityEngine;
using UnityEngine.Monetization;

public class AdManager : MonoBehaviour {

  public bool testMode = true;
  private const string adPlacement = "video";
  private const string promoPlacement = "promo";

  #if UNITY_IOS
    private const string gameId = "0000000"; // Your iOS game ID here
  #elif UNITY_ANDROID
    private const string gameId = "9999999"; // Your Android game ID here
  #else
    private const string gameId = "0123456"; // Prevents Editor Errors
  #endif

  private void Awake () {
    if (Monetization.isSupported && !Monetization.isInitialized) {
      Monetization.Initialize (gameId, testMode); 
    }
  }

  public void ShowVideoAd () { 
    ShowAdPlacementContent ad = Monetization.GetPlacementContent (adPlacement) as ShowAdPlacementContent; 
    if (ad != null){
      ad.Show ();
    }
  }

  public void ShowPromo () { 
    PromoAdPlacementContent promo = Monetization.GetPlacementContent (promoPlacement) as PromoAdPlacementContent; 
    if (promo != null) {
      promo.Show (); 
    }
  }
}
```
