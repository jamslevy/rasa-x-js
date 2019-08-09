# RasaXHttpApi.NLUDataApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addData**](NLUDataApi.md#addData) | **POST** /projects/{project_id}/data | Add new training example
[**deleteData**](NLUDataApi.md#deleteData) | **DELETE** /projects/{project_id}/data/{example_id} | Delete a training example by id
[**getData**](NLUDataApi.md#getData) | **GET** /projects/{project_id}/data | Get training examples
[**getDataJson**](NLUDataApi.md#getDataJson) | **GET** /projects/{project_id}/data.json | Download traning examples in JSON format
[**getDataWarnings**](NLUDataApi.md#getDataWarnings) | **GET** /projects/{project_id}/dataWarnings | Get warnings about training data.
[**getEntities**](NLUDataApi.md#getEntities) | **GET** /projects/{project_id}/entities | Available entities
[**replaceBulkData**](NLUDataApi.md#replaceBulkData) | **PUT** /projects/{project_id}/data | Replace training data in bulk
[**updateExample**](NLUDataApi.md#updateExample) | **PUT** /projects/{project_id}/data/{example_id} | Update a training example by id
[**updateExampleById**](NLUDataApi.md#updateExampleById) | **PUT** /projects/{project_id}/data/{hash} | Update a training example by id



## addData

> TrainingExample addData(projectId, trainingExample)

Add new training example

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
let trainingExample = new RasaXHttpApi.TrainingExample(); // TrainingExample | 
apiInstance.addData(projectId, trainingExample, (error, data, response) => {
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
 **trainingExample** | [**TrainingExample**](TrainingExample.md)|  | 

### Return type

[**TrainingExample**](TrainingExample.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteData

> InlineResponse2007 deleteData(projectId, exampleId)

Delete a training example by id

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
let exampleId = 5bb89a7f3b18fb3d95495f30; // String | Example ID
apiInstance.deleteData(projectId, exampleId, (error, data, response) => {
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
 **exampleId** | **String**| Example ID | 

### Return type

[**InlineResponse2007**](InlineResponse2007.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getData

> InlineResponse2005 getData(projectId, opts)

Get training examples

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
let opts = {
  'q': "q_example", // String | Search string
  'intent': "intent_example", // String | Intents to filter on
  'limit': 56, // Number | 
  'offset': 0, // Number | 
  'sorted': true // Boolean | 
};
apiInstance.getData(projectId, opts, (error, data, response) => {
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
 **q** | **String**| Search string | [optional] 
 **intent** | **String**| Intents to filter on | [optional] 
 **limit** | **Number**|  | [optional] 
 **offset** | **Number**|  | [optional] [default to 0]
 **sorted** | **Boolean**|  | [optional] 

### Return type

[**InlineResponse2005**](InlineResponse2005.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getDataJson

> Object getDataJson(projectId)

Download traning examples in JSON format

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
apiInstance.getDataJson(projectId, (error, data, response) => {
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

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getDataWarnings

> [DataWarning] getDataWarnings(projectId)

Get warnings about training data.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
apiInstance.getDataWarnings(projectId, (error, data, response) => {
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

[**[DataWarning]**](DataWarning.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEntities

> [Entity] getEntities(projectId)

Available entities

Unique entity types present in the training data.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
apiInstance.getEntities(projectId, (error, data, response) => {
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

[**[Entity]**](Entity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## replaceBulkData

> InlineResponse2006 replaceBulkData(projectId, inlineObject6)

Replace training data in bulk

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
let inlineObject6 = new RasaXHttpApi.InlineObject6(); // InlineObject6 | 
apiInstance.replaceBulkData(projectId, inlineObject6, (error, data, response) => {
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
 **inlineObject6** | [**InlineObject6**](InlineObject6.md)|  | 

### Return type

[**InlineResponse2006**](InlineResponse2006.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, text/markdown
- **Accept**: application/json


## updateExample

> TrainingExample updateExample(projectId, exampleId, trainingExample)

Update a training example by id

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
let exampleId = 5bb89a7f3b18fb3d95495f30; // String | Example ID
let trainingExample = new RasaXHttpApi.TrainingExample(); // TrainingExample | 
apiInstance.updateExample(projectId, exampleId, trainingExample, (error, data, response) => {
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
 **exampleId** | **String**| Example ID | 
 **trainingExample** | [**TrainingExample**](TrainingExample.md)|  | 

### Return type

[**TrainingExample**](TrainingExample.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateExampleById

> TrainingExample updateExampleById(projectId, hash)

Update a training example by id

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.NLUDataApi();
let projectId = default; // String | Project ID
let hash = b10a8db164e0754105b7a99be72e3fe5; // String | MD5 hash of an NLU example's text field
apiInstance.updateExampleById(projectId, hash, (error, data, response) => {
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
 **hash** | **String**| MD5 hash of an NLU example&#39;s text field | 

### Return type

[**TrainingExample**](TrainingExample.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

