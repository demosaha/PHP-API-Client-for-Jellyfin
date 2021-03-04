# Swagger\Client\YearsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getYear**](YearsApi.md#getyear) | **GET** /Years/{year} | Gets a year.
[**getYears**](YearsApi.md#getyears) | **GET** /Years | Get years.

# **getYear**
> \Swagger\Client\Model\BaseItemDto getYear($year, $user_id)

Gets a year.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\YearsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int | The year.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.

try {
    $result = $apiInstance->getYear($year, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YearsApi->getYear: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**| The year. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getYears**
> \Swagger\Client\Model\BaseItemDtoQueryResult getYears($start_index, $limit, $sort_order, $parent_id, $fields, $exclude_item_types, $include_item_types, $media_types, $sort_by, $enable_user_data, $image_type_limit, $enable_image_types, $user_id, $recursive, $enable_images)

Get years.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\YearsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_index = 56; // int | Skips over a given number of items within the results. Use for paging.
$limit = 56; // int | Optional. The maximum number of records to return.
$sort_order = "sort_order_example"; // string | Sort Order - Ascending,Descending.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Specify this to localize the search to a specific item or folder. Omit to use the root.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$exclude_item_types = array("exclude_item_types_example"); // string[] | Optional. If specified, results will be excluded based on item type. This allows multiple, comma delimited.
$include_item_types = array("include_item_types_example"); // string[] | Optional. If specified, results will be included based on item type. This allows multiple, comma delimited.
$media_types = array("media_types_example"); // string[] | Optional. Filter by MediaType. Allows multiple, comma delimited.
$sort_by = "sort_by_example"; // string | Optional. Specify one or more sort orders, comma delimited. Options: Album, AlbumArtist, Artist, Budget, CommunityRating, CriticRating, DateCreated, DatePlayed, PlayCount, PremiereDate, ProductionYear, SortName, Random, Revenue, Runtime.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User Id.
$recursive = true; // bool | Search recursively.
$enable_images = true; // bool | Optional. Include image information in output.

try {
    $result = $apiInstance->getYears($start_index, $limit, $sort_order, $parent_id, $fields, $exclude_item_types, $include_item_types, $media_types, $sort_by, $enable_user_data, $image_type_limit, $enable_image_types, $user_id, $recursive, $enable_images);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling YearsApi->getYears: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_index** | **int**| Skips over a given number of items within the results. Use for paging. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **sort_order** | **string**| Sort Order - Ascending,Descending. | [optional]
 **parent_id** | [**string**](../Model/.md)| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **exclude_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be excluded based on item type. This allows multiple, comma delimited. | [optional]
 **include_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be included based on item type. This allows multiple, comma delimited. | [optional]
 **media_types** | [**string[]**](../Model/string.md)| Optional. Filter by MediaType. Allows multiple, comma delimited. | [optional]
 **sort_by** | **string**| Optional. Specify one or more sort orders, comma delimited. Options: Album, AlbumArtist, Artist, Budget, CommunityRating, CriticRating, DateCreated, DatePlayed, PlayCount, PremiereDate, ProductionYear, SortName, Random, Revenue, Runtime. | [optional]
 **enable_user_data** | **bool**| Optional. Include user data. | [optional]
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **user_id** | [**string**](../Model/.md)| User Id. | [optional]
 **recursive** | **bool**| Search recursively. | [optional] [default to true]
 **enable_images** | **bool**| Optional. Include image information in output. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

