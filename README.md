This is our test branch of the below project. Things we'll be working on specifically: 

- [ ] Fixing Android pie notification issue. 
Seems to be Android wide. Multiple threads over the internet about notifications missing in multiple apps. Suspected solution is to build against SDK28. 
https://stackoverflow.com/questions/52827915/notification-is-not-showing-in-android-9

- [ ] Fix noise dampening/cancellation issues in video chat (echoes on the line). 
We aim to use hardware noise cancelling as per the article below. 
https://twigstechtips.blogspot.com/2013/07/android-enable-noise-cancellation-in.html

See below. 
https://developer.android.com/reference/android/media/audiofx/AcousticEchoCanceler
https://developer.android.com/reference/android/media/audiofx/NoiseSuppressor



- [ ] Import existing TOX accounts. 
Need to look though the code to work out what's going on and how to implement. 
Easy fix? https://wiki.tox.chat/users/import_export

- [ ] Add offline messaging capability. 
If user offline, add to db and attempt to resend every 5 seconds for 5 mins, drop to every 15 seconds after that. Drop down lower later? Consider traffic etc. and power implications. 

- [ ] Add Back button to chats. Take back to chat list.  

# Tox Reference Implementation for Android [TRIfA]

~~This is not a Reference Client, it's c-toxcore for Android.~~<br>
This is now also a Tox Client for Android.

<a href="https://f-droid.org/app/com.zoffcc.applications.trifa"><img src="https://gitlab.com/fdroid/artwork/raw/master/badge/get-it-on.png" width="200"></a>
<a href='https://play.google.com/store/apps/details?id=com.zoffcc.applications.trifa'><img alt='Get it on Google Play' src='https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png' height='80px'/></a>


Build Status
=
**CircleCI:** [![CircleCI](https://circleci.com/gh/zoff99/ToxAndroidRefImpl/tree/zoff99%2Fdev003.png?style=badge)](https://circleci.com/gh/zoff99/ToxAndroidRefImpl/tree/zoff99%2Fdev003)
**Bintray:** [![Download](https://api.bintray.com/packages/zoff99/maven/trifajni/images/download.svg)](https://bintray.com/zoff99/maven/trifajni/_latestVersion)
**Methods:** <a href="http://www.methodscount.com/?lib=com.zoffcc.applications.trifajni%3Atrifa-jni-lib%3A%2B"><img src="https://img.shields.io/badge/Methods and size-2 | 2525 KB-e91e63.svg"/></a>

Get in touch
=
* <a href="https://matrix.to/#/#trifa:matrix.org">Join discussion on Matrix</a><br>
* <a href="https://matrix.to/#/#freenode_#tox:matrix.org">Join Toxuser Channel</a><br>

Compile in Android Studio
=
**Open an existing Project:**<br>
<img src="https://github.com/zoff99/ToxAndroidRefImpl/blob/zoff99/dev003/image.png" width="400">

**and select the "android-refimpl-app" subdir:**<br>
<img src="https://github.com/zoff99/ToxAndroidRefImpl/blob/zoff99/dev003/image1.png" width="400">

<br><br>

Had to make native-audio.jni first. Needed cmake and ninja installed on OS. Then build module. 

Development Snapshot Version (Android)
=
the latest Development Snapshot can be downloaded from CircleCI, [here](https://circleci.com/api/v1/project/zoff99/ToxAndroidRefImpl/latest/artifacts/0/$CIRCLE_ARTIFACTS/ToxAndroidRefImpl.apk?filter=successful&branch=zoff99%2Fdev003)


<img src="https://circleci.com/api/v1/project/zoff99/ToxAndroidRefImpl/latest/artifacts/0/$CIRCLE_ARTIFACTS/capture_app_running_2.png?filter=successful&branch=zoff99%2Fdev003" width="148">


<img src="https://raw.githubusercontent.com/zoff99/ToxAndroidRefImpl/zoff99/dev003/qr_trifa_dev003_apk.png" width="300">
