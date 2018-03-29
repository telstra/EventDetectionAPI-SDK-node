# TelstraEventDetection.PushNotificationsApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pushNotifications**](PushNotificationsApi.md#pushNotifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications


<a name="pushNotifications"></a>
# **pushNotifications**
> PushNotificationObj pushNotifications(contentType, body)

Push event notifications

Push event notifications to the notification URL configured during the MSISDN registration process

### Example
```javascript
var TelstraEventDetection = require('Telstra_EventDetection');

var apiInstance = new TelstraEventDetection.PushNotificationsApi();

var contentType = "contentType_example"; // String | application/json

var body = new TelstraEventDetection.NotificationPayload(); // NotificationPayload | Application Id, MSISDN, Event Id and Event Date


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.pushNotifications(contentType, body, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contentType** | **String**| application/json | 
 **body** | [**NotificationPayload**](NotificationPayload.md)| Application Id, MSISDN, Event Id and Event Date | 

### Return type

[**PushNotificationObj**](PushNotificationObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

