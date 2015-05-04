# Twitter Notifier

This Android app notifies about incoming Twitter direct messages.  It makes use of the [GET user](https://dev.twitter.com/streaming/reference/get/user) endpoint provided by Twitter's [User Streams](https://dev.twitter.com/streaming/userstreams) API, so notifications should be pretty much instant as long as there is a network connection.

## Setup and Configuration

First, create a Twitter app (see [here](https://apps.twitter.com/)) that has the following permissions:

* Read
* Write 
* Access direct messages

Then, add a file `app/src/main/res/values/twitter4j.xml` to the project, containing the OAuth credentials from the previously created Twitter app:

```xml
<resources>
    <string name="consumerKey">X</string>
    <string name="consumerSecret">X</string>
    <string name="accessToken">X</string>
    <string name="accessTokenSecret">X</string>
</resources>
```

Assuming that the app has successfully been built and installed, it will start a background service (after a reboot) that displays a notification for each incoming Twitter direct message.
