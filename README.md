[![Build Status](https://travis-ci.org/RocketChat/monitoring.svg?branch=master)](https://travis-ci.org/RocketChat/monitoring)

## [Performance Monitoring for Rocket.Chat](https://kadira.io)

[![Performance Monitoring for Rocket.Chat](https://i.cloudup.com/LwrCCa_RRE.png)](https://rocket.chat)

### Getting started

1. Create an account at <https://kadira.io>
2. From the UI, create an app. You'll get an `AppId` and an `AppSecret`.
3. Run `meteor add rocketchat:monitoring` in your project
4. Configure your Meteor app with the `AppId` and `AppSecret` by adding the following code snippet to a `server/kadira.js` file:

```js
Meteor.startup(function() {
  Kadira.connect('<AppId>', '<AppSecret>');
});
```

Now you can deploy your application and it will send information to Kadira. Wait up to one minute and you'll see data appearing in the Kadira Dashboard.


### Auto Connect

Your app can connect to Kadira using environment variables or using [`Meteor.settings`](http://docs.meteor.com/#meteor_settings).

#### Using Meteor.settings
Use the followng `settings.json` file with your app:

```js
{
  ...
  "kadira": {
    "appId": "<appId>",
    "appSecret": "<appSecret>"
  }
  ...
}
```

The run your app with `meteor --settings=settings.json`.

#### Using Environment Variables

Export the following environment variables before running or deploying your app:

```
export KADIRA_APP_ID=<appId>
export KADIRA_APP_SECRET=<appSecret>
````

### Error Tracking

It comes with built in error tracking solution for Meteor apps. It has been enabled by default.
