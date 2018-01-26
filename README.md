/*
Title: Dashboard guide  
Sort: 20
*/


## Overview
The [Unity Ads monetization section of the Developer Dashboard](https://operate.dashboard.unity3d.com/) provides tools to manage Ads monetization across your Unity Projects. From the Dashboard, you can manage Project settings, test devices, and revenue reporting metrics to optimize your earning potential.

### Navigating the Dashboard
Most of the Ads Monetization Dashboard’s core functionality is available when you select an Ads-enabled Project (see section on [**Projects**](#projects)). From the Project view, you can access the following.

#### Statistics
The **Statistics** page provides customizable reporting tools that allow you to analyze your Ads performance and revenue. For an in-depth look at the metrics available here, see documentation on [**Monetization statistics**](https://unityads.unity3d.com/help/monetization/statistics).

#### Platforms
The **Platforms** page shows your **Game ID** for each store platform, which you need to [integrate Unity Ads in your game](https://unityads.unity3d.com/help/monetization/getting-started). Selecting an enabled platform opens its **Placements** menu. Placements are a critical component of Ads integration (for more information, see documentation on [**Placements and filters**](https://unityads.unity3d.com/help/monetization/placements-and-filters)). 

##### Store details (Optional)
To link your game to its published retail product, select **ADD STORE DETAILS** for the respective storefront. Doing so customizes your dashboard view to display your game’s store icon instead of the default Google Play or iTunes icons. 

**Note**: Setting this field has no impact on your ability to show ads or monetize with Unity Ads. 

For the Google Play store, enter the game’s **bundleID**, Extract the bundleID from your game’s URL, as shown in the highlighted section of the following URL:

<!-- insert image 
![Ad content filters](https://cdn.applifier.com/files/GoogleBundleID.png)
-->

<!-- Caption: Locating your game’s Google Play bundleID.-->  

For the iTunes store, extract the game’s **storeID** from its URL, as shown in the highlighted section of the following URL:

<!-- insert image 
![Ad content filters](https://cdn.applifier.com/files/AppleStoreID.png)
-->

<!-- Caption: Locating your game’s iTunes storeID. -->

**Note** : If you released your game recently, our system may not be able to access its store information. 

#### Settings
The **Settings** page displays your **Project ID** and [COPPA](https://en.wikipedia.org/wiki/Children%27s_Online_Privacy_Protection_Act) settings.

#### Instructions
The Instructions page contains helpful information on quickly installing the Unity Ads SDK and integrating Unity Ads in your game.

## Projects
To access the Ads monetization dashboard, navigate to the Developer Dashboard and select the **Operate** tab. 

**Note**: You can also access the dashboard from the Unity Editor, through the Ads section of the Services window (**Window** > **Services**), by selecting **Ads** > **Go to Dashboard**.

Selecting a Project from the **Projects** menu allows you to manage its [Placements](https://unityads.unity3d.com/help/monetization/placements-and-filters) and [metrics](https://unityads.unity3d.com/help/monetization/statistics) reports. At any time, you can return to the Projects menu by selecting the up arrow icon, or navigate directly to another Project by opening the Project drop-down menu.

<!-- insert image 
![Ad content filters](https://cdn.applifier.com/files/DashNavigation.png)
-->

<!-- Caption: Navigating Projects in the Ads dashboard.-->

### Managing Projects
#### Adding Projects 
Selecting **Projects** from the left navigation bar displays a list of Projects with Ads enabled, along with their Project IDs and enabled platforms. 

##### Enabling an existing Project
For Projects without Unity Ads enabled, check the **Enable Unity Ads for an existing project** radio button, then choose one of your organization’s Projects from the drop-down menu. 

Check the corresponding checkmarks for each platform you wish to enable (Apple or Google Play), then indicate whether your game has been published yet for each enabled platform. Note that you cannot edit game details if **This game has not been published yet** is checked. 

The Children’s Online Privacy Protection Act (COPPA) compliance notice requires you to indicate whether your game in intended for children under the age of 13 in the United States.

##### Creating a new Ads-enabled Project 
Follow these steps to configure a new Project for Ads:

1. From the **Projects** page, select **ADD NEW PROJECT**.
2. Select the **Create a new project and enable Unity Ads** radio button, then enter a name for the new Project.

<!-- insert image 
![Ad content filters](https://cdn.applifier.com/files/NewAdsProject.png)
-->

<!-- Caption: Creating a new Unity Ads-enabled Project in the dashboard.-->

3. Check the platforms (Apple App Store or Google Play) you wish to publish on. If the game is in development, check **This game has not been published yet**. If the game is released, uncheck that option and use the game’s lookup ID to link it to the dashboard (for more information on how to do this, see the above section on [Store details](#store-details-optional)). 

<!-- insert image 
![Ad content filters](https://cdn.applifier.com/files/EditPlatforms.png)
-->

<!-- Caption: Enabling platforms for a new Project in the dashboard.-->

#### Editing Projects
To edit your Project name or [transfer it to a different organization](https://support.unity3d.com/hc/en-us/articles/213524303-How-do-I-transfer-my-Project-to-a-different-Unity-Organization-), navigate to the **Develop** tab of the Developer Dashboard, then select **Settings** > **General** from the left navigation bar.

**Note**: These settings apply to all of your Project’s Unity Services, so take care making these changes. 

#### Archiving Projects
This [help article](https://support.unity3d.com/hc/en-us/articles/115000075126-How-do-I-archive-a-Project-) details how to archive old Projects that are cluttering your dashboard, and how to view or change the status of archived Projects.

### Test devices
#### Registering test devices
You can register an iOS or Android phone or tablet as a test device to test your Unity Ads integration without monetizing the device.

1. From the [**Operate** tab](https://operate.dashboard.unity3d.com) of the Developer Dashboard, select **Test Devices** from the left navigation bar.
2. Enter your device's name into the first input field.
3. Enter your **IDFA** (ID for advertising) into the second input field. For more information on locating your device's IDFA, review [this guide](http://blog.mparticle.com/how-to-find-your-mobile-device-identifiers/).

<!-- insert image 
![Ad content filters](https://cdn.applifier.com/files/RegisterTestDevice.png)
-->

<!-- Caption: Registering test devices on the dashboard.-->
