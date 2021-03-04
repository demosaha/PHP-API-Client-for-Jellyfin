# Swagger\Client\DlnaServerApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getConnectionManager**](DlnaServerApi.md#getconnectionmanager) | **GET** /Dlna/{serverId}/ConnectionManager | Gets Dlna media receiver registrar xml.
[**getConnectionManager2**](DlnaServerApi.md#getconnectionmanager2) | **GET** /Dlna/{serverId}/ConnectionManager/ConnectionManager | Gets Dlna media receiver registrar xml.
[**getConnectionManager3**](DlnaServerApi.md#getconnectionmanager3) | **GET** /Dlna/{serverId}/ConnectionManager/ConnectionManager.xml | Gets Dlna media receiver registrar xml.
[**getContentDirectory**](DlnaServerApi.md#getcontentdirectory) | **GET** /Dlna/{serverId}/ContentDirectory | Gets Dlna content directory xml.
[**getContentDirectory2**](DlnaServerApi.md#getcontentdirectory2) | **GET** /Dlna/{serverId}/ContentDirectory/ContentDirectory | Gets Dlna content directory xml.
[**getContentDirectory3**](DlnaServerApi.md#getcontentdirectory3) | **GET** /Dlna/{serverId}/ContentDirectory/ContentDirectory.xml | Gets Dlna content directory xml.
[**getDescriptionXml**](DlnaServerApi.md#getdescriptionxml) | **GET** /Dlna/{serverId}/description | Get Description Xml.
[**getDescriptionXml2**](DlnaServerApi.md#getdescriptionxml2) | **GET** /Dlna/{serverId}/description.xml | Get Description Xml.
[**getIcon**](DlnaServerApi.md#geticon) | **GET** /Dlna/icons/{fileName} | Gets a server icon.
[**getIconId**](DlnaServerApi.md#geticonid) | **GET** /Dlna/{serverId}/icons/{fileName} | Gets a server icon.
[**getMediaReceiverRegistrar**](DlnaServerApi.md#getmediareceiverregistrar) | **GET** /Dlna/{serverId}/MediaReceiverRegistrar | Gets Dlna media receiver registrar xml.
[**getMediaReceiverRegistrar2**](DlnaServerApi.md#getmediareceiverregistrar2) | **GET** /Dlna/{serverId}/MediaReceiverRegistrar/MediaReceiverRegistrar | Gets Dlna media receiver registrar xml.
[**getMediaReceiverRegistrar3**](DlnaServerApi.md#getmediareceiverregistrar3) | **GET** /Dlna/{serverId}/MediaReceiverRegistrar/MediaReceiverRegistrar.xml | Gets Dlna media receiver registrar xml.
[**processConnectionManagerControlRequest**](DlnaServerApi.md#processconnectionmanagercontrolrequest) | **POST** /Dlna/{serverId}/ConnectionManager/Control | Process a connection manager control request.
[**processContentDirectoryControlRequest**](DlnaServerApi.md#processcontentdirectorycontrolrequest) | **POST** /Dlna/{serverId}/ContentDirectory/Control | Process a content directory control request.
[**processMediaReceiverRegistrarControlRequest**](DlnaServerApi.md#processmediareceiverregistrarcontrolrequest) | **POST** /Dlna/{serverId}/MediaReceiverRegistrar/Control | Process a media receiver registrar control request.

# **getConnectionManager**
> string getConnectionManager($server_id)

Gets Dlna media receiver registrar xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getConnectionManager($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getConnectionManager: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConnectionManager2**
> string getConnectionManager2($server_id)

Gets Dlna media receiver registrar xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getConnectionManager2($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getConnectionManager2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConnectionManager3**
> string getConnectionManager3($server_id)

Gets Dlna media receiver registrar xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getConnectionManager3($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getConnectionManager3: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContentDirectory**
> string getContentDirectory($server_id)

Gets Dlna content directory xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getContentDirectory($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getContentDirectory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContentDirectory2**
> string getContentDirectory2($server_id)

Gets Dlna content directory xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getContentDirectory2($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getContentDirectory2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContentDirectory3**
> string getContentDirectory3($server_id)

Gets Dlna content directory xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getContentDirectory3($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getContentDirectory3: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDescriptionXml**
> string getDescriptionXml($server_id)

Get Description Xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getDescriptionXml($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getDescriptionXml: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDescriptionXml2**
> string getDescriptionXml2($server_id)

Get Description Xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getDescriptionXml2($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getDescriptionXml2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getIcon**
> string getIcon($file_name)

Gets a server icon.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$file_name = "file_name_example"; // string | The icon filename.

try {
    $result = $apiInstance->getIcon($file_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getIcon: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_name** | **string**| The icon filename. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getIconId**
> string getIconId($server_id, $file_name)

Gets a server icon.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.
$file_name = "file_name_example"; // string | The icon filename.

try {
    $result = $apiInstance->getIconId($server_id, $file_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getIconId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |
 **file_name** | **string**| The icon filename. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMediaReceiverRegistrar**
> string getMediaReceiverRegistrar($server_id)

Gets Dlna media receiver registrar xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getMediaReceiverRegistrar($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getMediaReceiverRegistrar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMediaReceiverRegistrar2**
> string getMediaReceiverRegistrar2($server_id)

Gets Dlna media receiver registrar xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getMediaReceiverRegistrar2($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getMediaReceiverRegistrar2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMediaReceiverRegistrar3**
> string getMediaReceiverRegistrar3($server_id)

Gets Dlna media receiver registrar xml.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->getMediaReceiverRegistrar3($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->getMediaReceiverRegistrar3: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **processConnectionManagerControlRequest**
> string processConnectionManagerControlRequest($server_id)

Process a connection manager control request.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->processConnectionManagerControlRequest($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->processConnectionManagerControlRequest: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **processContentDirectoryControlRequest**
> string processContentDirectoryControlRequest($server_id)

Process a content directory control request.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->processContentDirectoryControlRequest($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->processContentDirectoryControlRequest: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **processMediaReceiverRegistrarControlRequest**
> string processMediaReceiverRegistrarControlRequest($server_id)

Process a media receiver registrar control request.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DlnaServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$server_id = "server_id_example"; // string | Server UUID.

try {
    $result = $apiInstance->processMediaReceiverRegistrarControlRequest($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DlnaServerApi->processMediaReceiverRegistrarControlRequest: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| Server UUID. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

