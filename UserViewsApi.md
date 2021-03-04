# Swagger\Client\UserViewsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getGroupingOptions**](UserViewsApi.md#getgroupingoptions) | **GET** /Users/{userId}/GroupingOptions | Get user view grouping options.
[**getUserViews**](UserViewsApi.md#getuserviews) | **GET** /Users/{userId}/Views | Get user views.

# **getGroupingOptions**
> \Swagger\Client\Model\SpecialViewOptionDto[] getGroupingOptions($user_id)

Get user view grouping options.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserViewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.

try {
    $result = $apiInstance->getGroupingOptions($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserViewsApi->getGroupingOptions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |

### Return type

[**\Swagger\Client\Model\SpecialViewOptionDto[]**](../Model/SpecialViewOptionDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserViews**
> \Swagger\Client\Model\BaseItemDtoQueryResult getUserViews($user_id, $include_external_content, $preset_views, $include_hidden)

Get user views.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserViewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$include_external_content = true; // bool | Whether or not to include external views such as channels or live tv.
$preset_views = array("preset_views_example"); // string[] | Preset views.
$include_hidden = false; // bool | Whether or not to include hidden content.

try {
    $result = $apiInstance->getUserViews($user_id, $include_external_content, $preset_views, $include_hidden);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserViewsApi->getUserViews: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **include_external_content** | **bool**| Whether or not to include external views such as channels or live tv. | [optional]
 **preset_views** | [**string[]**](../Model/string.md)| Preset views. | [optional]
 **include_hidden** | **bool**| Whether or not to include hidden content. | [optional] [default to false]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

