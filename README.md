## Open Authentication Module
<table>
<tr> 
    <td bgcolor="#DDD"> Name</td><td>Open Authentication Module</td>
</tr>
<tr> 
    <td bgcolor="#DDD"> Author</td><td>Erwin 't Hoen</td>
</tr>
<tr> 
    <td bgcolor="#DDD"> Company</td><td>FlowFabric</td>
</tr>
<tr> 
    <td bgcolor="#DDD"> Type</td><td>Module</td>
</tr>
<tr> 
    <td bgcolor="#DDD"> Latest version</td><td>1.1</td>
</tr>
<tr> 
    <td bgcolor="#DDD"> Package name</td><td>OauthModule_v1.1.mpk</td>
</tr>
<tr> 
    <td bgcolor="#DDD"> Released</td><td>10-03-2014</td>
</tr>
</table>

##Description


The Open Authentication Module allow you to setup your app for authentication users with their Google, Linkedin or Facebook account.
The module can easily be expanded to incorporate any OAuth 2 provider.
###Services that support OAuth 2
<table>
<tr>
<td>
* <a href="http://groups.google.com/group/37signals-api/browse_thread/thread/86b0da52134c1b7e">37signals (draft 5)</a>
* <a href="http://developers.box.com/oauth/">Box</a>
<li> <a href="http://beeminder.com/api">Beeminder</a></li>
<li> <a href="http://www.campaignmonitor.com/api/getting-started/#authenticating_with_oauth">Campaign Monitor</a></li>
<li> DailyMotion
<li> <a href="https://do.com">Do.com (draft 22)</a></li>
<li> <a href="https://www.dropbox.com/developers/core/docs#oa2-authorize">Dropbox</a></li>
<li> <a href="http://developers.facebook.com/docs/authentication/">Facebook</a></li> <a href="http://www.sociallipstick.com/?p=239">(see here)</a></li>
<li> <a href="https://developer.foursquare.com/overview/auth">Foursquare</a></li>
<li> <a href="https://developers.geoloqi.com">Geologi</a></li>
<li> <a href="http://developer.github.com/v3/oauth/">Github</a></li>
<li> <a href="https://developers.google.com/accounts/docs/OAuth2">Google</a></li>
<li> <a href="https://developer.linkedin.com/documents/authentication">Linkedin</a></li>
<li> Mailchimp
</td>
<td>
<li> <a href="http://www.meetup.com/meetup_api/auth/#oauth2">Meetup</a></li>
<li> <a href="http://nationbuilder.com/api_quickstart">Nationbuilder</a></li>
<li> Paypal
<li> Reddit
<li> <a href="http://www.salesforce.com/us/developer/docs/api_rest/Content/quickstart_oauth.htm">Salesforce</a></li>
<li> Scoop.it
<li> <a href="http://www.sharefile.com/">Sharefile Citrix</a></li>
<li> StockTwits
<li> <a href="http://developers.soundcloud.com/docs/api/reference">Soundcloud</a></li>
<li> Vimeo
<li> <a href="http://msdn.microsoft.com/en-us/library/live/hh243647.aspx">Windows Live</a></li>
<li> WePay
<li> Wordpress
<li> Yahoo
<li> Yammer
</td>
</table>
*For a complete list see <a href="http://www.cheatography.com/kayalshri/cheat-sheets/oauth-end-points/">here</a>*

## Typical usage scenario


If you want to have your users login to their Mendix app with their credentials from their favorite social network. For example when using Chrome the user already logs in automatically into their Google account, then the Oauth module will allow the user to be logged in directly into their Mendix app (SSO).


If you need 2-factor authentication for accessing your app, then make use of the options that Google offers for this purpose in stead of build 2-factor authentication from scratch in your app. <br>
Using a corporate Google account, users can be setup so that the login process will require 2-factor authentication This](https://support.google.com/a/answer/184711?hl=en) is how you set this up on Google

## Features and limitations


<li> Authenticate users via Facebook, Google or Linkedin OOTB</li>
<li> Or use only one of these providers (pick and choose)</li>
<li> Style your own fault pages</li>
<li> Easily add your own Oauth 2 provider</li>
<li> Determine how you identify your authorized users based on the data provided by the Oauth provider <br>&nbsp;&nbsp;  (OOTB this is done based on the email address)</li>
<li> Implement your own logic for authentication of users even add user provisioning with a simple microflow</li>
<li> If you do not implement user provisioning then the users have to be known in the app by integration to an &nbsp;&nbsp;&nbsp;Active Directory or an Identity Management solution</li>
<li> Control if an Admin can login via the standard Mendix login circumventing the Oauth login via adaptation in &nbsp;&nbsp;&nbsp;your theme directory</li>


## Installation & Configuration

1. Download the zip file from Github
2. Extract the zip
3. Import the module (.mpk) into you application as a new module
4. From the theme directory copy all the files to your theme directory
5. Connect the page and microflow from the #Implementation folder to your navigation Assign the permissions to the userrole(s)
6. Import the Community Commons module from the app store if not already part of your project
7. Import the Model Reflection module from the app store  if not already part of your project
8. Set the microflow AS_StartOauthRequestHandlers as after Startup microflow
9. Add the attribute Email to the Administration.Account entity
10. To setup your Oauth module navigate to https://<yourapp>/adminlogin.html and login with your Admin account
11. Synchronize your Model Reflection module and make sure that the data for the OauthModule is created
12. Select the Oauth Config menu item and select the microflow ResolveUserByEmail
13. And you're done!
 

14. Wait, what if security requirements are more strict? Perform step 15
15. Delete the adminlogin.html from your theme folder to make sure that Oauth is the only login option, and redeploy your app
16. Done!


## Dependencies
 

1. Mendix 5.8.1 Environment
2. Mx Model Reflection module
3. Community Commons module


## Known bugs
 

* None so far
 

## Frequently Asked Questions
Ask your question at the Mendix Community Forum](https://mxforum.mendix.com/)

* None




