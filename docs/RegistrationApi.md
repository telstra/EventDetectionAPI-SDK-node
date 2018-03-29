# TelstraEventDetection.RegistrationApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**register**](RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
[**unregister**](RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


<a name="register"></a>
# **register**
> ResisterPhoneNumberList register(body)

Register

Register for an event

### Example
```javascript
var TelstraEventDetection = require('Telstra_EventDetection');
var defaultClient = TelstraEventDetection.ApiClient.instance;

// Configure OAuth2 access token for authorization: auth
var auth = defaultClient.authentications['auth'];
auth.accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new TelstraEventDetection.RegistrationApi();

var body = new TelstraEventDetection.SubscriptionObj(); // SubscriptionObj | Subscribe with a list of phone numbers, push notification URL (optional) and the event type.


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.register(body, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SubscriptionObj**](SubscriptionObj.md)| Subscribe with a list of phone numbers, push notification URL (optional) and the event type. | 

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="unregister"></a>
# **unregister**
> ResisterPhoneNumberList unregister(eventType, body)

Unregister

Unregister from an event

### Example
```javascript
var TelstraEventDetection = require('Telstra_EventDetection');
var defaultClient = TelstraEventDetection.ApiClient.instance;

// Configure OAuth2 access token for authorization: auth
var auth = defaultClient.authentications['auth'];
auth.accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new TelstraEventDetection.RegistrationApi();

var eventType = "eventType_example"; // String | Event Type

var body = new TelstraEventDetection.UnregisterRequestObj(); // UnregisterRequestObj | List of subscribed phone numbers and notification URL (optional)


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.unregister(eventType, body, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **eventType** | **String**| Event Type | 
 **body** | [**UnregisterRequestObj**](UnregisterRequestObj.md)| List of subscribed phone numbers and notification URL (optional) | 

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

