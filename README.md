# Telstra_EventDetection

TelstraEventDetection - JavaScript client for Telstra_EventDetection

- API version: 1.0.0
- Package version: 1.0.0

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),

Then install it via:

```shell
npm install Telstra_EventDetection --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your Telstra_EventDetection from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('Telstra_EventDetection')` in javascript files from the directory you ran the last 
command above from.

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/Telstra/EventDetectionAPI-SDK-node
then install it via:

```shell
    npm install Telstra/EventDetectionAPI-SDK-node --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var TelstraEventDetection = require('Telstra_EventDetection');

var api = new TelstraEventDetection.AuthenticationApi()

var clientId = "clientId_example"; // {String} 

var clientSecret = "clientSecret_example"; // {String} 

var grantType = "client_credentials"; // {String} 


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.authToken(clientId, clientSecret, grantType, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://tapi.telstra.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*TelstraEventDetection.AuthenticationApi* | [**authToken**](docs/AuthenticationApi.md#authToken) | **POST** /v2/oauth/token | Generate authentication token
*TelstraEventDetection.GetSubscriptionApi* | [**getSubscription**](docs/GetSubscriptionApi.md#getSubscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions
*TelstraEventDetection.LongPollApi* | [**longpoll**](docs/LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events
*TelstraEventDetection.PushNotificationsApi* | [**pushNotifications**](docs/PushNotificationsApi.md#pushNotifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications
*TelstraEventDetection.RegistrationApi* | [**register**](docs/RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
*TelstraEventDetection.RegistrationApi* | [**unregister**](docs/RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


## Documentation for Models

 - [TelstraEventDetection.Eventsattr](docs/Eventsattr.md)
 - [TelstraEventDetection.GetEventResponse](docs/GetEventResponse.md)
 - [TelstraEventDetection.GetSubscriptionResponse](docs/GetSubscriptionResponse.md)
 - [TelstraEventDetection.NotificationPayload](docs/NotificationPayload.md)
 - [TelstraEventDetection.OAuthResponse](docs/OAuthResponse.md)
 - [TelstraEventDetection.PhoneNumberList](docs/PhoneNumberList.md)
 - [TelstraEventDetection.PollingObj](docs/PollingObj.md)
 - [TelstraEventDetection.PushNotificationObj](docs/PushNotificationObj.md)
 - [TelstraEventDetection.ResisterPhoneNumberList](docs/ResisterPhoneNumberList.md)
 - [TelstraEventDetection.ServiceEventsAttr](docs/ServiceEventsAttr.md)
 - [TelstraEventDetection.SubscriptionObj](docs/SubscriptionObj.md)
 - [TelstraEventDetection.Subscriptionattr](docs/Subscriptionattr.md)
 - [TelstraEventDetection.Test](docs/Test.md)
 - [TelstraEventDetection.UnregisterRequestObj](docs/UnregisterRequestObj.md)


## Documentation for Authorisation


### auth

- **Type**: OAuth
- **Flow**: application
- **Authorisation URL**: 
- **Scopes**: 
  - v1_eventdetection_simswap: v1_eventdetection_simswap

