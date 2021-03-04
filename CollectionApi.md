# Swagger\Client\CollectionApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addToCollection**](CollectionApi.md#addtocollection) | **POST** /Collections/{collectionId}/Items | Adds items to a collection.
[**createCollection**](CollectionApi.md#createcollection) | **POST** /Collections | Creates a new collection.
[**removeFromCollection**](CollectionApi.md#removefromcollection) | **DELETE** /Collections/{collectionId}/Items | Removes items from a collection.

# **addToCollection**
> addToCollection($collection_id, $ids)

Adds items to a collection.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$collection_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The collection id.
$ids = array("ids_example"); // string[] | Item ids, comma delimited.

try {
    $apiInstance->addToCollection($collection_id, $ids);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->addToCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | [**string**](../Model/.md)| The collection id. |
 **ids** | [**string[]**](../Model/string.md)| Item ids, comma delimited. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createCollection**
> \Swagger\Client\Model\CollectionCreationResult createCollection($name, $ids, $parent_id, $is_locked)

Creates a new collection.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | The name of the collection.
$ids = array("ids_example"); // string[] | Item Ids to add to the collection.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Create the collection within a specific folder.
$is_locked = false; // bool | Whether or not to lock the new collection.

try {
    $result = $apiInstance->createCollection($name, $ids, $parent_id, $is_locked);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->createCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| The name of the collection. | [optional]
 **ids** | [**string[]**](../Model/string.md)| Item Ids to add to the collection. | [optional]
 **parent_id** | [**string**](../Model/.md)| Optional. Create the collection within a specific folder. | [optional]
 **is_locked** | **bool**| Whether or not to lock the new collection. | [optional] [default to false]

### Return type

[**\Swagger\Client\Model\CollectionCreationResult**](../Model/CollectionCreationResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeFromCollection**
> removeFromCollection($collection_id, $ids)

Removes items from a collection.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\CollectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$collection_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The collection id.
$ids = array("ids_example"); // string[] | Item ids, comma delimited.

try {
    $apiInstance->removeFromCollection($collection_id, $ids);
} catch (Exception $e) {
    echo 'Exception when calling CollectionApi->removeFromCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_id** | [**string**](../Model/.md)| The collection id. |
 **ids** | [**string[]**](../Model/string.md)| Item ids, comma delimited. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

