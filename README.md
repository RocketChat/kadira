[![Build Status](https://travis-ci.org/RocketChat/monitoring.svg?branch=master)](https://travis-ci.org/RocketChat/monitoring)

## [Performance Monitoring for Rocket.Chat](https://kadira.io)

[![Performance Monitoring for Rocket.Chat](https://i.cloudup.com/LwrCCa_RRE.png)](https://rocket.chat)

### Getting started

1. Create an account at <https://kadira.io>
2. From the UI, create an app. You'll get an `AppId` and an `AppSecret`.
3. Run `meteor add rocketchat:monitoring` in your project
4. Export the following environment variables before running or deploying your app:

```
export KADIRA_APP_ID=<appId>
export KADIRA_APP_SECRET=<appSecret>
```

Now you can deploy your application and it will send information to Kadira. Wait up to one minute and you'll see data appearing in the Kadira Dashboard.

### Error Tracking

It comes with built in error tracking solution for Meteor apps. It has been enabled by default.
