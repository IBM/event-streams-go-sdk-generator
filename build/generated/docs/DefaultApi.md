# \DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateTopic**](DefaultApi.md#CreateTopic) | **Post** /admin/topics | Create a new topic.
[**DeleteTopic**](DefaultApi.md#DeleteTopic) | **Delete** /admin/topics/{topic_name} | Delete a topic.
[**GetTopic**](DefaultApi.md#GetTopic) | **Get** /admin/topics/{topic_name} | Get detailed information on a topic.
[**ListTopics**](DefaultApi.md#ListTopics) | **Get** /admin/topics | Get a list of topics.
[**UpdateTopic**](DefaultApi.md#UpdateTopic) | **Patch** /admin/topics/{topic_name} | Increase the number of partitions and/or update one or more topic configuration parameters. 



## CreateTopic

> map[string]interface{} CreateTopic(ctx, topicCreate)

Create a new topic.

Create a new topic.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**topicCreate** | [**TopicCreateRequest**](TopicCreateRequest.md)| The new topic to be created. | 

### Return type

**map[string]interface{}**

### Authorization

[APIKeyAuth](../README.md#APIKeyAuth), [BasicAuth](../README.md#BasicAuth), [TokenAuth](../README.md#TokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteTopic

> map[string]interface{} DeleteTopic(ctx, topicName)

Delete a topic.

Delete a topic.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**topicName** | **string**| The topic name for the topic to be listed. | 

### Return type

**map[string]interface{}**

### Authorization

[APIKeyAuth](../README.md#APIKeyAuth), [BasicAuth](../README.md#BasicAuth), [TokenAuth](../README.md#TokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTopic

> TopicDetail GetTopic(ctx, topicName)

Get detailed information on a topic.

Get detailed information on a topic.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**topicName** | **string**| The topic name for the topic to be listed. | 

### Return type

[**TopicDetail**](topic_detail.md)

### Authorization

[APIKeyAuth](../README.md#APIKeyAuth), [BasicAuth](../README.md#BasicAuth), [TokenAuth](../README.md#TokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListTopics

> []TopicDetail ListTopics(ctx, optional)

Get a list of topics.

Returns a list containing information about all of the Kafka topics that are defined for an instance of the Event Streams service. If there are currently no topics defined then an empty list is returned. 

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***ListTopicsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a ListTopicsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **topicFilter** | **optional.String**| A filter to be applied to the topic names. A simple filter can be specified as a string with asterisk (&#x60;*&#x60;) wildcards representing 0 or more characters, e.g. &#x60;topic-name*&#x60; will filter all topic names that begin with the string &#x60;topic-name&#x60; followed by any character sequence. A more complex filter pattern can be used by surrounding a regular expression in forward slash (&#x60;/&#x60;) delimiters, e.g. &#x60;/topic-name.* /&#x60;.  | 
 **perPage** | **optional.Int32**| The number of topic names to be returns. | 
 **page** | **optional.Int32**| The page number to be returned. The number 1 represents the first page. The default value is 1.  | 

### Return type

[**[]TopicDetail**](topic_detail.md)

### Authorization

[APIKeyAuth](../README.md#APIKeyAuth), [BasicAuth](../README.md#BasicAuth), [TokenAuth](../README.md#TokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateTopic

> map[string]interface{} UpdateTopic(ctx, topicName, topicUpdate)

Increase the number of partitions and/or update one or more topic configuration parameters. 

Increase the number of partitions and/or update one or more topic configuration parameters. 

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**topicName** | **string**| The topic name for the topic to be listed. | 
**topicUpdate** | [**TopicUpdateRequest**](TopicUpdateRequest.md)| The new partition number or the configurations to be updated for the topic. | 

### Return type

**map[string]interface{}**

### Authorization

[APIKeyAuth](../README.md#APIKeyAuth), [BasicAuth](../README.md#BasicAuth), [TokenAuth](../README.md#TokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

