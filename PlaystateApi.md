# Swagger\Client\PlaystateApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**markPlayedItem**](PlaystateApi.md#markplayeditem) | **POST** /Users/{userId}/PlayedItems/{itemId} | Marks an item as played for user.
[**markUnplayedItem**](PlaystateApi.md#markunplayeditem) | **DELETE** /Users/{userId}/PlayedItems/{itemId} | Marks an item as unplayed for user.
[**onPlaybackProgress**](PlaystateApi.md#onplaybackprogress) | **POST** /Users/{userId}/PlayingItems/{itemId}/Progress | Reports a user&#x27;s playback progress.
[**onPlaybackStart**](PlaystateApi.md#onplaybackstart) | **POST** /Users/{userId}/PlayingItems/{itemId} | Reports that a user has begun playing an item.
[**onPlaybackStopped**](PlaystateApi.md#onplaybackstopped) | **DELETE** /Users/{userId}/PlayingItems/{itemId} | Reports that a user has stopped playing an item.
[**pingPlaybackSession**](PlaystateApi.md#pingplaybacksession) | **POST** /Sessions/Playing/Ping | Pings a playback session.
[**reportPlaybackProgress**](PlaystateApi.md#reportplaybackprogress) | **POST** /Sessions/Playing/Progress | Reports playback progress within a session.
[**reportPlaybackStart**](PlaystateApi.md#reportplaybackstart) | **POST** /Sessions/Playing | Reports playback has started within a session.
[**reportPlaybackStopped**](PlaystateApi.md#reportplaybackstopped) | **POST** /Sessions/Playing/Stopped | Reports playback has stopped within a session.

# **markPlayedItem**
> \Swagger\Client\Model\UserItemDataDto markPlayedItem($user_id, $item_id, $date_played)

Marks an item as played for user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$date_played = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The date the item was played.

try {
    $result = $apiInstance->markPlayedItem($user_id, $item_id, $date_played);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->markPlayedItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |
 **date_played** | **\DateTime**| Optional. The date the item was played. | [optional]

### Return type

[**\Swagger\Client\Model\UserItemDataDto**](../Model/UserItemDataDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **markUnplayedItem**
> \Swagger\Client\Model\UserItemDataDto markUnplayedItem($user_id, $item_id)

Marks an item as unplayed for user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->markUnplayedItem($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->markUnplayedItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |

### Return type

[**\Swagger\Client\Model\UserItemDataDto**](../Model/UserItemDataDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **onPlaybackProgress**
> onPlaybackProgress($user_id, $item_id, $media_source_id, $position_ticks, $audio_stream_index, $subtitle_stream_index, $volume_level, $play_method, $live_stream_id, $play_session_id, $repeat_mode, $is_paused, $is_muted)

Reports a user's playback progress.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$media_source_id = "media_source_id_example"; // string | The id of the MediaSource.
$position_ticks = 789; // int | Optional. The current position, in ticks. 1 tick = 10000 ms.
$audio_stream_index = 56; // int | The audio stream index.
$subtitle_stream_index = 56; // int | The subtitle stream index.
$volume_level = 56; // int | Scale of 0-100.
$play_method = new \Swagger\Client\Model\PlayMethod(); // \Swagger\Client\Model\PlayMethod | The play method.
$live_stream_id = "live_stream_id_example"; // string | The live stream id.
$play_session_id = "play_session_id_example"; // string | The play session id.
$repeat_mode = new \Swagger\Client\Model\RepeatMode(); // \Swagger\Client\Model\RepeatMode | The repeat mode.
$is_paused = false; // bool | Indicates if the player is paused.
$is_muted = false; // bool | Indicates if the player is muted.

try {
    $apiInstance->onPlaybackProgress($user_id, $item_id, $media_source_id, $position_ticks, $audio_stream_index, $subtitle_stream_index, $volume_level, $play_method, $live_stream_id, $play_session_id, $repeat_mode, $is_paused, $is_muted);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->onPlaybackProgress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |
 **media_source_id** | **string**| The id of the MediaSource. | [optional]
 **position_ticks** | **int**| Optional. The current position, in ticks. 1 tick &#x3D; 10000 ms. | [optional]
 **audio_stream_index** | **int**| The audio stream index. | [optional]
 **subtitle_stream_index** | **int**| The subtitle stream index. | [optional]
 **volume_level** | **int**| Scale of 0-100. | [optional]
 **play_method** | [**\Swagger\Client\Model\PlayMethod**](../Model/.md)| The play method. | [optional]
 **live_stream_id** | **string**| The live stream id. | [optional]
 **play_session_id** | **string**| The play session id. | [optional]
 **repeat_mode** | [**\Swagger\Client\Model\RepeatMode**](../Model/.md)| The repeat mode. | [optional]
 **is_paused** | **bool**| Indicates if the player is paused. | [optional] [default to false]
 **is_muted** | **bool**| Indicates if the player is muted. | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **onPlaybackStart**
> onPlaybackStart($user_id, $item_id, $media_source_id, $audio_stream_index, $subtitle_stream_index, $play_method, $live_stream_id, $play_session_id, $can_seek)

Reports that a user has begun playing an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$media_source_id = "media_source_id_example"; // string | The id of the MediaSource.
$audio_stream_index = 56; // int | The audio stream index.
$subtitle_stream_index = 56; // int | The subtitle stream index.
$play_method = new \Swagger\Client\Model\PlayMethod(); // \Swagger\Client\Model\PlayMethod | The play method.
$live_stream_id = "live_stream_id_example"; // string | The live stream id.
$play_session_id = "play_session_id_example"; // string | The play session id.
$can_seek = false; // bool | Indicates if the client can seek.

try {
    $apiInstance->onPlaybackStart($user_id, $item_id, $media_source_id, $audio_stream_index, $subtitle_stream_index, $play_method, $live_stream_id, $play_session_id, $can_seek);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->onPlaybackStart: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |
 **media_source_id** | **string**| The id of the MediaSource. | [optional]
 **audio_stream_index** | **int**| The audio stream index. | [optional]
 **subtitle_stream_index** | **int**| The subtitle stream index. | [optional]
 **play_method** | [**\Swagger\Client\Model\PlayMethod**](../Model/.md)| The play method. | [optional]
 **live_stream_id** | **string**| The live stream id. | [optional]
 **play_session_id** | **string**| The play session id. | [optional]
 **can_seek** | **bool**| Indicates if the client can seek. | [optional] [default to false]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **onPlaybackStopped**
> onPlaybackStopped($user_id, $item_id, $media_source_id, $next_media_type, $position_ticks, $live_stream_id, $play_session_id)

Reports that a user has stopped playing an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$media_source_id = "media_source_id_example"; // string | The id of the MediaSource.
$next_media_type = "next_media_type_example"; // string | The next media type that will play.
$position_ticks = 789; // int | Optional. The position, in ticks, where playback stopped. 1 tick = 10000 ms.
$live_stream_id = "live_stream_id_example"; // string | The live stream id.
$play_session_id = "play_session_id_example"; // string | The play session id.

try {
    $apiInstance->onPlaybackStopped($user_id, $item_id, $media_source_id, $next_media_type, $position_ticks, $live_stream_id, $play_session_id);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->onPlaybackStopped: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |
 **media_source_id** | **string**| The id of the MediaSource. | [optional]
 **next_media_type** | **string**| The next media type that will play. | [optional]
 **position_ticks** | **int**| Optional. The position, in ticks, where playback stopped. 1 tick &#x3D; 10000 ms. | [optional]
 **live_stream_id** | **string**| The live stream id. | [optional]
 **play_session_id** | **string**| The play session id. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pingPlaybackSession**
> pingPlaybackSession($play_session_id)

Pings a playback session.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$play_session_id = "play_session_id_example"; // string | Playback session id.

try {
    $apiInstance->pingPlaybackSession($play_session_id);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->pingPlaybackSession: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **play_session_id** | **string**| Playback session id. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reportPlaybackProgress**
> reportPlaybackProgress($body)

Reports playback progress within a session.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PlaybackProgressInfo(); // \Swagger\Client\Model\PlaybackProgressInfo | The playback progress info.

try {
    $apiInstance->reportPlaybackProgress($body);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->reportPlaybackProgress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PlaybackProgressInfo**](../Model/PlaybackProgressInfo.md)| The playback progress info. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reportPlaybackStart**
> reportPlaybackStart($body)

Reports playback has started within a session.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PlaybackStartInfo(); // \Swagger\Client\Model\PlaybackStartInfo | The playback start info.

try {
    $apiInstance->reportPlaybackStart($body);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->reportPlaybackStart: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PlaybackStartInfo**](../Model/PlaybackStartInfo.md)| The playback start info. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reportPlaybackStopped**
> reportPlaybackStopped($body)

Reports playback has stopped within a session.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaystateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PlaybackStopInfo(); // \Swagger\Client\Model\PlaybackStopInfo | The playback stop info.

try {
    $apiInstance->reportPlaybackStopped($body);
} catch (Exception $e) {
    echo 'Exception when calling PlaystateApi->reportPlaybackStopped: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PlaybackStopInfo**](../Model/PlaybackStopInfo.md)| The playback stop info. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

