/*
Title: Placements & filters
Sort: 60
*/


## Overview
Placements are triggered events within your game that display ads from the Unity network. How you choose to implement them is entirely up to you. Our **[Best practices guide](https://unityads.unity3d.com/help/monetization/design-guide)** provides some advice and examples of effective implementation. Settings in the [Ads Monetization Dashboard](https://operate.dashboard.unity3d.com) control how those Placements display ad content. 

## Managing Placements
1. From the [Operate tab](https://operate.dashboard.unity3d.com) of the Developer Dashboard, select your Project.
2. Select **Platforms** from the left navigation bar to view a list of your Project's active platforms.
3. Select the platform with Placements to manage.

### Default Placements
The **AD PLACEMENTS** tab displays a list of all Placements associated with the Project and platform. Newly created Projects include two default Placements:

- **Video**, which allows users to skip the ad after 5 seconds
- **Rewarded Video**, which requires user opt-in to watch a video in exchange for incentives, but does not allow skipping

<!-- insert image 
![Platform Placements list](https://cdn.applifier.com/files/PlatformPlacementsList.png)
-->

Rewarded Video Placements are often the most effective implementation of Unity Ads in your game. Learn more about why in our **[Best practices guide](https://unityads.unity3d.com/help/monetization/design-guide)**.

### Creating New Placements
To create a new Placement, select **ADD NEW PLACEMENT** to open the **Create a new placement** configuration window. Next, specify the following fields:

- Check **Rewarded video** to make the ads displayed through this Placement unskippable.
- Select the ad **Type** to display through this Placement (currently, **Video** is the only option). 
- **Name** the Placement. The **Placement ID**, which you call in your code implementation, automatically populates based on your entry.
- Check **mute audio** if you want the ad to default to muted audio.
- If you did not check **Rewarded video**, you can specify the number of seconds to **Allow skip after** for ads displayed through this Placement.

<!-- insert image 
![Create new Placement](https://cdn.applifier.com/files/CreateNewPlacement.png)
-->

<!-- Caption: Creating a new Placement in the dashboard.-->

### Editing existing Placements
Select **EDIT** next to the Placement you wish to edit to bring up the **Edit placement** configuration window. You can edit the same fields available through the Placement creation process.

**Note**: You cannot edit the **PlacementID**, nor does it change if the Placement **Name** does.

## Filtering ad content
Unity Ads provides tools to refine your ad Placement strategy by targeting specific demographics with specific content.
 
1. From the [Operate tab](https://operate.dashboard.unity3d.com) of the Developer Dashboard, select your Project.
2. Select **Platforms** from the left navigation bar to view a list of your Project's active platforms.
3. Select the platform with Placements you wish to filter.
4. Select the **AD FILTERING** tab to bring up the configuration menu. Here you can exclude ad categories to suit your game's target audience, using the following filter criteria:
   - A) Check options in the **GAME CATEGORIES** section to filter out ad content for games of a certain genre.
   - B) Check options in the **OTHER CATEGORIES** section to filter out ad content for games containing certain content or themes.
   - C) Check options in the **EXCLUDE CONTENT** section to filter out ad content for apps targeting specific age ratings. 
5. Select **SAVE** to apply your selected filters.

<!-- insert image 
![Ad content filters](https://cdn.applifier.com/files/AdContentFilters.png)
-->

<!-- Caption: Applying ad content filters in the dashboard.-->

Using a combination of these three sections is the best way to ensure certain content gets excluded. For example, if your game targets users under 13 years old, checking the following would safely  reduce the possibility of them seeing ad content related to gambling:

- [GAME CATEGORIES] Casino
- [OTHER CATEGORIES] Lottery and Gambling 
- [EXCLUDE CONTENT] Do not show ads rated 13+

**Note**: Filtering ad content is often advantageous, but it can negatively impact revenue by creating smaller ad pools to draw from. For more information on this trade off, please read our **[Best practices guide](https://unityads.unity3d.com/help/monetization/design-guide)**.

Please contact [Unity Ads support](mailto:unityads-support@unity3d.com) if you have additional questions or unique requests regarding ad filtering.

## Implementing Placements in-game
### Initialization
Your game must initialize Unity Ads for the service to work properly. If you enable Unity Ads through the Services window (**Window** > **Services**), the service is auto-initialized. If you enable Unity Ads through the dashboard, you must call the initialize function from your Ads Manager class. Please refer to the integration guides for information on executing this for your platform.

### Calling Placements in code
To trigger a Placement in your game, implement the following code, using the desired Placement ID string established on the dashboard:

```
// Display an ad using placementID Placement
if(Advertisement.IsReady(“placementID”))
{
	Advertisement.Show(“placementID”);
}
```

If you do not specify a Placement ID, Unity Ads selects the default Placement specified in your Dashboard settings. For example:

```
// Display an ad using the default Placement
if(Advertisement.IsReady())
{
	Advertisement.Show();
}
```

For a new Project, this code calls the “video” Placement ID, as it is the default setting.

This is the same in C#, Obj-C, Swift, & Java:

#### Unity (C#)
```
if(Advertisement.IsReady("placementID")) 
{
	Advertisement.Show("placementID");
}
```

#### iOS (Obj-C)
```
if ([UnityAds isReady]) 
{
	[UnityAds show:self placementId:@"placementID"];
}
```

#### Android (Java)
```
if (UnityAds.isReady()) 
{
	UnityAds.show(this, "placementID");
}
```

## Fill rate
Unity Ads has a global fill rate of greater than 95%, but some regions outside of America and Europe that might have smaller ad pools won't always have ads available. It's important to check whether ads are available before showing ads to your users.

For more tips on maximizing impressions, see the **[Best practices guide](https://unityads.unity3d.com/help/monetization/design-guide)**. If you are interested in further restricting the maximum number of ads users can view, please contact [Unity Ads support](mailto:unityads-support@unity3d.com). 


