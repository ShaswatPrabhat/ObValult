* The `<a>` and `<form>` elements have been around from the very beginning. 
* Links for a browser to get things from a [[server]], and forms for a browser to send things to a [[server]] (and get things in return). 
* With this two-way communication established as a part of the specification from the start, it has been possible to create powerful applications on the [[web]] forever.
* One of the things that distinguishes [[web]] architectures is _where the code lives.
* With Multi-Page Apps [[MPA]], all of the code _we_ write lives on the server. The UI Feedback code on the client is handled by the user’s browser.
* ![[Pasted image 20221012192134.png]]

* It’s important that successful [[mutations]] sent a redirect response rather than just the new HTML. Otherwise you’ll have the POST request in your history stack and hitting the back button will trigger the POST request again
* Mental model of [[MPA]]:  there was _some_ state and complicated flows handled primarily by cookies in the requests, for the most part everything happened within the time of a request/response cycle.
* This required full page refreshes for simple tasks 
* Animations were pretty hard