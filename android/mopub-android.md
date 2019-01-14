# MoPub Android

[Resources](#Resources)

[Setup](#Setup)

[Native](#Native)

---

## Resources

**Community**

[github.com/mopub/mopub-android-sdk/issues](https://github.com/mopub/mopub-android-sdk/issues)

**Documentation**

[Android](https://developers.mopub.com/docs/android/)

**Samples**

[Ad Placer (via MoPubAdAdapter)](https://github.com/mopub/mopub-android-sdk/blob/master/mopub-sample/src/main/java/com/mopub/simpleadsdemo/NativeListViewFragment.java)

[Ad Placer (via MoPubRecyclerAdapter)](https://github.com/mopub/mopub-android-sdk/blob/master/mopub-sample/src/main/java/com/mopub/simpleadsdemo/NativeRecyclerViewFragment.java)

## Setup

[Getting Started](https://developers.mopub.com/docs/android/getting-started/#add-a-network-security-configuration-file)

[Issue: Could not find _moat-mobile-app-kit_](https://stackoverflow.com/a/54057021/2253682)

Facebook - [Android Network Security Config](https://developers.facebook.com/docs/audience-network/android-network-security-config)

[Integrate MoPub Mediation Adapters](https://developers.mopub.com/docs/mediation/integrate/)

[Usage With Existing RecyclerAdapter](https://developers.mopub.com/docs/android/native/#method-2-ad-placer-via-mopubrecycleradapter)

## Native

[Native](https://developers.mopub.com/docs/android/native/)

Facebook, Flurry - [Set up your ad renderers](https://developers.mopub.com/docs/android/integrating-networks/#native-ad-set-up-your-ad-renderers) (required)

**Modifying Original Adapter**
     
     adapter.organizeContent(moPubAdapter.getOriginalPosition(viewHolder.adapterPosition))

**Content Change Strategy**

    moPubAdapter.setContentChangeStrategy(MoPubRecyclerAdapter.ContentChangeStrategy.KEEP_ADS_FIXED)

**Test Ad Unit ID:** _11a17b188668469fb0412708c3d16813_