#architecture #backend #uber #blog-read 
* Notes from https://eng.uber.com/usl-ubers-unified-signup-and-login-stack/


* To maximize support, we made the decision to go web-based, so that USL would be supported by all clients that can open a web browser.
* We’re aware that as compared to a web based solution a native experience would be faster, so we’re constantly looking at ways to close this performance gap to the point where it’s unnoticeable to our customers.
* Being web-based, any security update or growth feature was instantly deployed to all users and didn’t require any mobile app upgrades, adding to developer velocity.
* With USL we have _combined_ signup and login flows in order to avoid forcing users to switch between them.
* We also have inbuilt deduplication and linking flows.



![[Pasted image 20220607123824.png|900]]

* Our Android clients open USL using a [trusted web activity](https://developer.chrome.com/docs/android/custom-tabs/#when-should-i-use-custom-tabs-vs-trusted-web-activity). Trusted web activities (TWAs) extend [Chrome custom tabs (CCTs)](https://developer.chrome.com/docs/android/custom-tabs), which help make transitions between native and web content more seamless without having to resort to a [WebView](https://developer.android.com/reference/android/webkit/WebView).
* USL itself is a web-based single-page application built using [FusionJS](https://fusionjs.com/): a plugin-based web framework for building universal React applications.
  

 ![[Pasted image 20220607124816.png|900]]
* The client application is responsible for just the presentation of the current state. It contains a main <Controller /> component, which reads from the Redux state and loads the current screen component on the UI.

* As we were building custom flows for each Uber app using native flows, this meant we could never deprecate an old flow. The backend systems became very complex and slowed us down when developing new features.
* On the backend, a user’s login and signup journey is represented as a graph, which is traversed by a state machine. A node in the graph is the screen the user sees.

![[Pasted image 20220607162627.png|800]]

![[Pasted image 20220607162755.png|1200]]

* 