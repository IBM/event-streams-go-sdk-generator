# TopicCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | The name of topic to be created. | [optional] 
**Partitions** | **int64** | The number of partitions. | [optional] 
**PartitionCount** | **int64** | The number of partitions, this field takes precedence over &#39;partitions&#39;. Default value is 1 if not specified. | [optional] [default to 1]
**Configs** | [**[]ConfigCreate**](config_create.md) | The config properties to be set for the new topic. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


