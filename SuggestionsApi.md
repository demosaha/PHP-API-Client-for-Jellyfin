# Swagger\Client\SuggestionsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSuggestions**](SuggestionsApi.md#getsuggestions) | **GET** /Users/{userId}/Suggestions | Gets suggestions.

# **getSuggestions**
> \Swagger\Client\Model\BaseItemDtoQueryResult getSuggestions($user_id, $media_type, $type, $start_index, $limit, $enable_total_record_count)

Gets suggestions.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SuggestionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The user id.
$media_type = array("media_type_example"); // string[] | The media types.
$type = array("type_example"); // string[] | The type.
$start_index = 56; // int | Optional. The start index.
$limit = 56; // int | Optional. The limit.
$enable_total_record_count = false; // bool | Whether to enable the total record count.

try {
    $result = $apiInstance->getSuggestions($user_id, $media_type, $type, $start_index, $limit, $enable_total_record_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuggestionsApi->getSuggestions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| The user id. |
 **media_type** | [**string[]**](../Model/string.md)| The media types. | [optional]
 **type** | [**string[]**](../Model/string.md)| The type. | [optional]
 **start_index** | **int**| Optional. The start index. | [optional]
 **limit** | **int**| Optional. The limit. | [optional]
 **enable_total_record_count** | **bool**| Whether to enable the total record count. | [optional] [default to false]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

