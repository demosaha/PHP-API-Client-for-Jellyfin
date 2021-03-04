# Swagger\Client\BrandingApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getBrandingCss**](BrandingApi.md#getbrandingcss) | **GET** /Branding/Css | Gets branding css.
[**getBrandingCss2**](BrandingApi.md#getbrandingcss2) | **GET** /Branding/Css.css | Gets branding css.
[**getBrandingOptions**](BrandingApi.md#getbrandingoptions) | **GET** /Branding/Configuration | Gets branding configuration.

# **getBrandingCss**
> string getBrandingCss()

Gets branding css.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getBrandingCss();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->getBrandingCss: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/css, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBrandingCss2**
> string getBrandingCss2()

Gets branding css.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getBrandingCss2();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->getBrandingCss2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/css, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBrandingOptions**
> \Swagger\Client\Model\BrandingOptions getBrandingOptions()

Gets branding configuration.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BrandingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getBrandingOptions();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandingApi->getBrandingOptions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\BrandingOptions**](../Model/BrandingOptions.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

