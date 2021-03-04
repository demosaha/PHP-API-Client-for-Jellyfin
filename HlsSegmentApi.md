# Swagger\Client\HlsSegmentApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getHlsAudioSegmentLegacyAac**](HlsSegmentApi.md#gethlsaudiosegmentlegacyaac) | **GET** /Audio/{itemId}/hls/{segmentId}/stream.aac | Gets the specified audio segment for an audio item.
[**getHlsAudioSegmentLegacyMp3**](HlsSegmentApi.md#gethlsaudiosegmentlegacymp3) | **GET** /Audio/{itemId}/hls/{segmentId}/stream.mp3 | Gets the specified audio segment for an audio item.
[**getHlsPlaylistLegacy**](HlsSegmentApi.md#gethlsplaylistlegacy) | **GET** /Videos/{itemId}/hls/{playlistId}/stream.m3u8 | Gets a hls video playlist.
[**getHlsVideoSegmentLegacy**](HlsSegmentApi.md#gethlsvideosegmentlegacy) | **GET** /Videos/{itemId}/hls/{playlistId}/{segmentId}.{segmentContainer} | Gets a hls video segment.
[**stopEncodingProcess**](HlsSegmentApi.md#stopencodingprocess) | **DELETE** /Videos/ActiveEncodings | Stops an active encoding.

# **getHlsAudioSegmentLegacyAac**
> string getHlsAudioSegmentLegacyAac($item_id, $segment_id)

Gets the specified audio segment for an audio item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\HlsSegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "item_id_example"; // string | The item id.
$segment_id = "segment_id_example"; // string | The segment id.

try {
    $result = $apiInstance->getHlsAudioSegmentLegacyAac($item_id, $segment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HlsSegmentApi->getHlsAudioSegmentLegacyAac: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **string**| The item id. |
 **segment_id** | **string**| The segment id. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: audio/_*

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getHlsAudioSegmentLegacyMp3**
> string getHlsAudioSegmentLegacyMp3($item_id, $segment_id)

Gets the specified audio segment for an audio item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\HlsSegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "item_id_example"; // string | The item id.
$segment_id = "segment_id_example"; // string | The segment id.

try {
    $result = $apiInstance->getHlsAudioSegmentLegacyMp3($item_id, $segment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HlsSegmentApi->getHlsAudioSegmentLegacyMp3: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **string**| The item id. |
 **segment_id** | **string**| The segment id. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: audio/_*

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getHlsPlaylistLegacy**
> string getHlsPlaylistLegacy($item_id, $playlist_id)

Gets a hls video playlist.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\HlsSegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "item_id_example"; // string | The video id.
$playlist_id = "playlist_id_example"; // string | The playlist id.

try {
    $result = $apiInstance->getHlsPlaylistLegacy($item_id, $playlist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HlsSegmentApi->getHlsPlaylistLegacy: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **string**| The video id. |
 **playlist_id** | **string**| The playlist id. |

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/x-mpegURL

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getHlsVideoSegmentLegacy**
> string getHlsVideoSegmentLegacy($item_id, $playlist_id, $segment_id, $segment_container)

Gets a hls video segment.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\HlsSegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "item_id_example"; // string | The item id.
$playlist_id = "playlist_id_example"; // string | The playlist id.
$segment_id = "segment_id_example"; // string | The segment id.
$segment_container = "segment_container_example"; // string | The segment container.

try {
    $result = $apiInstance->getHlsVideoSegmentLegacy($item_id, $playlist_id, $segment_id, $segment_container);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HlsSegmentApi->getHlsVideoSegmentLegacy: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | **string**| The item id. |
 **playlist_id** | **string**| The playlist id. |
 **segment_id** | **string**| The segment id. |
 **segment_container** | **string**| The segment container. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: video/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **stopEncodingProcess**
> stopEncodingProcess($device_id, $play_session_id)

Stops an active encoding.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\HlsSegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = "device_id_example"; // string | The device id of the client requesting. Used to stop encoding processes when needed.
$play_session_id = "play_session_id_example"; // string | The play session id.

try {
    $apiInstance->stopEncodingProcess($device_id, $play_session_id);
} catch (Exception $e) {
    echo 'Exception when calling HlsSegmentApi->stopEncodingProcess: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_id** | **string**| The device id of the client requesting. Used to stop encoding processes when needed. | [optional]
 **play_session_id** | **string**| The play session id. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

