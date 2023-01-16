# Mobile-Deep-Linking
AprivaPay Mobile - Deep Linking Sample

Mobile Deep Linking 
What is Mobile Deep Linking?
The term “deep link” has come to mean the routes to specific spots on websites and to a native application via a link. A version of the term, called a “mobile deep link,” is a link that contains all the information needed to take a user directly into an app or a particular location within an app instead of just launching the app’s home page.

How to Create Deep Links
When you create a tracking link for your app, you can configure it to be a deep link. With a deep link, if a user clicks on this link and they already have your app installed, not only will the app open - but it will show specific app content of your choice, not just the app's default screen such as the checkout / payment total page on AprivaPay Mobile so that third party applications can pass payment requests over to AP Mobile. 

Step by Step

1. Plan the Deep Links for Your App
To begin, make a list of all the deep links you want to implement in your integrator guide for the app.
For each deep link, decide on the following:
•	The app content should open when the user clicks the deep link. (Checkout view so total or amlount can be passed over)
•	The fallback redirect - i.e., where you want to redirect the user if they don't already have the app installed on their device. Typically, you send them to the app store to download the app.
•	Whether you want the link to work as a deferred deep link. With a deferred deep link, even if the user doesn't have the app installed yet, and they click on the ad and get to the app store, the user sees the special content after they install the app and open it.

2. Create a Link Domain
Deep Links have the following structure, where [DOMAIN] is chosen by you:
https://[DOMAIN].link/[PARAMETERS]
Adding Dynamic Content to the Link
You can make a deep-link do even more work by adding data to it dynamically on a third party application. This data can then be read and used by your app if a user passes values from the third party app and then arrives into AP Mobile.  

Note for Developers: Using the _p Parameter
To add dynamic data to a deep -link, append the _p parameter and any value to the end of the deep-link Link URL. _p stands for "passthrough" and the value can be a URL-encoded JSON value or an unstructured string value. 
An exaple wuld be a ‘Pay Now via Mobile Pay’ button that links to: https:// apriva.link/_p=amount123 
The passthrough parameter value(s) here would allow an external app to pass over a payment value. 
