# RasaXHttpApi.UserApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**changePassword**](UserApi.md#changePassword) | **POST** /user/password | Change password
[**deleteUser**](UserApi.md#deleteUser) | **DELETE** /users/{username} | Delete a user
[**updateUsername**](UserApi.md#updateUsername) | **PATCH** /user | Update username



## changePassword

> User changePassword(inlineObject3)

Change password

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.UserApi();
let inlineObject3 = new RasaXHttpApi.InlineObject3(); // InlineObject3 | 
apiInstance.changePassword(inlineObject3, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inlineObject3** | [**InlineObject3**](InlineObject3.md)|  | 

### Return type

[**User**](User.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteUser

> OneOfUserobject deleteUser(username)

Delete a user

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.UserApi();
let username = "username_example"; // String | 
apiInstance.deleteUser(username, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **String**|  | 

### Return type

[**OneOfUserobject**](OneOfUserobject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateUsername

> User updateUsername(inlineObject2)

Update username

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.UserApi();
let inlineObject2 = new RasaXHttpApi.InlineObject2(); // InlineObject2 | 
apiInstance.updateUsername(inlineObject2, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inlineObject2** | [**InlineObject2**](InlineObject2.md)|  | 

### Return type

[**User**](User.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

