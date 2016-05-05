## Cordova Plugin for AdMob

Forked from https://github.com/floatinghotpot/cordova-admob-pro in response to https://github.com/floatinghotpot/cordova-plugin-admob/issues/205.

Simple and easy plugin to monetize your HTML5 hybrid apps and games.

Usage:
```bash
cordova plugin add https://github.com/floatinghotpot/cordova-plugin-admob
```

Example Code:
```javascript
        window.plugins.AdMob.setOptions( {
          publisherId: admobid.banner,
          interstitialAdId: admobid.interstitial,
          bannerAtTop: false, // set to true, to put banner at top
          overlap: false, // set to true, to allow banner overlap webview
          offsetTopBar: false, // set to true to avoid ios7 status bar overlap
          isTesting: false, // receiving test ad
          autoShow: true // auto show interstitial ad when loaded
        });
        // display the banner at startup
        window.plugins.AdMob.createBannerView();
        
        // create interstitial ad
        window.plugins.AdMob.createInterstitialView();
        window.plugins.AdMob.showInterstitialAd(
          true, 
          function(){},
          function(e){alert(JSON.stringify(e));}
        );
```
