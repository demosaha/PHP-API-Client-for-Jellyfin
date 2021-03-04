# Swagger\Client\ChannelsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAllChannelFeatures**](ChannelsApi.md#getallchannelfeatures) | **GET** /Channels/Features | Get all channel features.
[**getChannelFeatures**](ChannelsApi.md#getchannelfeatures) | **GET** /Channels/{channelId}/Features | Get channel features.
[**getChannelItems**](ChannelsApi.md#getchannelitems) | **GET** /Channels/{channelId}/Items | Get channel items.
[**getChannels**](ChannelsApi.md#getchannels) | **GET** /Channels | Gets available channels.
[**getLatestChannelItems**](ChannelsApi.md#getlatestchannelitems) | **GET** /Channels/Items/Latest | Gets latest channel items.

# **getAllChannelFeatures**
> \Swagger\Client\Model\ChannelFeatures[] getAllChannelFeatures()

Get all channel features.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllChannelFeatures();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->getAllChannelFeatures: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ChannelFeatures[]**](../Model/ChannelFeatures.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChannelFeatures**
> \Swagger\Client\Model\ChannelFeatures getChannelFeatures($channel_id)

Get channel features.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Channel id.

try {
    $result = $apiInstance->getChannelFeatures($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->getChannelFeatures: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | [**string**](../Model/.md)| Channel id. |

### Return type

[**\Swagger\Client\Model\ChannelFeatures**](../Model/ChannelFeatures.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChannelItems**
> \Swagger\Client\Model\BaseItemDtoQueryResult getChannelItems($channel_id, $folder_id, $user_id, $start_index, $limit, $sort_order, $filters, $sort_by, $fields)

Get channel items.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Channel Id.
$folder_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Folder Id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. User Id.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$sort_order = "sort_order_example"; // string | Optional. Sort Order - Ascending,Descending.
$filters = array(new \Swagger\Client\Model\ItemFilter()); // \Swagger\Client\Model\ItemFilter[] | Optional. Specify additional filters to apply.
$sort_by = "sort_by_example"; // string | Optional. Specify one or more sort orders, comma delimited. Options: Album, AlbumArtist, Artist, Budget, CommunityRating, CriticRating, DateCreated, DatePlayed, PlayCount, PremiereDate, ProductionYear, SortName, Random, Revenue, Runtime.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.

try {
    $result = $apiInstance->getChannelItems($channel_id, $folder_id, $user_id, $start_index, $limit, $sort_order, $filters, $sort_by, $fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->getChannelItems: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | [**string**](../Model/.md)| Channel Id. |
 **folder_id** | [**string**](../Model/.md)| Optional. Folder Id. | [optional]
 **user_id** | [**string**](../Model/.md)| Optional. User Id. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **sort_order** | **string**| Optional. Sort Order - Ascending,Descending. | [optional]
 **filters** | [**\Swagger\Client\Model\ItemFilter[]**](../Model/\Swagger\Client\Model\ItemFilter.md)| Optional. Specify additional filters to apply. | [optional]
 **sort_by** | **string**| Optional. Specify one or more sort orders, comma delimited. Options: Album, AlbumArtist, Artist, Budget, CommunityRating, CriticRating, DateCreated, DatePlayed, PlayCount, PremiereDate, ProductionYear, SortName, Random, Revenue, Runtime. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChannels**
> \Swagger\Client\Model\BaseItemDtoQueryResult getChannels($user_id, $start_index, $limit, $supports_latest_items, $supports_media_deletion, $is_favorite)

Gets available channels.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User Id to filter by. Use System.Guid.Empty to not filter by user.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$supports_latest_items = true; // bool | Optional. Filter by channels that support getting latest items.
$supports_media_deletion = true; // bool | Optional. Filter by channels that support media deletion.
$is_favorite = true; // bool | Optional. Filter by channels that are favorite.

try {
    $result = $apiInstance->getChannels($user_id, $start_index, $limit, $supports_latest_items, $supports_media_deletion, $is_favorite);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->getChannels: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User Id to filter by. Use System.Guid.Empty to not filter by user. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **supports_latest_items** | **bool**| Optional. Filter by channels that support getting latest items. | [optional]
 **supports_media_deletion** | **bool**| Optional. Filter by channels that support media deletion. | [optional]
 **is_favorite** | **bool**| Optional. Filter by channels that are favorite. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLatestChannelItems**
> \Swagger\Client\Model\BaseItemDtoQueryResult getLatestChannelItems($user_id, $start_index, $limit, $filters, $fields, $channel_ids)

Gets latest channel items.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. User Id.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$filters = array(new \Swagger\Client\Model\ItemFilter()); // \Swagger\Client\Model\ItemFilter[] | Optional. Specify additional filters to apply.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$channel_ids = array("channel_ids_example"); // string[] | Optional. Specify one or more channel id's, comma delimited.

try {
    $result = $apiInstance->getLatestChannelItems($user_id, $start_index, $limit, $filters, $fields, $channel_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->getLatestChannelItems: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| Optional. User Id. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **filters** | [**\Swagger\Client\Model\ItemFilter[]**](../Model/\Swagger\Client\Model\ItemFilter.md)| Optional. Specify additional filters to apply. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **channel_ids** | [**string[]**](../Model/string.md)| Optional. Specify one or more channel id&#x27;s, comma delimited. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

