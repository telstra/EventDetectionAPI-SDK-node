# TelstraEventDetection.AuthenticationApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authToken**](AuthenticationApi.md#authToken) | **POST** /v2/oauth/token | Generate authentication token


<a name="authToken"></a>
# **authToken**
> OAuthResponse authToken(clientId, clientSecret, grantType)

Generate authentication token

Generate authentication token

### Example
```javascript
var TelstraEventDetection = require('Telstra_EventDetection');

var apiInstance = new TelstraEventDetection.AuthenticationApi();

var clientId = "clientId_example"; // String | 

var clientSecret = "clientSecret_example"; // String | 

var grantType = "client_credentials"; // String | 


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.authToken(clientId, clientSecret, grantType, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **clientId** | **String**|  | 
 **clientSecret** | **String**|  | 
 **grantType** | **String**|  | [default to client_credentials]

### Return type

[**OAuthResponse**](OAuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

