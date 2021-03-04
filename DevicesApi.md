# Swagger\Client\DevicesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteDevice**](DevicesApi.md#deletedevice) | **DELETE** /Devices | Deletes a device.
[**getDeviceInfo**](DevicesApi.md#getdeviceinfo) | **GET** /Devices/Info | Get info for a device.
[**getDeviceOptions**](DevicesApi.md#getdeviceoptions) | **GET** /Devices/Options | Get options for a device.
[**getDevices**](DevicesApi.md#getdevices) | **GET** /Devices | Get Devices.
[**updateDeviceOptions**](DevicesApi.md#updatedeviceoptions) | **POST** /Devices/Options | Update device options.

# **deleteDevice**
> deleteDevice($id)

Deletes a device.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DevicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Device Id.

try {
    $apiInstance->deleteDevice($id);
} catch (Exception $e) {
    echo 'Exception when calling DevicesApi->deleteDevice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Device Id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDeviceInfo**
> \Swagger\Client\Model\DeviceInfo getDeviceInfo($id)

Get info for a device.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DevicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Device Id.

try {
    $result = $apiInstance->getDeviceInfo($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DevicesApi->getDeviceInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Device Id. |

### Return type

[**\Swagger\Client\Model\DeviceInfo**](../Model/DeviceInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDeviceOptions**
> \Swagger\Client\Model\DeviceOptions getDeviceOptions($id)

Get options for a device.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DevicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Device Id.

try {
    $result = $apiInstance->getDeviceOptions($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DevicesApi->getDeviceOptions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Device Id. |

### Return type

[**\Swagger\Client\Model\DeviceOptions**](../Model/DeviceOptions.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDevices**
> \Swagger\Client\Model\DeviceInfoQueryResult getDevices($supports_sync, $user_id)

Get Devices.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DevicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supports_sync = true; // bool | Gets or sets a value indicating whether [supports synchronize].
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Gets or sets the user identifier.

try {
    $result = $apiInstance->getDevices($supports_sync, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DevicesApi->getDevices: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supports_sync** | **bool**| Gets or sets a value indicating whether [supports synchronize]. | [optional]
 **user_id** | [**string**](../Model/.md)| Gets or sets the user identifier. | [optional]

### Return type

[**\Swagger\Client\Model\DeviceInfoQueryResult**](../Model/DeviceInfoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateDeviceOptions**
> updateDeviceOptions($body, $id)

Update device options.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DevicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DeviceOptions(); // \Swagger\Client\Model\DeviceOptions | Device Options.
$id = "id_example"; // string | Device Id.

try {
    $apiInstance->updateDeviceOptions($body, $id);
} catch (Exception $e) {
    echo 'Exception when calling DevicesApi->updateDeviceOptions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DeviceOptions**](../Model/DeviceOptions.md)| Device Options. |
 **id** | **string**| Device Id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

