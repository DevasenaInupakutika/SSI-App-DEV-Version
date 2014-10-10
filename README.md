This repository is for the Institute's development version of Android Mobile Application with some feature bug fixes to V0.1 of the application in Google Play Store production.

Google Play Store V0.1 is present at below link:

https://play.google.com/apps/publish/?dev_acc=05870928095713950316#AppListPlace

A brief description on methods used for WebView Caching:

Use of WebSettings.LOAD_CACHE_ELSE_NETWORK in METHOD 1 (currently commented in detail fragment activity) tells the WebView to load the page from cache but if it needs anything that
isn't in cache, it looks to the network, and when we don't have connection, it will just show blank screen/ activity. This is because unfortunately not everything is stored in
cache and even with the above setting in METHOD 1, browser/ WebView client (in our app's case) uses network.

In order to get the WebView ignore no connection is to use:

WebSettings.LOAD_CACHE_ONLY cache mode instead (METHOD II). Some images still will not load with this setting since they weren't cached but it loads everything it finds in cache.


