# Swagger\Client\DisplayPreferencesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getDisplayPreferences**](DisplayPreferencesApi.md#getdisplaypreferences) | **GET** /DisplayPreferences/{displayPreferencesId} | Get Display Preferences.
[**updateDisplayPreferences**](DisplayPreferencesApi.md#updatedisplaypreferences) | **POST** /DisplayPreferences/{displayPreferencesId} | Update Display Preferences.

# **getDisplayPreferences**
> \Swagger\Client\Model\DisplayPreferencesDto getDisplayPreferences($display_preferences_id, $user_id, $client)

Get Display Preferences.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DisplayPreferencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$display_preferences_id = "display_preferences_id_example"; // string | Display preferences id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$client = "client_example"; // string | Client.

try {
    $result = $apiInstance->getDisplayPreferences($display_preferences_id, $user_id, $client);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DisplayPreferencesApi->getDisplayPreferences: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **display_preferences_id** | **string**| Display preferences id. |
 **user_id** | [**string**](../Model/.md)| User id. |
 **client** | **string**| Client. |

### Return type

[**\Swagger\Client\Model\DisplayPreferencesDto**](../Model/DisplayPreferencesDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateDisplayPreferences**
> updateDisplayPreferences($body, $user_id, $client, $display_preferences_id)

Update Display Preferences.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DisplayPreferencesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DisplayPreferencesDto(); // \Swagger\Client\Model\DisplayPreferencesDto | New Display Preferences object.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User Id.
$client = "client_example"; // string | Client.
$display_preferences_id = "display_preferences_id_example"; // string | Display preferences id.

try {
    $apiInstance->updateDisplayPreferences($body, $user_id, $client, $display_preferences_id);
} catch (Exception $e) {
    echo 'Exception when calling DisplayPreferencesApi->updateDisplayPreferences: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DisplayPreferencesDto**](../Model/DisplayPreferencesDto.md)| New Display Preferences object. |
 **user_id** | [**string**](../Model/.md)| User Id. |
 **client** | **string**| Client. |
 **display_preferences_id** | **string**| Display preferences id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

