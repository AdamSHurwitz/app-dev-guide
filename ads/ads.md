# Ads

[MoPub](#MoPub)

[Facebook](#Facebook)

---

## MoPub

### Resources

**Documentation**

[Publisher UI](https://developers.mopub.com/docs/ui/)

[Mediation](https://developers.mopub.com/docs/mediation/)

   - [Integrate MoPub Mediation Adapters](https://developers.mopub.com/docs/mediation/integrate/)

**Community**

[Twitter Forum](https://twittercommunity.com/)

### [Android](../android/mopub-android.md)

### [Flutter](../flutter/mopub-flutter.md)

### Sources
#### Marketplace

   About: Advertisers bid against each other for placements through _DSPs_ (Demand Side Partners).

   [Documentation](https://developers.mopub.com/docs/ui/marketplace/)

#### Networks

   About: Show ads from specific networks using mediation for competitive bidding.

   [Networks](https://developers.mopub.com/docs/ui/networks/)
   
   [Mediation](https://developers.mopub.com/docs/mediation/)

   Best practices
   - Use unique network IDs per ad unit. 
   - Reduce [latency](https://developers.mopub.com/docs/mediation/waterfall-latency-and-best-practices/#latency-types-summary)
      - Minimize ad sources in waterfall. (ie:  removing low-CPM and low-fill network partners)
      - Set items at the same priority to parallelize requests improving latency and CPMs due to competition. 

#### Orders & Line Items

   About: Direct sale or in-house ads.

   [Documentation](https://developers.mopub.com/docs/ui/orders/#line-item-types)

- Guaranteed: Will always show. Used for direct buys. _Default is Priority 6_
- Promotional: House ads or in-app purchases. _Default Priority 10_
- Marketplace: Set a geo floor price for marketplace, or to prioritize Marketplace higher than network campaigns. _Default Priority 10_
- Network: One-time network campaign at a higher priority than your other network campaigns. Used to run a network with limited budget or time period. _Default Priority 10_
- Non-Guaranteed: Campaign without a guaranteed number of impressions. _Default Priority 12_
- Backfill: Promotional line item like house ads. _Default lowest Priority level, 16_

   ##### Targeting
   [Documentation](https://developers.mopub.com/docs/ui/orders/line-item-targeting/)

   - Geo
   - Installed apps (that you own)
   - Custom data (sent from client)

### Organize With Segments

[Documentation](https://developers.mopub.com/docs/ui/segments/)

Grouping
- Ad units/Apps
- Ad networks
- Geography

Best Practices

- Assign CPM to each segment and containing units/networks.
- Don't overlap segments.
- Each country is only present in a single segment in order to see complete network waterfall in one segment.


### Native

[Supported Networks Chart](https://developers.mopub.com/docs/mediation/supported-mediation-partners/)

[Best Practices](https://developers.mopub.com/docs/publisher/best-practices/native-ads/)

#### Attributes

- Frequency Caps (per user)
   - hourly impressions
   - daily impressions

- Ad Positions: show ads every _number_.

**Test**

Setup direct campaign from [_Orders_](https://developers.mopub.com/docs/ui/orders/) tab.

or

Use ad unit ID with sample ads: 76a3fefaced247959582d2d2df6f4757

#### Ad Unit Ids

_Apps_ > _appName_ > _adUnitName_ > _Edit Ad Unit_ > _View code integration_

![ad unit id](images/ad_unit_id.png)

## Facebook

### Resources

[Mediate Facebook](https://developers.mopub.com/docs/mediation/networks/facebook/)

[System User Token Generation](https://developers.facebook.com/docs/audience-network/reporting-api/systemuser/) (Used to enable MoPub reporting access.)

[Testing Audience Network Implementation](https://developers.facebook.com/docs/audience-network/testing/#testing-real)