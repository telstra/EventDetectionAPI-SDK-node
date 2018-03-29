# TelstraEventDetection.LongPollApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**longpoll**](LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events


<a name="longpoll"></a>
# **longpoll**
> GetEventResponse longpoll(eventType, body)

Poll events

Poll events for a given set of MSISDNs

### Example
```javascript
var TelstraEventDetection = require('Telstra_EventDetection');
var defaultClient = TelstraEventDetection.ApiClient.instance;

// Configure OAuth2 access token for authorization: auth
var auth = defaultClient.authentications['auth'];
auth.accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new TelstraEventDetection.LongPollApi();

var eventType = "eventType_example"; // String | Event Type

var body = new TelstraEventDetection.PollingObj(); // PollingObj | List of MSISDNs to pull the events


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.longpoll(eventType, body, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **eventType** | **String**| Event Type | 
 **body** | [**PollingObj**](PollingObj.md)| List of MSISDNs to pull the events | 

### Return type

[**GetEventResponse**](GetEventResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

