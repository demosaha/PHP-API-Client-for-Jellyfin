# Swagger\Client\EnvironmentApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getDefaultDirectoryBrowser**](EnvironmentApi.md#getdefaultdirectorybrowser) | **GET** /Environment/DefaultDirectoryBrowser | Get Default directory browser.
[**getDirectoryContents**](EnvironmentApi.md#getdirectorycontents) | **GET** /Environment/DirectoryContents | Gets the contents of a given directory in the file system.
[**getDrives**](EnvironmentApi.md#getdrives) | **GET** /Environment/Drives | Gets available drives from the server&#x27;s file system.
[**getNetworkShares**](EnvironmentApi.md#getnetworkshares) | **GET** /Environment/NetworkShares | Gets network paths.
[**getParentPath**](EnvironmentApi.md#getparentpath) | **GET** /Environment/ParentPath | Gets the parent path of a given path.
[**validatePath**](EnvironmentApi.md#validatepath) | **POST** /Environment/ValidatePath | Validates path.

# **getDefaultDirectoryBrowser**
> \Swagger\Client\Model\DefaultDirectoryBrowserInfoDto getDefaultDirectoryBrowser()

Get Default directory browser.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\EnvironmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getDefaultDirectoryBrowser();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentApi->getDefaultDirectoryBrowser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\DefaultDirectoryBrowserInfoDto**](../Model/DefaultDirectoryBrowserInfoDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDirectoryContents**
> \Swagger\Client\Model\FileSystemEntryInfo[] getDirectoryContents($path, $include_files, $include_directories)

Gets the contents of a given directory in the file system.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\EnvironmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$path = "path_example"; // string | The path.
$include_files = false; // bool | An optional filter to include or exclude files from the results. true/false.
$include_directories = false; // bool | An optional filter to include or exclude folders from the results. true/false.

try {
    $result = $apiInstance->getDirectoryContents($path, $include_files, $include_directories);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentApi->getDirectoryContents: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **path** | **string**| The path. |
 **include_files** | **bool**| An optional filter to include or exclude files from the results. true/false. | [optional] [default to false]
 **include_directories** | **bool**| An optional filter to include or exclude folders from the results. true/false. | [optional] [default to false]

### Return type

[**\Swagger\Client\Model\FileSystemEntryInfo[]**](../Model/FileSystemEntryInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDrives**
> \Swagger\Client\Model\FileSystemEntryInfo[] getDrives()

Gets available drives from the server's file system.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\EnvironmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getDrives();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentApi->getDrives: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\FileSystemEntryInfo[]**](../Model/FileSystemEntryInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getNetworkShares**
> \Swagger\Client\Model\FileSystemEntryInfo[] getNetworkShares()

Gets network paths.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\EnvironmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getNetworkShares();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentApi->getNetworkShares: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\FileSystemEntryInfo[]**](../Model/FileSystemEntryInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getParentPath**
> string getParentPath($path)

Gets the parent path of a given path.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\EnvironmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$path = "path_example"; // string | The path.

try {
    $result = $apiInstance->getParentPath($path);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentApi->getParentPath: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **path** | **string**| The path. |

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **validatePath**
> validatePath($body)

Validates path.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\EnvironmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ValidatePathDto(); // \Swagger\Client\Model\ValidatePathDto | Validate request object.

try {
    $apiInstance->validatePath($body);
} catch (Exception $e) {
    echo 'Exception when calling EnvironmentApi->validatePath: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ValidatePathDto**](../Model/ValidatePathDto.md)| Validate request object. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

