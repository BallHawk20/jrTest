## Adding a new creative pack
In the Creative packs section of the campaign page, select **CREATE** (or **CREATE CREATIVE PACKS** if none exist yet).

![Setting up a new creative pack.](https://github.com/Applifier/unity-ads/wiki/advertising/NewCreatives.png)
<p align="center"><i>Setting up a new creative pack.</i></p>

Enter a **creative pack name**, then upload **end card** and **video** assets (detailed below).

### Creative asset specs
#### End cards
End cards are creative assets displayed at the end of an ad with a call to action for users to download the advertised product. 

Select **Square** end cards from the dropdown menu to upload one creative format that will work on any device, in any orientation, and any aspect ratio (recommended to prevent cropping and maximize compatibility).

Select **Portrait & landscape** end cards from the dropdown menu to upload one creative for each device orientation.
 
**Note**: Dynamic cropping may occur when using landscape and portrait images, to account for different device sizes. To avoid losing critical information, allow a 100-pixel buffer from the top and bottom edges of landscape images, or left and right edges for portrait images.
 
- Use JPG or PNG format.
- Use 800 x 800 (1:1) pixel resolution for square images
- Use 800 x 600 (4:3) pixel resolution for landscape images
- Use 600 x 800 (3:4) pixel resolution for portrait images.
- (Apple only) Due to Apple requirements, Unity recommends only depicting the Apple app store logo on end cards for iOS videos. See [Apple marketing guidelines](https://developer.apple.com/app-store/marketing/guidelines/#badges) for more information.

#### Videos
Video ad assets marketing your app. While only one video is required, uploading a video for each orientation yields better optimization. When a creative contains both, Unity’s valuation algorithm selects the best orientation to display.

- 30 seconds or less.
- H.264-encoded MOV, MP4, or AVI format.
- 16:9 pixel ratio for landscape videos, or 9:16 pixel ratio for portrait videos.
- Recommended file size is 10MB. Maximum file size is 100MB. Videos are re-encoded to be suitable for various bitrates. The final video shown will be optimized for the user's available network speed and cache settings.
- (Apple only) Due to Apple requirements, we recommend only depicting the Apple app store logo. See [Apple marketing guidelines](https://developer.apple.com/app-store/marketing/guidelines/#badges) for more information.

![Uploading creative assets for your campaign.](https://github.com/Applifier/unity-ads/wiki/advertising/UploadCreatives.png)
<p align="center"><i>Uploading creative assets for your campaign.</i></p>
 
When finished uploading creative assets, click **CREATE**. Your new creative pack now appears in the campaign’s **Creative Packs** list with a **Processing** status. This status indicates that your creative pack is undergoing moderation (see section on **Moderation** below). Click **ASSIGN** to choose which creative packs to include with the campaign. Note that selecting the downward arrow expands the creative pack’s details.
