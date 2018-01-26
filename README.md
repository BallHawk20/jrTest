/*
Title: Best Practices guide    
Sort: 100  
*/


## Overview
Incorporating Unity Ads is simple, but maximizing monetization requires an effective implementation strategy. When considering this, it is important to first understand how Unity Ads generates revenue, then determine the design and placement of ads in your game accordingly. In this guide, we share effective strategies and tips for optimizing your Unity Ads implementation using **Rewarded Ads**. 

**Note**: Be sure to check out the in-depth [case studies](#case-studies-and-references) at the bottom of the guide!

## Understanding how ads generate revenue
Every time your game requests an ad, Unity Ads holds an open auction for advertisers to bid on your impression. The highest bidder provides an ad. Advertisers can bid on different impression types to provide a diverse source of revenue streams. The following types are listed in escalating order of expected earning potential:
 
1. Ad start (the player triggers an ad)
2. Completed view (the player watches an ad to the end)
3. Click (the player clicks the ad, leading to an external product link)
4. Install (the player clicks out to the external product page and installs the product)   
 
Your **eCPM** (effective cost per 1000 impressions), represents your overall blended revenue across these streams. The key to maximizing your eCPM is designing your ads to consistently generate the highest quality impressions. 

For an in-depth look at Unity Ads metrics, KPI, and terminology, see documentation on [Monetization statistics](https://unityads.unity3d.com/help/monetization/statistics).  

## Rewarded Ads
Rewarded Ads provide in-game rewards to players in exchange for watching ads. 

### Why use Rewarded Ads?
When done right, the incentive to voluntarily watch ads makes Rewarded Ads an extremely effective form of marketing as it helps create a positive player experience. Rewarded Ads monetize better, typically yielding higher quality impressions. They can also drive help engagement and retention. As a byproduct, they increase the likelihood of players investing further through in-app purchases.

### Implementing Rewarded Ads effectively
Like any other game mechanic, remember that effective ads implementation requires carefully considered game design. Think of the following tips as recommendations; the best approach will ultimately depend on the specifics of your game and incorporate input from marketing, production, and game design disciplines within your team. To learn more about design-driven monetization, watch [this presentation](https://youtu.be/s1AhKkP9nCc) from Unite ‘16.   

#### Let the player choose
Allow players to opt in to watching ads, so they can choose between skipping them or receiving a reward. When players voluntarily watch an ad, they are more likely to pay attention and show interest in the advertised product. This is turn increases the quality of your impressions.

![Opt-in Rewarded Ad](https://cdn.applifier.com/files/Rovio1.png)
> _Example of rewarded ads implementation with opt-in, courtesy of Rovio._

#### Identify the right incentive
Encouraging players to voluntarily watch an ad requires a compelling incentive. Successful implementations tend to offer in-game currency, power-ups, additional lives, or consumable items such as potions that help players recover and flourish in the game. 

![Incentivized ads](https://cdn.applifier.com/files/Zynga1.png)
> _Example of implementing rewarded ads to provide unlock keys, courtesy of Zynga._

#### Identify the right placement
Take the above tip a step further, by choosing the right incentive at the right time and place. When considering your ad [Placements](https://unityads.unity3d.com/help/monetization/placements-and-filters), think about stress points in your game that might be a good opportunity for an injection of resources. Consider the following examples to spur the creative process:

- Implement a special shop type that allows the player to purchase unique items in exchange for watching an ad.

![Specialty Merchant](https://cdn.applifier.com/files/NextGames.png)
> _Example of implementing rewarded ads as a specialty merchant, courtesy of Next Games._

- Augment retention mechanics by boosting their rewards in exchange for watching an ad. For example, double the rewards from a daily login bonus, or offer extra daily attempts to win in-game prizes. 

![Double Login Bonus](https://cdn.applifier.com/files/Futureplay1.png)
> _Example of implementing rewarded ads to boost daily login bonuses, courtesy of Futureplay._

![Extra Spins](https://cdn.applifier.com/files/Zynga2.png)
> _Example of implementing rewarded ads to provide extra chances at prizes, courtesy of Zynga._

- Create a fun mini-game available to players that choose to watch an ad.

![Carnival Mini-Game](https://cdn.applifier.com/files/Futureplay2.png)
> _Example of implementing rewarded ads as a mini-game, courtesy of Futureplay._

- Allow players to continue playing if they run out of lives, in exchange for watching an ad.

![Continue Playing](https://cdn.applifier.com/files/Rovio2.png)
> _Example of implementing rewarded ads to provide extra lives, courtesy of Rovio._

- When starting a new game session, promote engagement by presenting a chance to receive 30 minutes of double points or earned currency in exchange for watching an ad. 

![Double Currency](https://cdn.applifier.com/files/Futureplay3.png)
> _Example of implementing rewarded ads to boost earned currency for a period, courtesy of Futureplay._

- Offer a power-up or boost if the player is about to lose, in exchange for watching an ad.

![Avoid Losing](https://cdn.applifier.com/files/Twimler.png)
> _Example of implementing rewarded ads to stave off losing, courtesy of Twimler._

- Get creative! Offer players earned currency when they don’t have enough to purchase an item at a shop; place a character or shop right before a challenging boss fight that offers to completely heal and regenerate the player character’s resources; offer a unique consumable boost to help push players who continue to fail a mission over the top. 

As you can see, many of these examples drive retention and engagement in addition to boosting the quality of impressions.

#### Pair Rewarded Ads with in-app purchasing
Because Rewarded Ads are effective retention mechanics, they complement in-app purchasing systems quite well. Rewarded Ads often generate engagement through reward and investment, which encourages further investment through other monetization channels. Strive for a diverse monetization approach that provides opportunities for both. For example, consider running Rewarded Ads that grant small amounts of premium currency, offsetting the cost of paid content. Players with a little premium currency may buy more to supplement a purchase they’re eyeballing, rather than let their currency go to waste. For more insight, read [How to get the most out of currency sales](https://blogs.unity3d.com/2016/12/07/just-in-time-for-the-holidays-how-to-get-the-most-out-of-currency-sales/).

Remember, it’s important that your ads integration encourages in-app purchases instead of competing with them and cannibalizing revenue (see section below).

#### Don’t lose sight of your game’s economy
Ad rewards should complement in-app purchase items rather than compete with them. As a general rule, Rewarded Ads should provide small benefits that drive engagement & retention, while in-app purchases should provide larger benefits that feel worth the financial investment. When possible, try to avoid offering purchasable items as ad rewards. 

Aside from not wanting to cannibalize in-app purchase revenue, remember that Rewarded Ads infuse the game economy with more digital goods. This can impact game balance and diminish the value of other rewards if not done responsibly. Game designers typically craft their in-game economies meticulously, so double-check that your implementation isn’t harmful in that regard and always design incentives in keeping with their expected values within the economy.  

Examples:
- If a special sword sells in the IAP store for $4.99, but players can get it in exchange for watching an ad, they will never have a reason to buy it. Offering small amounts of premium currency that can be applied towards purchasing the sword is a better approach.
- If the reward for watching an ad is on par with the reward for winning an extremely challenging battle, the experience of succeeding feels cheapened and can hurt engagement. 
- If a health potion costs 100 Gold, but players can get health potions free at any time for watching an ad, that can devalue health potions and potentially even Gold itself. 

#### Take advantage of ad filters
Unity Ads has robust tools for filtering the ad content you show. No one understands your game’s demographics better than you; targeting them with content that is relevant to their interests enhances the likelihood of interacting with that content and creating higher quality impressions. The [Ads Monetization Dashboard](https://operate.dashboard.unity3d.com) allows you to exclude content based on genre, age rating, and theme. For a complete guide on using ad filters, see documentation on [**Placements and filters**](https://unityads.unity3d.com/help/monetization/placements-and-filters).

#### Preserve the user experience
Design your ads to fit your game, with as little disruption to the user experience as possible. For example, if you choose to implement interstitial ads, use them strategically and strive to place them at natural pauses or breaks in gameplay, such as a load or level change. 

In general, focus on well-designed ad placements and incentives rather than sheer volume. A great ads implementation becomes part of the game experience, making it more enticing for players to engage. Done right, it can be a positive experience that players look forward to repeating on top of the reward incentive. At the end of the day, your ads monetization success depends on this engagement, as building traffic and DAU in turn boosts impressions.  

## Case studies and references
Next Games used rewarded ads to increase player LTV. 
- [Read the Next Games case study](http://response.unity3d.com/ads-case-study-next-games)
- [Watch the Unite Europe 2016 talk](https://www.youtube.com/watch?v=Hl3HJdfJ8vs)

Cheetah Mobile achieved a 16% revenue increase and 10% 2nd day retention increase with Unity Ads.
- [Read the Cheetah Mobile case study](https://create.unity3d.com/ads-case-study-cheetah)

A hobbyist developing games in his spare time used Unity Ads to help grow to 10 million-plus downloads.
- [Read the Twimler case study](http://response.unity3d.com/mobile-case-study-twimler)

Unity Ads helped Playdots, Inc. monetize an enormous user base in a way the players have embraced.
- [Watch the video](https://www.youtube.com/watch?v=nig-Zy-G_PM)

Futureplay showcases how Unity Ads drives revenue through engagement and retention.
- [Read the Futureplay case study](http://response.unity3d.com/ads-case-study-futureplay) 

Unity Ads helped Game Hive monetize an expanding user base without alienating players by pioneering a best practice model for ‘view-to-play’ monetization en route to over 100 million downloads across iOS and Android.
- [Read the Game Hive case study](http://response.unity3d.com/ads-case-study-game-hive)

Want to learn more? Unity Blogs has plenty of additional reading: 
- [A Designer’s Guide to Using Video Ads](https://blogs.unity3d.com/2015/04/15/a-designers-guide-to-using-video-ads/)
- [Best Practices for Rewarded Video Ads](https://blogs.unity3d.com/2016/04/20/best-practices-for-rewarded-video-ads-2/)
- [Zynga & Unity: Exclusive Rewarded Advertising](https://blogs.unity3d.com/2017/08/02/zynga-unity-exclusive-rewarded-ads/)
