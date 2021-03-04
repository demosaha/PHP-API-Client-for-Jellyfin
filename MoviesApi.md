# Swagger\Client\MoviesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMovieRecommendations**](MoviesApi.md#getmovierecommendations) | **GET** /Movies/Recommendations | Gets movie recommendations.

# **getMovieRecommendations**
> \Swagger\Client\Model\RecommendationDto[] getMovieRecommendations($user_id, $parent_id, $fields, $category_limit, $item_limit)

Gets movie recommendations.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MoviesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Specify this to localize the search to a specific item or folder. Omit to use the root.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. The fields to return.
$category_limit = 5; // int | The max number of categories to return.
$item_limit = 8; // int | The max number of items to return per category.

try {
    $result = $apiInstance->getMovieRecommendations($user_id, $parent_id, $fields, $category_limit, $item_limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MoviesApi->getMovieRecommendations: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
 **parent_id** | [**string**](../Model/.md)| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. The fields to return. | [optional]
 **category_limit** | **int**| The max number of categories to return. | [optional] [default to 5]
 **item_limit** | **int**| The max number of items to return per category. | [optional] [default to 8]

### Return type

[**\Swagger\Client\Model\RecommendationDto[]**](../Model/RecommendationDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

