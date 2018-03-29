# TelstraEventDetection.GetSubscriptionApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSubscription**](GetSubscriptionApi.md#getSubscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions


<a name="getSubscription"></a>
# **getSubscription**
> GetSubscriptionResponse getSubscription(body)

Get Event Subscriptions

Get the list of events subscribed for

### Example
```javascript
var TelstraEventDetection = require('Telstra_EventDetection');
var defaultClient = TelstraEventDetection.ApiClient.instance;

// Configure OAuth2 access token for authorization: auth
var auth = defaultClient.authentications['auth'];
auth.accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new TelstraEventDetection.GetSubscriptionApi();

var body = new TelstraEventDetection.PhoneNumberList(); // PhoneNumberList | List of subscribed phone numbers


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.getSubscription(body, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhoneNumberList**](PhoneNumberList.md)| List of subscribed phone numbers | 

### Return type

[**GetSubscriptionResponse**](GetSubscriptionResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

