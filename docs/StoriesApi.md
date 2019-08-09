# RasaXHttpApi.StoriesApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteStory**](StoriesApi.md#deleteStory) | **DELETE** /stories/{story_id} | Delete a Rasa Core Story
[**getStories**](StoriesApi.md#getStories) | **GET** /stories | Get saved stories
[**getStoriesAsMarkdown**](StoriesApi.md#getStoriesAsMarkdown) | **GET** /stories.md | Get stories as markdown file
[**modifyStory**](StoriesApi.md#modifyStory) | **PUT** /stories/{story_id} | Modify Rasa Core story
[**replaceStories**](StoriesApi.md#replaceStories) | **PUT** /stories | Replace stories
[**uploadStories**](StoriesApi.md#uploadStories) | **POST** /stories | Upload stories



## deleteStory

> String deleteStory(storyId)

Delete a Rasa Core Story

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.StoriesApi();
let storyId = 5bb89a7f3b18fb3d95495f31; // String | Story ID
apiInstance.deleteStory(storyId, (error, data, response) => {
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
 **storyId** | **String**| Story ID | 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain, application/json


## getStories

> [RasaCoreStoryObject] getStories(opts)

Get saved stories

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.StoriesApi();
let opts = {
  'q': "q_example" // String | Search string
};
apiInstance.getStories(opts, (error, data, response) => {
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
 **q** | **String**| Search string | [optional] 

### Return type

[**[RasaCoreStoryObject]**](RasaCoreStoryObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getStoriesAsMarkdown

> String getStoriesAsMarkdown(opts)

Get stories as markdown file

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.StoriesApi();
let opts = {
  'q': "q_example" // String | Search string
};
apiInstance.getStoriesAsMarkdown(opts, (error, data, response) => {
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
 **q** | **String**| Search string | [optional] 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/markdown, application/json


## modifyStory

> RasaCoreStoryObject modifyStory(storyId, body)

Modify Rasa Core story

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.StoriesApi();
let storyId = 5bb89a7f3b18fb3d95495f31; // String | Story ID
let body = "body_example"; // String | 
apiInstance.modifyStory(storyId, body, (error, data, response) => {
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
 **storyId** | **String**| Story ID | 
 **body** | **String**|  | 

### Return type

[**RasaCoreStoryObject**](RasaCoreStoryObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: text/markdown
- **Accept**: application/json


## replaceStories

> [RasaCoreStoryObject] replaceStories(body)

Replace stories

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.StoriesApi();
let body = "body_example"; // String | 
apiInstance.replaceStories(body, (error, data, response) => {
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

### Return type

[**[RasaCoreStoryObject]**](RasaCoreStoryObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: text/markdown
- **Accept**: application/json


## uploadStories

> [RasaCoreStoryObject] uploadStories(body)

Upload stories

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.StoriesApi();
let body = "body_example"; // String | 
apiInstance.uploadStories(body, (error, data, response) => {
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

### Return type

[**[RasaCoreStoryObject]**](RasaCoreStoryObject.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: text/markdown
- **Accept**: application/json

