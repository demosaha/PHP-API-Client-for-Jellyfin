# Swagger\Client\SubtitleApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteSubtitle**](SubtitleApi.md#deletesubtitle) | **DELETE** /Videos/{itemId}/Subtitles/{index} | Deletes an external subtitle file.
[**downloadRemoteSubtitles**](SubtitleApi.md#downloadremotesubtitles) | **POST** /Items/{itemId}/RemoteSearch/Subtitles/{subtitleId} | Downloads a remote subtitle.
[**getFallbackFont**](SubtitleApi.md#getfallbackfont) | **GET** /FallbackFont/Fonts/{name} | Gets a fallback font file.
[**getFallbackFontList**](SubtitleApi.md#getfallbackfontlist) | **GET** /FallbackFont/Fonts | Gets a list of available fallback font files.
[**getRemoteSubtitles**](SubtitleApi.md#getremotesubtitles) | **GET** /Providers/Subtitles/Subtitles/{id} | Gets the remote subtitles.
[**getSubtitle**](SubtitleApi.md#getsubtitle) | **GET** /Videos/{itemId}/{mediaSourceId}/Subtitles/{index}/Stream.{format} | Gets subtitles in a specified format.
[**getSubtitlePlaylist**](SubtitleApi.md#getsubtitleplaylist) | **GET** /Videos/{itemId}/{mediaSourceId}/Subtitles/{index}/subtitles.m3u8 | Gets an HLS subtitle playlist.
[**getSubtitleWithTicks**](SubtitleApi.md#getsubtitlewithticks) | **GET** /Videos/{itemId}/{mediaSourceId}/Subtitles/{index}/{startPositionTicks}/Stream.{format} | Gets subtitles in a specified format.
[**searchRemoteSubtitles**](SubtitleApi.md#searchremotesubtitles) | **GET** /Items/{itemId}/RemoteSearch/Subtitles/{language} | Search remote subtitles.
[**uploadSubtitle**](SubtitleApi.md#uploadsubtitle) | **POST** /Videos/{itemId}/Subtitles | Upload an external subtitle file.

# **deleteSubtitle**
> deleteSubtitle($item_id, $index)

Deletes an external subtitle file.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$index = 56; // int | The index of the subtitle file.

try {
    $apiInstance->deleteSubtitle($item_id, $index);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->deleteSubtitle: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **index** | **int**| The index of the subtitle file. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **downloadRemoteSubtitles**
> downloadRemoteSubtitles($item_id, $subtitle_id)

Downloads a remote subtitle.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$subtitle_id = "subtitle_id_example"; // string | The subtitle id.

try {
    $apiInstance->downloadRemoteSubtitles($item_id, $subtitle_id);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->downloadRemoteSubtitles: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **subtitle_id** | **string**| The subtitle id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFallbackFont**
> string getFallbackFont($name)

Gets a fallback font file.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | The name of the fallback font file to get.

try {
    $result = $apiInstance->getFallbackFont($name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->getFallbackFont: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| The name of the fallback font file to get. |

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: font/_*

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFallbackFontList**
> \Swagger\Client\Model\FontFile[] getFallbackFontList()

Gets a list of available fallback font files.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getFallbackFontList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->getFallbackFontList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\FontFile[]**](../Model/FontFile.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRemoteSubtitles**
> string getRemoteSubtitles($id)

Gets the remote subtitles.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | The item id.

try {
    $result = $apiInstance->getRemoteSubtitles($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->getRemoteSubtitles: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The item id. |

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/_*

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSubtitle**
> string getSubtitle($item_id, $media_source_id, $index, $format, $end_position_ticks, $copy_timestamps, $add_vtt_time_map, $start_position_ticks)

Gets subtitles in a specified format.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$media_source_id = "media_source_id_example"; // string | The media source id.
$index = 56; // int | The subtitle stream index.
$format = "format_example"; // string | The format of the returned subtitle.
$end_position_ticks = 789; // int | Optional. The end position of the subtitle in ticks.
$copy_timestamps = false; // bool | Optional. Whether to copy the timestamps.
$add_vtt_time_map = false; // bool | Optional. Whether to add a VTT time map.
$start_position_ticks = 0; // int | Optional. The start position of the subtitle in ticks.

try {
    $result = $apiInstance->getSubtitle($item_id, $media_source_id, $index, $format, $end_position_ticks, $copy_timestamps, $add_vtt_time_map, $start_position_ticks);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->getSubtitle: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **media_source_id** | **string**| The media source id. |
 **index** | **int**| The subtitle stream index. |
 **format** | **string**| The format of the returned subtitle. |
 **end_position_ticks** | **int**| Optional. The end position of the subtitle in ticks. | [optional]
 **copy_timestamps** | **bool**| Optional. Whether to copy the timestamps. | [optional] [default to false]
 **add_vtt_time_map** | **bool**| Optional. Whether to add a VTT time map. | [optional] [default to false]
 **start_position_ticks** | **int**| Optional. The start position of the subtitle in ticks. | [optional] [default to 0]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/_*

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSubtitlePlaylist**
> string getSubtitlePlaylist($item_id, $index, $media_source_id, $segment_length)

Gets an HLS subtitle playlist.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$index = 56; // int | The subtitle stream index.
$media_source_id = "media_source_id_example"; // string | The media source id.
$segment_length = 56; // int | The subtitle segment length.

try {
    $result = $apiInstance->getSubtitlePlaylist($item_id, $index, $media_source_id, $segment_length);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->getSubtitlePlaylist: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **index** | **int**| The subtitle stream index. |
 **media_source_id** | **string**| The media source id. |
 **segment_length** | **int**| The subtitle segment length. |

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/x-mpegURL

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSubtitleWithTicks**
> string getSubtitleWithTicks($item_id, $media_source_id, $index, $start_position_ticks, $format, $end_position_ticks, $copy_timestamps, $add_vtt_time_map)

Gets subtitles in a specified format.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$media_source_id = "media_source_id_example"; // string | The media source id.
$index = 56; // int | The subtitle stream index.
$start_position_ticks = 789; // int | Optional. The start position of the subtitle in ticks.
$format = "format_example"; // string | The format of the returned subtitle.
$end_position_ticks = 789; // int | Optional. The end position of the subtitle in ticks.
$copy_timestamps = false; // bool | Optional. Whether to copy the timestamps.
$add_vtt_time_map = false; // bool | Optional. Whether to add a VTT time map.

try {
    $result = $apiInstance->getSubtitleWithTicks($item_id, $media_source_id, $index, $start_position_ticks, $format, $end_position_ticks, $copy_timestamps, $add_vtt_time_map);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->getSubtitleWithTicks: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **media_source_id** | **string**| The media source id. |
 **index** | **int**| The subtitle stream index. |
 **start_position_ticks** | **int**| Optional. The start position of the subtitle in ticks. |
 **format** | **string**| The format of the returned subtitle. |
 **end_position_ticks** | **int**| Optional. The end position of the subtitle in ticks. | [optional]
 **copy_timestamps** | **bool**| Optional. Whether to copy the timestamps. | [optional] [default to false]
 **add_vtt_time_map** | **bool**| Optional. Whether to add a VTT time map. | [optional] [default to false]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/_*

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **searchRemoteSubtitles**
> \Swagger\Client\Model\RemoteSubtitleInfo[] searchRemoteSubtitles($item_id, $language, $is_perfect_match)

Search remote subtitles.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$language = "language_example"; // string | The language of the subtitles.
$is_perfect_match = true; // bool | Optional. Only show subtitles which are a perfect match.

try {
    $result = $apiInstance->searchRemoteSubtitles($item_id, $language, $is_perfect_match);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->searchRemoteSubtitles: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **language** | **string**| The language of the subtitles. |
 **is_perfect_match** | **bool**| Optional. Only show subtitles which are a perfect match. | [optional]

### Return type

[**\Swagger\Client\Model\RemoteSubtitleInfo[]**](../Model/RemoteSubtitleInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **uploadSubtitle**
> uploadSubtitle($body, $item_id)

Upload an external subtitle file.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SubtitleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\UploadSubtitleDto(); // \Swagger\Client\Model\UploadSubtitleDto | The request body.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item the subtitle belongs to.

try {
    $apiInstance->uploadSubtitle($body, $item_id);
} catch (Exception $e) {
    echo 'Exception when calling SubtitleApi->uploadSubtitle: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UploadSubtitleDto**](../Model/UploadSubtitleDto.md)| The request body. |
 **item_id** | [**string**](../Model/.md)| The item the subtitle belongs to. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

