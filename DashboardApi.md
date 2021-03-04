# Swagger\Client\DashboardApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getConfigurationPages**](DashboardApi.md#getconfigurationpages) | **GET** /web/ConfigurationPages | Gets the configuration pages.
[**getDashboardConfigurationPage**](DashboardApi.md#getdashboardconfigurationpage) | **GET** /web/ConfigurationPage | Gets a dashboard configuration page.

# **getConfigurationPages**
> \Swagger\Client\Model\ConfigurationPageInfo[] getConfigurationPages($enable_in_main_menu, $page_type)

Gets the configuration pages.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DashboardApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$enable_in_main_menu = true; // bool | Whether to enable in the main menu.
$page_type = new \Swagger\Client\Model\ConfigurationPageType(); // \Swagger\Client\Model\ConfigurationPageType | The Jellyfin.Api.Models.ConfigurationPageInfo.

try {
    $result = $apiInstance->getConfigurationPages($enable_in_main_menu, $page_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DashboardApi->getConfigurationPages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **enable_in_main_menu** | **bool**| Whether to enable in the main menu. | [optional]
 **page_type** | [**\Swagger\Client\Model\ConfigurationPageType**](../Model/.md)| The Jellyfin.Api.Models.ConfigurationPageInfo. | [optional]

### Return type

[**\Swagger\Client\Model\ConfigurationPageInfo[]**](../Model/ConfigurationPageInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDashboardConfigurationPage**
> string getDashboardConfigurationPage($name)

Gets a dashboard configuration page.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DashboardApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | The name of the page.

try {
    $result = $apiInstance->getDashboardConfigurationPage($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DashboardApi->getDashboardConfigurationPage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| The name of the page. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/html, application/x-javascript, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

