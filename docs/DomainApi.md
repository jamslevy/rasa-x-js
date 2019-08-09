# RasaXHttpApi.DomainApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAction**](DomainApi.md#createAction) | **POST** /projects/{project_id}/actions | Create new action
[**deleteAction**](DomainApi.md#deleteAction) | **DELETE** /projects/{project_id}/actions/{action_id} | Delete action
[**getDomain**](DomainApi.md#getDomain) | **GET** /domain | Retrieve Rasa domain
[**getDomainActions**](DomainApi.md#getDomainActions) | **GET** /projects/{project_id}/actions | Retrieve Rasa domain actions
[**getDomainWarnings**](DomainApi.md#getDomainWarnings) | **GET** /domainWarnings | Retrieve Rasa domain warnings
[**updateAction**](DomainApi.md#updateAction) | **PUT** /projects/{project_id}/actions/{action_id} | Update action
[**updateDomain**](DomainApi.md#updateDomain) | **PUT** /domain | Update Rasa domain



## createAction

> Action createAction(projectId, action)

Create new action

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.DomainApi();
let projectId = default; // String | Project ID
let action = new RasaXHttpApi.Action(); // Action | 
apiInstance.createAction(projectId, action, (error, data, response) => {
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
 **projectId** | **String**| Project ID | 
 **action** | [**Action**](Action.md)|  | 

### Return type

[**Action**](Action.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteAction

> deleteAction(projectId, actionId)

Delete action

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.DomainApi();
let projectId = default; // String | Project ID
let actionId = "actionId_example"; // String | Unique id of an action
apiInstance.deleteAction(projectId, actionId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectId** | **String**| Project ID | 
 **actionId** | **String**| Unique id of an action | 

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getDomain

> String getDomain()

Retrieve Rasa domain

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.DomainApi();
apiInstance.getDomain((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain, application/json


## getDomainActions

> [String] getDomainActions(projectId)

Retrieve Rasa domain actions

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.DomainApi();
let projectId = default; // String | Project ID
apiInstance.getDomainActions(projectId, (error, data, response) => {
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
 **projectId** | **String**| Project ID | 

### Return type

**[String]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getDomainWarnings

> DomainWarnings getDomainWarnings()

Retrieve Rasa domain warnings

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.DomainApi();
apiInstance.getDomainWarnings((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**DomainWarnings**](DomainWarnings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateAction

> Action updateAction(projectId, actionId, action)

Update action

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.DomainApi();
let projectId = default; // String | Project ID
let actionId = "actionId_example"; // String | Unique id of an action
let action = new RasaXHttpApi.Action(); // Action | 
apiInstance.updateAction(projectId, actionId, action, (error, data, response) => {
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
 **projectId** | **String**| Project ID | 
 **actionId** | **String**| Unique id of an action | 
 **action** | [**Action**](Action.md)|  | 

### Return type

[**Action**](Action.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateDomain

> String updateDomain(body, opts)

Update Rasa domain

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.DomainApi();
let body = "body_example"; // String | 
let opts = {
  'storeTemplates': false // Boolean | Specifies whether to store the templates from the uploaded domain.
};
apiInstance.updateDomain(body, opts, (error, data, response) => {
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
 **body** | **String**|  | 
 **storeTemplates** | **Boolean**| Specifies whether to store the templates from the uploaded domain. | [optional] [default to false]

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: text/plain
- **Accept**: text/plain, application/json

