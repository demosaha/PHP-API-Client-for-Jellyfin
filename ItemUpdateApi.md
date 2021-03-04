# Swagger\Client\ItemUpdateApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMetadataEditorInfo**](ItemUpdateApi.md#getmetadataeditorinfo) | **GET** /Items/{itemId}/MetadataEditor | Gets metadata editor info for an item.
[**updateItem**](ItemUpdateApi.md#updateitem) | **POST** /Items/{itemId} | Updates an item.
[**updateItemContentType**](ItemUpdateApi.md#updateitemcontenttype) | **POST** /Items/{itemId}/ContentType | Updates an item&#x27;s content type.

# **getMetadataEditorInfo**
> \Swagger\Client\Model\MetadataEditorInfo getMetadataEditorInfo($item_id)

Gets metadata editor info for an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.

try {
    $result = $apiInstance->getMetadataEditorInfo($item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemUpdateApi->getMetadataEditorInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |

### Return type

[**\Swagger\Client\Model\MetadataEditorInfo**](../Model/MetadataEditorInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateItem**
> updateItem($body, $item_id)

Updates an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\BaseItemDto(); // \Swagger\Client\Model\BaseItemDto | The new item properties.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.

try {
    $apiInstance->updateItem($body, $item_id);
} catch (Exception $e) {
    echo 'Exception when calling ItemUpdateApi->updateItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)| The new item properties. |
 **item_id** | [**string**](../Model/.md)| The item id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateItemContentType**
> updateItemContentType($item_id, $content_type)

Updates an item's content type.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$content_type = "content_type_example"; // string | The content type of the item.

try {
    $apiInstance->updateItemContentType($item_id, $content_type);
} catch (Exception $e) {
    echo 'Exception when calling ItemUpdateApi->updateItemContentType: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **content_type** | **string**| The content type of the item. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

