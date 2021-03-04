# Swagger\Client\ItemRefreshApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**post**](ItemRefreshApi.md#post) | **POST** /Items/{itemId}/Refresh | Refreshes metadata for an item.

# **post**
> post($item_id, $metadata_refresh_mode, $image_refresh_mode, $replace_all_metadata, $replace_all_images)

Refreshes metadata for an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemRefreshApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$metadata_refresh_mode = new \Swagger\Client\Model\MetadataRefreshMode(); // \Swagger\Client\Model\MetadataRefreshMode | (Optional) Specifies the metadata refresh mode.
$image_refresh_mode = new \Swagger\Client\Model\MetadataRefreshMode(); // \Swagger\Client\Model\MetadataRefreshMode | (Optional) Specifies the image refresh mode.
$replace_all_metadata = false; // bool | (Optional) Determines if metadata should be replaced. Only applicable if mode is FullRefresh.
$replace_all_images = false; // bool | (Optional) Determines if images should be replaced. Only applicable if mode is FullRefresh.

try {
    $apiInstance->post($item_id, $metadata_refresh_mode, $image_refresh_mode, $replace_all_metadata, $replace_all_images);
} catch (Exception $e) {
    echo 'Exception when calling ItemRefreshApi->post: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **metadata_refresh_mode** | [**\Swagger\Client\Model\MetadataRefreshMode**](../Model/.md)| (Optional) Specifies the metadata refresh mode. | [optional]
 **image_refresh_mode** | [**\Swagger\Client\Model\MetadataRefreshMode**](../Model/.md)| (Optional) Specifies the image refresh mode. | [optional]
 **replace_all_metadata** | **bool**| (Optional) Determines if metadata should be replaced. Only applicable if mode is FullRefresh. | [optional] [default to false]
 **replace_all_images** | **bool**| (Optional) Determines if images should be replaced. Only applicable if mode is FullRefresh. | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

