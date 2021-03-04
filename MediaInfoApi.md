# Swagger\Client\MediaInfoApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**closeLiveStream**](MediaInfoApi.md#closelivestream) | **POST** /LiveStreams/Close | Closes a media source.
[**getBitrateTestBytes**](MediaInfoApi.md#getbitratetestbytes) | **GET** /Playback/BitrateTest | Tests the network with a request with the size of the bitrate.
[**getPlaybackInfo**](MediaInfoApi.md#getplaybackinfo) | **GET** /Items/{itemId}/PlaybackInfo | Gets live playback media info for an item.
[**getPostedPlaybackInfo**](MediaInfoApi.md#getpostedplaybackinfo) | **POST** /Items/{itemId}/PlaybackInfo | Gets live playback media info for an item.
[**openLiveStream**](MediaInfoApi.md#openlivestream) | **POST** /LiveStreams/Open | Opens a media source.

# **closeLiveStream**
> closeLiveStream($live_stream_id)

Closes a media source.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaInfoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$live_stream_id = "live_stream_id_example"; // string | The livestream id.

try {
    $apiInstance->closeLiveStream($live_stream_id);
} catch (Exception $e) {
    echo 'Exception when calling MediaInfoApi->closeLiveStream: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **live_stream_id** | **string**| The livestream id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBitrateTestBytes**
> string getBitrateTestBytes($size)

Tests the network with a request with the size of the bitrate.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaInfoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$size = 102400; // int | The bitrate. Defaults to 102400.

try {
    $result = $apiInstance->getBitrateTestBytes($size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaInfoApi->getBitrateTestBytes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **size** | **int**| The bitrate. Defaults to 102400. | [optional] [default to 102400]

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPlaybackInfo**
> \Swagger\Client\Model\PlaybackInfoResponse getPlaybackInfo($item_id, $user_id)

Gets live playback media info for an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaInfoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The user id.

try {
    $result = $apiInstance->getPlaybackInfo($item_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaInfoApi->getPlaybackInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **user_id** | [**string**](../Model/.md)| The user id. |

### Return type

[**\Swagger\Client\Model\PlaybackInfoResponse**](../Model/PlaybackInfoResponse.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPostedPlaybackInfo**
> \Swagger\Client\Model\PlaybackInfoResponse getPostedPlaybackInfo($item_id, $body, $user_id, $max_streaming_bitrate, $start_time_ticks, $audio_stream_index, $subtitle_stream_index, $max_audio_channels, $media_source_id, $live_stream_id, $auto_open_live_stream, $enable_direct_play, $enable_direct_stream, $enable_transcoding, $allow_video_stream_copy, $allow_audio_stream_copy)

Gets live playback media info for an item.

For backwards compatibility parameters can be sent via Query or Body, with Query having higher precedence.  Query parameters are obsolete.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaInfoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$body = new \Swagger\Client\Model\PlaybackInfoDto(); // \Swagger\Client\Model\PlaybackInfoDto | The playback info.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The user id.
$max_streaming_bitrate = 56; // int | The maximum streaming bitrate.
$start_time_ticks = 789; // int | The start time in ticks.
$audio_stream_index = 56; // int | The audio stream index.
$subtitle_stream_index = 56; // int | The subtitle stream index.
$max_audio_channels = 56; // int | The maximum number of audio channels.
$media_source_id = "media_source_id_example"; // string | The media source id.
$live_stream_id = "live_stream_id_example"; // string | The livestream id.
$auto_open_live_stream = true; // bool | Whether to auto open the livestream.
$enable_direct_play = true; // bool | Whether to enable direct play. Default: true.
$enable_direct_stream = true; // bool | Whether to enable direct stream. Default: true.
$enable_transcoding = true; // bool | Whether to enable transcoding. Default: true.
$allow_video_stream_copy = true; // bool | Whether to allow to copy the video stream. Default: true.
$allow_audio_stream_copy = true; // bool | Whether to allow to copy the audio stream. Default: true.

try {
    $result = $apiInstance->getPostedPlaybackInfo($item_id, $body, $user_id, $max_streaming_bitrate, $start_time_ticks, $audio_stream_index, $subtitle_stream_index, $max_audio_channels, $media_source_id, $live_stream_id, $auto_open_live_stream, $enable_direct_play, $enable_direct_stream, $enable_transcoding, $allow_video_stream_copy, $allow_audio_stream_copy);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaInfoApi->getPostedPlaybackInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| The item id. |
 **body** | [**\Swagger\Client\Model\PlaybackInfoDto**](../Model/PlaybackInfoDto.md)| The playback info. | [optional]
 **user_id** | [**string**](../Model/.md)| The user id. | [optional]
 **max_streaming_bitrate** | **int**| The maximum streaming bitrate. | [optional]
 **start_time_ticks** | **int**| The start time in ticks. | [optional]
 **audio_stream_index** | **int**| The audio stream index. | [optional]
 **subtitle_stream_index** | **int**| The subtitle stream index. | [optional]
 **max_audio_channels** | **int**| The maximum number of audio channels. | [optional]
 **media_source_id** | **string**| The media source id. | [optional]
 **live_stream_id** | **string**| The livestream id. | [optional]
 **auto_open_live_stream** | **bool**| Whether to auto open the livestream. | [optional]
 **enable_direct_play** | **bool**| Whether to enable direct play. Default: true. | [optional]
 **enable_direct_stream** | **bool**| Whether to enable direct stream. Default: true. | [optional]
 **enable_transcoding** | **bool**| Whether to enable transcoding. Default: true. | [optional]
 **allow_video_stream_copy** | **bool**| Whether to allow to copy the video stream. Default: true. | [optional]
 **allow_audio_stream_copy** | **bool**| Whether to allow to copy the audio stream. Default: true. | [optional]

### Return type

[**\Swagger\Client\Model\PlaybackInfoResponse**](../Model/PlaybackInfoResponse.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **openLiveStream**
> \Swagger\Client\Model\LiveStreamResponse openLiveStream($body, $open_token, $user_id, $play_session_id, $max_streaming_bitrate, $start_time_ticks, $audio_stream_index, $subtitle_stream_index, $max_audio_channels, $item_id, $enable_direct_play, $enable_direct_stream)

Opens a media source.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MediaInfoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\OpenLiveStreamDto(); // \Swagger\Client\Model\OpenLiveStreamDto | The open live stream dto.
$open_token = "open_token_example"; // string | The open token.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The user id.
$play_session_id = "play_session_id_example"; // string | The play session id.
$max_streaming_bitrate = 56; // int | The maximum streaming bitrate.
$start_time_ticks = 789; // int | The start time in ticks.
$audio_stream_index = 56; // int | The audio stream index.
$subtitle_stream_index = 56; // int | The subtitle stream index.
$max_audio_channels = 56; // int | The maximum number of audio channels.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$enable_direct_play = true; // bool | Whether to enable direct play. Default: true.
$enable_direct_stream = true; // bool | Whether to enable direct stream. Default: true.

try {
    $result = $apiInstance->openLiveStream($body, $open_token, $user_id, $play_session_id, $max_streaming_bitrate, $start_time_ticks, $audio_stream_index, $subtitle_stream_index, $max_audio_channels, $item_id, $enable_direct_play, $enable_direct_stream);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaInfoApi->openLiveStream: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\OpenLiveStreamDto**](../Model/OpenLiveStreamDto.md)| The open live stream dto. | [optional]
 **open_token** | **string**| The open token. | [optional]
 **user_id** | [**string**](../Model/.md)| The user id. | [optional]
 **play_session_id** | **string**| The play session id. | [optional]
 **max_streaming_bitrate** | **int**| The maximum streaming bitrate. | [optional]
 **start_time_ticks** | **int**| The start time in ticks. | [optional]
 **audio_stream_index** | **int**| The audio stream index. | [optional]
 **subtitle_stream_index** | **int**| The subtitle stream index. | [optional]
 **max_audio_channels** | **int**| The maximum number of audio channels. | [optional]
 **item_id** | [**string**](../Model/.md)| The item id. | [optional]
 **enable_direct_play** | **bool**| Whether to enable direct play. Default: true. | [optional]
 **enable_direct_stream** | **bool**| Whether to enable direct stream. Default: true. | [optional]

### Return type

[**\Swagger\Client\Model\LiveStreamResponse**](../Model/LiveStreamResponse.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

