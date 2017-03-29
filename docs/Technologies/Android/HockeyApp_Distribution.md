#HockeyApp for beta distribution

[HockeyApp](https://hockeyapp.net) is a service provided by Microsoft to help developers manage mobile apps though all phases of developing. It provides features such as:  [Distribution](https://hockeyapp.net/features/distribution/), [Crash Reports](https://hockeyapp.net/features/crashreports/), [Feedback](https://hockeyapp.net/features/feedback/) and basic [User Metrics](https://hockeyapp.net/features/user-metrics/). However, as of today, there are more sophisticated solutions in the market for Crash Reporting (such as [Crashlytics](https://try.crashlytics.com) and [Firebase Crash Reporting](https://firebase.google.com/docs/crash/)) and User Metrics (such as [Google Analytics](https://developers.google.com/analytics/) and [Firebase Analytics](https://firebase.google.com/docs/analytics/)). This article focuses on the distribution feature of HockeyApp.

By using HockeyApp for distribution purposes we can make a beta release available for testers or send demos to clients. It is necessary to mention that as of today, the free version of HockeyApp only allows the management of 10 apps, refer to [pricing](https://hockeyapp.net/pricing/) for more updated information. 

This are the steps to follow in order to distribute an app for beta testing. 

1) **Creating a HockeyApp account:** First you need to [sign up](https://rink.hockeyapp.net/users/sign_up) to use this service. 

2) **Creating a new app in the dashboard:** This can be done by following this [tutorial](https://support.hockeyapp.net/kb/app-management-2/how-to-create-a-new-app). 

3) **Integrating the HockeyApp SDK:** HockeyApp has SDKs for [Android](https://support.hockeyapp.net/kb/client-integration-android/hockeyapp-for-android-sdk) and [iOS](https://support.hockeyapp.net/kb/client-integration-ios-mac-os-x-tvos/hockeyapp-for-ios). Integrating this SDKs in our app allow us to use the following features: 

* Collect crash reports from the beta testing.
* In-app feedback from testers. 
* Track basic user metrics such as number of users, number of sessions and session times. 
* Display an update dialog in the app once a new beta version is released. This allows testers to make an update directly form within the app.
* Force the authentication of a user through HockeyApp to prevent the usage of the app by non invited users. 


If you add code for using this features after integrating the SDK, it is necessary to make sure this code is not included in the release build of the app. Having this features such as HockeyApp´s feedback, automatic updates or force authentication in a release build can confuse end users, make them download a beta build that is not ready for release or deny the usage of the app altogether, respectively. For features such as Crash Reporting and User Metrics in a production environment, refer to the other solutions discussed in the beginning of this article. A way of encapsulating this code and use it only in a beta build in Android is configuring a [build type](https://developer.android.com/studio/build/build-variants.html#build-types) or [product flavor](https://developer.android.com/studio/build/build-variants.html#product-flavors), as long as the code is not ran in the release build you are good to go. 

The integration of this SDK is not necessary if you are not interested in the features exposed above. The app can still be distributed and downloaded using the dashboard and native apps discussed in the next steps. By not using the SDK you will only receive information about the number of Downloads the app has and which user downloaded it, on top of that, there is no update option so the user will need to uninstall the previous build and reinstall the new one. 

4) **Creating a new version for the app in the dashboard:** This can be done using this [tutorial](https://support.hockeyapp.net/kb/app-management-2/how-to-create-a-new-version). Subsequent version released can be managed in the same manner. 

5) **Downloading the native apps of HockeyApp:** Android and iOS [native apps](https://hockeyapp.net/apps/) are provided to download and manage beta distributions. This apps will also allow beta testers to download the distribution of new versions of the app. If the SDK is not integrated, there will be no limitation as to who can install and use the beta app once it is downloaded from the HockeyApp native app (this could be achieved with the force authentication feature). Once the app is downloaded and installed you should login with your credentials and see if you can see and download the beta version that you created in the previous step.  

6) **Invite new beta testers:** This can be done by following this [tutorial](https://support.hockeyapp.net/kb/app-management-2/how-to-invite-beta-testers). You will usually use the Invite User feature in the dashboard and send an email invitation to the tester / client you want to invite. Once the user accepts the invitation you will be able to manage it by defining which apps he can see, adding him to a team, editing his information or deleting him all together. You can also restrict a version of the app so that just some users can download it. For more information on managing users follow this [link](https://support.hockeyapp.net/kb/app-management-2/how-to-manage-users-and-restrict-builds). 

##Android Specific

Here is a short guide oriented to Android clients that had not used HockeyApp before:

1) Accept the HockeyApp invitation that will arrive to your email address and create a new account.
2) Download the HockeyApp native app to your device and login with your credentials.
3) Browser the Android apps and tap <BETA APP NAME>. If by any chance you can´t see the app listed, notify us and we can give you permission to see it.
4) Download the available version of the apk for beta testing and install it.

During this process you might need to enable the installation of apps from unknown sources. This is necessary because Android by default prevents the installation of apps that doesn’t come from the Google Play Store for security reasons. The location of this setting varies between different device brands but it is usually located in Settings -> Security -> Device Administration - > Unknown sources. Simply enable this option.


If you have not integrated the HockeyApp SDK for update dialogs you might also need to ask the client to uninstall the previous version of the beta app before installing any new version. 


##Other useful links: 

* [HockeyApp Knowledge Base:](https://support.hockeyapp.net/kb) In this link you can find information and guides on pretty much all HockeyApp has to offer, as well as forum discussions of other developers that might have encountered the same problems as you.  
* [HockeyApp Support:](https://support.hockeyapp.net) For asking questions and starting new discussions in their forum if necessary. 

