# Swagger\Client\LiveTvApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addListingProvider**](LiveTvApi.md#addlistingprovider) | **POST** /LiveTv/ListingProviders | Adds a listings provider.
[**addTunerHost**](LiveTvApi.md#addtunerhost) | **POST** /LiveTv/TunerHosts | Adds a tuner host.
[**cancelSeriesTimer**](LiveTvApi.md#cancelseriestimer) | **DELETE** /LiveTv/SeriesTimers/{timerId} | Cancels a live tv series timer.
[**cancelTimer**](LiveTvApi.md#canceltimer) | **DELETE** /LiveTv/Timers/{timerId} | Cancels a live tv timer.
[**createSeriesTimer**](LiveTvApi.md#createseriestimer) | **POST** /LiveTv/SeriesTimers | Creates a live tv series timer.
[**createTimer**](LiveTvApi.md#createtimer) | **POST** /LiveTv/Timers | Creates a live tv timer.
[**deleteListingProvider**](LiveTvApi.md#deletelistingprovider) | **DELETE** /LiveTv/ListingProviders | Delete listing provider.
[**deleteRecording**](LiveTvApi.md#deleterecording) | **DELETE** /LiveTv/Recordings/{recordingId} | Deletes a live tv recording.
[**deleteTunerHost**](LiveTvApi.md#deletetunerhost) | **DELETE** /LiveTv/TunerHosts | Deletes a tuner host.
[**discoverTuners**](LiveTvApi.md#discovertuners) | **GET** /LiveTv/Tuners/Discover | Discover tuners.
[**discvoverTuners**](LiveTvApi.md#discvovertuners) | **GET** /LiveTv/Tuners/Discvover | Discover tuners.
[**getChannel**](LiveTvApi.md#getchannel) | **GET** /LiveTv/Channels/{channelId} | Gets a live tv channel.
[**getChannelMappingOptions**](LiveTvApi.md#getchannelmappingoptions) | **GET** /LiveTv/ChannelMappingOptions | Get channel mapping options.
[**getDefaultListingProvider**](LiveTvApi.md#getdefaultlistingprovider) | **GET** /LiveTv/ListingProviders/Default | Gets default listings provider info.
[**getDefaultTimer**](LiveTvApi.md#getdefaulttimer) | **GET** /LiveTv/Timers/Defaults | Gets the default values for a new timer.
[**getGuideInfo**](LiveTvApi.md#getguideinfo) | **GET** /LiveTv/GuideInfo | Get guid info.
[**getLineups**](LiveTvApi.md#getlineups) | **GET** /LiveTv/ListingProviders/Lineups | Gets available lineups.
[**getLiveRecordingFile**](LiveTvApi.md#getliverecordingfile) | **GET** /LiveTv/LiveRecordings/{recordingId}/stream | Gets a live tv recording stream.
[**getLiveStreamFile**](LiveTvApi.md#getlivestreamfile) | **GET** /LiveTv/LiveStreamFiles/{streamId}/stream.{container} | Gets a live tv channel stream.
[**getLiveTvChannels**](LiveTvApi.md#getlivetvchannels) | **GET** /LiveTv/Channels | Gets available live tv channels.
[**getLiveTvInfo**](LiveTvApi.md#getlivetvinfo) | **GET** /LiveTv/Info | Gets available live tv services.
[**getLiveTvPrograms**](LiveTvApi.md#getlivetvprograms) | **GET** /LiveTv/Programs | Gets available live tv epgs.
[**getProgram**](LiveTvApi.md#getprogram) | **GET** /LiveTv/Programs/{programId} | Gets a live tv program.
[**getPrograms**](LiveTvApi.md#getprograms) | **POST** /LiveTv/Programs | Gets available live tv epgs.
[**getRecommendedPrograms**](LiveTvApi.md#getrecommendedprograms) | **GET** /LiveTv/Programs/Recommended | Gets recommended live tv epgs.
[**getRecording**](LiveTvApi.md#getrecording) | **GET** /LiveTv/Recordings/{recordingId} | Gets a live tv recording.
[**getRecordingFolders**](LiveTvApi.md#getrecordingfolders) | **GET** /LiveTv/Recordings/Folders | Gets recording folders.
[**getRecordingGroup**](LiveTvApi.md#getrecordinggroup) | **GET** /LiveTv/Recordings/Groups/{groupId} | Get recording group.
[**getRecordingGroups**](LiveTvApi.md#getrecordinggroups) | **GET** /LiveTv/Recordings/Groups | Gets live tv recording groups.
[**getRecordings**](LiveTvApi.md#getrecordings) | **GET** /LiveTv/Recordings | Gets live tv recordings.
[**getRecordingsSeries**](LiveTvApi.md#getrecordingsseries) | **GET** /LiveTv/Recordings/Series | Gets live tv recording series.
[**getSchedulesDirectCountries**](LiveTvApi.md#getschedulesdirectcountries) | **GET** /LiveTv/ListingProviders/SchedulesDirect/Countries | Gets available countries.
[**getSeriesTimer**](LiveTvApi.md#getseriestimer) | **GET** /LiveTv/SeriesTimers/{timerId} | Gets a live tv series timer.
[**getSeriesTimers**](LiveTvApi.md#getseriestimers) | **GET** /LiveTv/SeriesTimers | Gets live tv series timers.
[**getTimer**](LiveTvApi.md#gettimer) | **GET** /LiveTv/Timers/{timerId} | Gets a timer.
[**getTimers**](LiveTvApi.md#gettimers) | **GET** /LiveTv/Timers | Gets the live tv timers.
[**getTunerHostTypes**](LiveTvApi.md#gettunerhosttypes) | **GET** /LiveTv/TunerHosts/Types | Get tuner host types.
[**resetTuner**](LiveTvApi.md#resettuner) | **POST** /LiveTv/Tuners/{tunerId}/Reset | Resets a tv tuner.
[**setChannelMapping**](LiveTvApi.md#setchannelmapping) | **POST** /LiveTv/ChannelMappings | Set channel mappings.
[**updateSeriesTimer**](LiveTvApi.md#updateseriestimer) | **POST** /LiveTv/SeriesTimers/{timerId} | Updates a live tv series timer.
[**updateTimer**](LiveTvApi.md#updatetimer) | **POST** /LiveTv/Timers/{timerId} | Updates a live tv timer.

# **addListingProvider**
> \Swagger\Client\Model\ListingsProviderInfo addListingProvider($body, $pw, $validate_listings, $validate_login)

Adds a listings provider.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ListingsProviderInfo(); // \Swagger\Client\Model\ListingsProviderInfo | New listings info.
$pw = "pw_example"; // string | Password.
$validate_listings = false; // bool | Validate listings.
$validate_login = false; // bool | Validate login.

try {
    $result = $apiInstance->addListingProvider($body, $pw, $validate_listings, $validate_login);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->addListingProvider: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ListingsProviderInfo**](../Model/ListingsProviderInfo.md)| New listings info. | [optional]
 **pw** | **string**| Password. | [optional]
 **validate_listings** | **bool**| Validate listings. | [optional] [default to false]
 **validate_login** | **bool**| Validate login. | [optional] [default to false]

### Return type

[**\Swagger\Client\Model\ListingsProviderInfo**](../Model/ListingsProviderInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **addTunerHost**
> \Swagger\Client\Model\TunerHostInfo addTunerHost($body)

Adds a tuner host.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TunerHostInfo(); // \Swagger\Client\Model\TunerHostInfo | New tuner host.

try {
    $result = $apiInstance->addTunerHost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->addTunerHost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TunerHostInfo**](../Model/TunerHostInfo.md)| New tuner host. | [optional]

### Return type

[**\Swagger\Client\Model\TunerHostInfo**](../Model/TunerHostInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cancelSeriesTimer**
> cancelSeriesTimer($timer_id)

Cancels a live tv series timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$timer_id = "timer_id_example"; // string | Timer id.

try {
    $apiInstance->cancelSeriesTimer($timer_id);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->cancelSeriesTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **timer_id** | **string**| Timer id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cancelTimer**
> cancelTimer($timer_id)

Cancels a live tv timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$timer_id = "timer_id_example"; // string | Timer id.

try {
    $apiInstance->cancelTimer($timer_id);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->cancelTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **timer_id** | **string**| Timer id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createSeriesTimer**
> createSeriesTimer($body)

Creates a live tv series timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\SeriesTimerInfoDto(); // \Swagger\Client\Model\SeriesTimerInfoDto | New series timer info.

try {
    $apiInstance->createSeriesTimer($body);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->createSeriesTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\SeriesTimerInfoDto**](../Model/SeriesTimerInfoDto.md)| New series timer info. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createTimer**
> createTimer($body)

Creates a live tv timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TimerInfoDto(); // \Swagger\Client\Model\TimerInfoDto | New timer info.

try {
    $apiInstance->createTimer($body);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->createTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TimerInfoDto**](../Model/TimerInfoDto.md)| New timer info. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteListingProvider**
> deleteListingProvider($id)

Delete listing provider.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Listing provider id.

try {
    $apiInstance->deleteListingProvider($id);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->deleteListingProvider: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Listing provider id. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteRecording**
> deleteRecording($recording_id)

Deletes a live tv recording.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recording_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Recording id.

try {
    $apiInstance->deleteRecording($recording_id);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->deleteRecording: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_id** | [**string**](../Model/.md)| Recording id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteTunerHost**
> deleteTunerHost($id)

Deletes a tuner host.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Tuner host id.

try {
    $apiInstance->deleteTunerHost($id);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->deleteTunerHost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Tuner host id. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **discoverTuners**
> \Swagger\Client\Model\TunerHostInfo[] discoverTuners($new_devices_only)

Discover tuners.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$new_devices_only = false; // bool | Only discover new tuners.

try {
    $result = $apiInstance->discoverTuners($new_devices_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->discoverTuners: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_devices_only** | **bool**| Only discover new tuners. | [optional] [default to false]

### Return type

[**\Swagger\Client\Model\TunerHostInfo[]**](../Model/TunerHostInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **discvoverTuners**
> \Swagger\Client\Model\TunerHostInfo[] discvoverTuners($new_devices_only)

Discover tuners.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$new_devices_only = false; // bool | Only discover new tuners.

try {
    $result = $apiInstance->discvoverTuners($new_devices_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->discvoverTuners: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new_devices_only** | **bool**| Only discover new tuners. | [optional] [default to false]

### Return type

[**\Swagger\Client\Model\TunerHostInfo[]**](../Model/TunerHostInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChannel**
> \Swagger\Client\Model\BaseItemDto getChannel($channel_id, $user_id)

Gets a live tv channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Channel id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Attach user data.

try {
    $result = $apiInstance->getChannel($channel_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getChannel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | [**string**](../Model/.md)| Channel id. |
 **user_id** | [**string**](../Model/.md)| Optional. Attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChannelMappingOptions**
> \Swagger\Client\Model\ChannelMappingOptionsDto getChannelMappingOptions($provider_id)

Get channel mapping options.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider_id = "provider_id_example"; // string | Provider id.

try {
    $result = $apiInstance->getChannelMappingOptions($provider_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getChannelMappingOptions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provider_id** | **string**| Provider id. | [optional]

### Return type

[**\Swagger\Client\Model\ChannelMappingOptionsDto**](../Model/ChannelMappingOptionsDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDefaultListingProvider**
> \Swagger\Client\Model\ListingsProviderInfo getDefaultListingProvider()

Gets default listings provider info.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getDefaultListingProvider();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getDefaultListingProvider: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ListingsProviderInfo**](../Model/ListingsProviderInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDefaultTimer**
> \Swagger\Client\Model\SeriesTimerInfoDto getDefaultTimer($program_id)

Gets the default values for a new timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$program_id = "program_id_example"; // string | Optional. To attach default values based on a program.

try {
    $result = $apiInstance->getDefaultTimer($program_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getDefaultTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **program_id** | **string**| Optional. To attach default values based on a program. | [optional]

### Return type

[**\Swagger\Client\Model\SeriesTimerInfoDto**](../Model/SeriesTimerInfoDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getGuideInfo**
> \Swagger\Client\Model\GuideInfo getGuideInfo()

Get guid info.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getGuideInfo();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getGuideInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\GuideInfo**](../Model/GuideInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLineups**
> \Swagger\Client\Model\NameIdPair[] getLineups($id, $type, $location, $country)

Gets available lineups.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | Provider id.
$type = "type_example"; // string | Provider type.
$location = "location_example"; // string | Location.
$country = "country_example"; // string | Country.

try {
    $result = $apiInstance->getLineups($id, $type, $location, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getLineups: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Provider id. | [optional]
 **type** | **string**| Provider type. | [optional]
 **location** | **string**| Location. | [optional]
 **country** | **string**| Country. | [optional]

### Return type

[**\Swagger\Client\Model\NameIdPair[]**](../Model/NameIdPair.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLiveRecordingFile**
> string getLiveRecordingFile($recording_id)

Gets a live tv recording stream.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_id = "recording_id_example"; // string | Recording id.

try {
    $result = $apiInstance->getLiveRecordingFile($recording_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getLiveRecordingFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_id** | **string**| Recording id. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: video/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLiveStreamFile**
> string getLiveStreamFile($stream_id, $container)

Gets a live tv channel stream.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$stream_id = "stream_id_example"; // string | Stream id.
$container = "container_example"; // string | Container type.

try {
    $result = $apiInstance->getLiveStreamFile($stream_id, $container);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getLiveStreamFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stream_id** | **string**| Stream id. |
 **container** | **string**| Container type. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: video/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLiveTvChannels**
> \Swagger\Client\Model\BaseItemDtoQueryResult getLiveTvChannels($type, $user_id, $start_index, $is_movie, $is_series, $is_news, $is_kids, $is_sports, $limit, $is_favorite, $is_liked, $is_disliked, $enable_images, $image_type_limit, $enable_image_types, $fields, $enable_user_data, $sort_by, $sort_order, $enable_favorite_sorting, $add_current_program)

Gets available live tv channels.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$type = new \Swagger\Client\Model\ChannelType(); // \Swagger\Client\Model\ChannelType | Optional. Filter by channel type.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user and attach user data.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$is_movie = true; // bool | Optional. Filter for movies.
$is_series = true; // bool | Optional. Filter for series.
$is_news = true; // bool | Optional. Filter for news.
$is_kids = true; // bool | Optional. Filter for kids.
$is_sports = true; // bool | Optional. Filter for sports.
$limit = 56; // int | Optional. The maximum number of records to return.
$is_favorite = true; // bool | Optional. Filter by channels that are favorites, or not.
$is_liked = true; // bool | Optional. Filter by channels that are liked, or not.
$is_disliked = true; // bool | Optional. Filter by channels that are disliked, or not.
$enable_images = true; // bool | Optional. Include image information in output.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | \"Optional. The image types to include in the output.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_user_data = true; // bool | Optional. Include user data.
$sort_by = array("sort_by_example"); // string[] | Optional. Key to sort by.
$sort_order = new \Swagger\Client\Model\SortOrder(); // \Swagger\Client\Model\SortOrder | Optional. Sort order.
$enable_favorite_sorting = false; // bool | Optional. Incorporate favorite and like status into channel sorting.
$add_current_program = true; // bool | Optional. Adds current program info to each channel.

try {
    $result = $apiInstance->getLiveTvChannels($type, $user_id, $start_index, $is_movie, $is_series, $is_news, $is_kids, $is_sports, $limit, $is_favorite, $is_liked, $is_disliked, $enable_images, $image_type_limit, $enable_image_types, $fields, $enable_user_data, $sort_by, $sort_order, $enable_favorite_sorting, $add_current_program);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getLiveTvChannels: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | [**\Swagger\Client\Model\ChannelType**](../Model/.md)| Optional. Filter by channel type. | [optional]
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user and attach user data. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **is_movie** | **bool**| Optional. Filter for movies. | [optional]
 **is_series** | **bool**| Optional. Filter for series. | [optional]
 **is_news** | **bool**| Optional. Filter for news. | [optional]
 **is_kids** | **bool**| Optional. Filter for kids. | [optional]
 **is_sports** | **bool**| Optional. Filter for sports. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **is_favorite** | **bool**| Optional. Filter by channels that are favorites, or not. | [optional]
 **is_liked** | **bool**| Optional. Filter by channels that are liked, or not. | [optional]
 **is_disliked** | **bool**| Optional. Filter by channels that are disliked, or not. | [optional]
 **enable_images** | **bool**| Optional. Include image information in output. | [optional]
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| \&quot;Optional. The image types to include in the output. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **enable_user_data** | **bool**| Optional. Include user data. | [optional]
 **sort_by** | [**string[]**](../Model/string.md)| Optional. Key to sort by. | [optional]
 **sort_order** | [**\Swagger\Client\Model\SortOrder**](../Model/.md)| Optional. Sort order. | [optional]
 **enable_favorite_sorting** | **bool**| Optional. Incorporate favorite and like status into channel sorting. | [optional] [default to false]
 **add_current_program** | **bool**| Optional. Adds current program info to each channel. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLiveTvInfo**
> \Swagger\Client\Model\LiveTvInfo getLiveTvInfo()

Gets available live tv services.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getLiveTvInfo();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getLiveTvInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\LiveTvInfo**](../Model/LiveTvInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLiveTvPrograms**
> \Swagger\Client\Model\BaseItemDtoQueryResult getLiveTvPrograms($channel_ids, $user_id, $min_start_date, $has_aired, $is_airing, $max_start_date, $min_end_date, $max_end_date, $is_movie, $is_series, $is_news, $is_kids, $is_sports, $start_index, $limit, $sort_by, $sort_order, $genres, $genre_ids, $enable_images, $image_type_limit, $enable_image_types, $enable_user_data, $series_timer_id, $library_series_id, $fields, $enable_total_record_count)

Gets available live tv epgs.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_ids = array("channel_ids_example"); // string[] | The channels to return guide information for.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id.
$min_start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The minimum premiere start date.
$has_aired = true; // bool | Optional. Filter by programs that have completed airing, or not.
$is_airing = true; // bool | Optional. Filter by programs that are currently airing, or not.
$max_start_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The maximum premiere start date.
$min_end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The minimum premiere end date.
$max_end_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The maximum premiere end date.
$is_movie = true; // bool | Optional. Filter for movies.
$is_series = true; // bool | Optional. Filter for series.
$is_news = true; // bool | Optional. Filter for news.
$is_kids = true; // bool | Optional. Filter for kids.
$is_sports = true; // bool | Optional. Filter for sports.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$sort_by = "sort_by_example"; // string | Optional. Specify one or more sort orders, comma delimited. Options: Name, StartDate.
$sort_order = "sort_order_example"; // string | Sort Order - Ascending,Descending.
$genres = array("genres_example"); // string[] | The genres to return guide information for.
$genre_ids = array("genre_ids_example"); // string[] | The genre ids to return guide information for.
$enable_images = true; // bool | Optional. Include image information in output.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$enable_user_data = true; // bool | Optional. Include user data.
$series_timer_id = "series_timer_id_example"; // string | Optional. Filter by series timer id.
$library_series_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by library series id.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_total_record_count = true; // bool | Retrieve total record count.

try {
    $result = $apiInstance->getLiveTvPrograms($channel_ids, $user_id, $min_start_date, $has_aired, $is_airing, $max_start_date, $min_end_date, $max_end_date, $is_movie, $is_series, $is_news, $is_kids, $is_sports, $start_index, $limit, $sort_by, $sort_order, $genres, $genre_ids, $enable_images, $image_type_limit, $enable_image_types, $enable_user_data, $series_timer_id, $library_series_id, $fields, $enable_total_record_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getLiveTvPrograms: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_ids** | [**string[]**](../Model/string.md)| The channels to return guide information for. | [optional]
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id. | [optional]
 **min_start_date** | **\DateTime**| Optional. The minimum premiere start date. | [optional]
 **has_aired** | **bool**| Optional. Filter by programs that have completed airing, or not. | [optional]
 **is_airing** | **bool**| Optional. Filter by programs that are currently airing, or not. | [optional]
 **max_start_date** | **\DateTime**| Optional. The maximum premiere start date. | [optional]
 **min_end_date** | **\DateTime**| Optional. The minimum premiere end date. | [optional]
 **max_end_date** | **\DateTime**| Optional. The maximum premiere end date. | [optional]
 **is_movie** | **bool**| Optional. Filter for movies. | [optional]
 **is_series** | **bool**| Optional. Filter for series. | [optional]
 **is_news** | **bool**| Optional. Filter for news. | [optional]
 **is_kids** | **bool**| Optional. Filter for kids. | [optional]
 **is_sports** | **bool**| Optional. Filter for sports. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **sort_by** | **string**| Optional. Specify one or more sort orders, comma delimited. Options: Name, StartDate. | [optional]
 **sort_order** | **string**| Sort Order - Ascending,Descending. | [optional]
 **genres** | [**string[]**](../Model/string.md)| The genres to return guide information for. | [optional]
 **genre_ids** | [**string[]**](../Model/string.md)| The genre ids to return guide information for. | [optional]
 **enable_images** | **bool**| Optional. Include image information in output. | [optional]
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **enable_user_data** | **bool**| Optional. Include user data. | [optional]
 **series_timer_id** | **string**| Optional. Filter by series timer id. | [optional]
 **library_series_id** | [**string**](../Model/.md)| Optional. Filter by library series id. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **enable_total_record_count** | **bool**| Retrieve total record count. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProgram**
> \Swagger\Client\Model\BaseItemDto getProgram($program_id, $user_id)

Gets a live tv program.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$program_id = "program_id_example"; // string | Program id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Attach user data.

try {
    $result = $apiInstance->getProgram($program_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getProgram: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **program_id** | **string**| Program id. |
 **user_id** | [**string**](../Model/.md)| Optional. Attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPrograms**
> \Swagger\Client\Model\BaseItemDtoQueryResult getPrograms($body)

Gets available live tv epgs.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\GetProgramsDto(); // \Swagger\Client\Model\GetProgramsDto | Request body.

try {
    $result = $apiInstance->getPrograms($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getPrograms: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\GetProgramsDto**](../Model/GetProgramsDto.md)| Request body. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecommendedPrograms**
> \Swagger\Client\Model\BaseItemDtoQueryResult getRecommendedPrograms($user_id, $limit, $is_airing, $has_aired, $is_series, $is_movie, $is_news, $is_kids, $is_sports, $enable_images, $image_type_limit, $enable_image_types, $genre_ids, $fields, $enable_user_data, $enable_total_record_count)

Gets recommended live tv epgs.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. filter by user id.
$limit = 56; // int | Optional. The maximum number of records to return.
$is_airing = true; // bool | Optional. Filter by programs that are currently airing, or not.
$has_aired = true; // bool | Optional. Filter by programs that have completed airing, or not.
$is_series = true; // bool | Optional. Filter for series.
$is_movie = true; // bool | Optional. Filter for movies.
$is_news = true; // bool | Optional. Filter for news.
$is_kids = true; // bool | Optional. Filter for kids.
$is_sports = true; // bool | Optional. Filter for sports.
$enable_images = true; // bool | Optional. Include image information in output.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$genre_ids = array("genre_ids_example"); // string[] | The genres to return guide information for.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_user_data = true; // bool | Optional. include user data.
$enable_total_record_count = true; // bool | Retrieve total record count.

try {
    $result = $apiInstance->getRecommendedPrograms($user_id, $limit, $is_airing, $has_aired, $is_series, $is_movie, $is_news, $is_kids, $is_sports, $enable_images, $image_type_limit, $enable_image_types, $genre_ids, $fields, $enable_user_data, $enable_total_record_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getRecommendedPrograms: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| Optional. filter by user id. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **is_airing** | **bool**| Optional. Filter by programs that are currently airing, or not. | [optional]
 **has_aired** | **bool**| Optional. Filter by programs that have completed airing, or not. | [optional]
 **is_series** | **bool**| Optional. Filter for series. | [optional]
 **is_movie** | **bool**| Optional. Filter for movies. | [optional]
 **is_news** | **bool**| Optional. Filter for news. | [optional]
 **is_kids** | **bool**| Optional. Filter for kids. | [optional]
 **is_sports** | **bool**| Optional. Filter for sports. | [optional]
 **enable_images** | **bool**| Optional. Include image information in output. | [optional]
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **genre_ids** | [**string[]**](../Model/string.md)| The genres to return guide information for. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **enable_user_data** | **bool**| Optional. include user data. | [optional]
 **enable_total_record_count** | **bool**| Retrieve total record count. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecording**
> \Swagger\Client\Model\BaseItemDto getRecording($recording_id, $user_id)

Gets a live tv recording.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$recording_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Recording id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Attach user data.

try {
    $result = $apiInstance->getRecording($recording_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getRecording: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_id** | [**string**](../Model/.md)| Recording id. |
 **user_id** | [**string**](../Model/.md)| Optional. Attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecordingFolders**
> \Swagger\Client\Model\BaseItemDtoQueryResult getRecordingFolders($user_id)

Gets recording folders.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user and attach user data.

try {
    $result = $apiInstance->getRecordingFolders($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getRecordingFolders: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user and attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecordingGroup**
> getRecordingGroup($group_id)

Get recording group.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Group id.

try {
    $apiInstance->getRecordingGroup($group_id);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getRecordingGroup: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_id** | [**string**](../Model/.md)| Group id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecordingGroups**
> \Swagger\Client\Model\BaseItemDtoQueryResult getRecordingGroups($user_id)

Gets live tv recording groups.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user and attach user data.

try {
    $result = $apiInstance->getRecordingGroups($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getRecordingGroups: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user and attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecordings**
> \Swagger\Client\Model\BaseItemDtoQueryResult getRecordings($channel_id, $user_id, $start_index, $limit, $status, $is_in_progress, $series_timer_id, $enable_images, $image_type_limit, $enable_image_types, $fields, $enable_user_data, $is_movie, $is_series, $is_kids, $is_sports, $is_news, $is_library_item, $enable_total_record_count)

Gets live tv recordings.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = "channel_id_example"; // string | Optional. Filter by channel id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user and attach user data.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$status = new \Swagger\Client\Model\RecordingStatus(); // \Swagger\Client\Model\RecordingStatus | Optional. Filter by recording status.
$is_in_progress = true; // bool | Optional. Filter by recordings that are in progress, or not.
$series_timer_id = "series_timer_id_example"; // string | Optional. Filter by recordings belonging to a series timer.
$enable_images = true; // bool | Optional. Include image information in output.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_user_data = true; // bool | Optional. Include user data.
$is_movie = true; // bool | Optional. Filter for movies.
$is_series = true; // bool | Optional. Filter for series.
$is_kids = true; // bool | Optional. Filter for kids.
$is_sports = true; // bool | Optional. Filter for sports.
$is_news = true; // bool | Optional. Filter for news.
$is_library_item = true; // bool | Optional. Filter for is library item.
$enable_total_record_count = true; // bool | Optional. Return total record count.

try {
    $result = $apiInstance->getRecordings($channel_id, $user_id, $start_index, $limit, $status, $is_in_progress, $series_timer_id, $enable_images, $image_type_limit, $enable_image_types, $fields, $enable_user_data, $is_movie, $is_series, $is_kids, $is_sports, $is_news, $is_library_item, $enable_total_record_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getRecordings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Optional. Filter by channel id. | [optional]
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user and attach user data. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **status** | [**\Swagger\Client\Model\RecordingStatus**](../Model/.md)| Optional. Filter by recording status. | [optional]
 **is_in_progress** | **bool**| Optional. Filter by recordings that are in progress, or not. | [optional]
 **series_timer_id** | **string**| Optional. Filter by recordings belonging to a series timer. | [optional]
 **enable_images** | **bool**| Optional. Include image information in output. | [optional]
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **enable_user_data** | **bool**| Optional. Include user data. | [optional]
 **is_movie** | **bool**| Optional. Filter for movies. | [optional]
 **is_series** | **bool**| Optional. Filter for series. | [optional]
 **is_kids** | **bool**| Optional. Filter for kids. | [optional]
 **is_sports** | **bool**| Optional. Filter for sports. | [optional]
 **is_news** | **bool**| Optional. Filter for news. | [optional]
 **is_library_item** | **bool**| Optional. Filter for is library item. | [optional]
 **enable_total_record_count** | **bool**| Optional. Return total record count. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRecordingsSeries**
> \Swagger\Client\Model\BaseItemDtoQueryResult getRecordingsSeries($channel_id, $user_id, $group_id, $start_index, $limit, $status, $is_in_progress, $series_timer_id, $enable_images, $image_type_limit, $enable_image_types, $fields, $enable_user_data, $enable_total_record_count)

Gets live tv recording series.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = "channel_id_example"; // string | Optional. Filter by channel id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user and attach user data.
$group_id = "group_id_example"; // string | Optional. Filter by recording group.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$status = new \Swagger\Client\Model\RecordingStatus(); // \Swagger\Client\Model\RecordingStatus | Optional. Filter by recording status.
$is_in_progress = true; // bool | Optional. Filter by recordings that are in progress, or not.
$series_timer_id = "series_timer_id_example"; // string | Optional. Filter by recordings belonging to a series timer.
$enable_images = true; // bool | Optional. Include image information in output.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_user_data = true; // bool | Optional. Include user data.
$enable_total_record_count = true; // bool | Optional. Return total record count.

try {
    $result = $apiInstance->getRecordingsSeries($channel_id, $user_id, $group_id, $start_index, $limit, $status, $is_in_progress, $series_timer_id, $enable_images, $image_type_limit, $enable_image_types, $fields, $enable_user_data, $enable_total_record_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getRecordingsSeries: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Optional. Filter by channel id. | [optional]
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user and attach user data. | [optional]
 **group_id** | **string**| Optional. Filter by recording group. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **status** | [**\Swagger\Client\Model\RecordingStatus**](../Model/.md)| Optional. Filter by recording status. | [optional]
 **is_in_progress** | **bool**| Optional. Filter by recordings that are in progress, or not. | [optional]
 **series_timer_id** | **string**| Optional. Filter by recordings belonging to a series timer. | [optional]
 **enable_images** | **bool**| Optional. Include image information in output. | [optional]
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **enable_user_data** | **bool**| Optional. Include user data. | [optional]
 **enable_total_record_count** | **bool**| Optional. Return total record count. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSchedulesDirectCountries**
> string getSchedulesDirectCountries()

Gets available countries.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getSchedulesDirectCountries();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getSchedulesDirectCountries: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSeriesTimer**
> \Swagger\Client\Model\SeriesTimerInfoDto getSeriesTimer($timer_id)

Gets a live tv series timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$timer_id = "timer_id_example"; // string | Timer id.

try {
    $result = $apiInstance->getSeriesTimer($timer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getSeriesTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **timer_id** | **string**| Timer id. |

### Return type

[**\Swagger\Client\Model\SeriesTimerInfoDto**](../Model/SeriesTimerInfoDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSeriesTimers**
> \Swagger\Client\Model\SeriesTimerInfoDtoQueryResult getSeriesTimers($sort_by, $sort_order)

Gets live tv series timers.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort_by = "sort_by_example"; // string | Optional. Sort by SortName or Priority.
$sort_order = new \Swagger\Client\Model\SortOrder(); // \Swagger\Client\Model\SortOrder | Optional. Sort in Ascending or Descending order.

try {
    $result = $apiInstance->getSeriesTimers($sort_by, $sort_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getSeriesTimers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort_by** | **string**| Optional. Sort by SortName or Priority. | [optional]
 **sort_order** | [**\Swagger\Client\Model\SortOrder**](../Model/.md)| Optional. Sort in Ascending or Descending order. | [optional]

### Return type

[**\Swagger\Client\Model\SeriesTimerInfoDtoQueryResult**](../Model/SeriesTimerInfoDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTimer**
> \Swagger\Client\Model\TimerInfoDto getTimer($timer_id)

Gets a timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$timer_id = "timer_id_example"; // string | Timer id.

try {
    $result = $apiInstance->getTimer($timer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **timer_id** | **string**| Timer id. |

### Return type

[**\Swagger\Client\Model\TimerInfoDto**](../Model/TimerInfoDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTimers**
> \Swagger\Client\Model\TimerInfoDtoQueryResult getTimers($channel_id, $series_timer_id, $is_active, $is_scheduled)

Gets the live tv timers.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = "channel_id_example"; // string | Optional. Filter by channel id.
$series_timer_id = "series_timer_id_example"; // string | Optional. Filter by timers belonging to a series timer.
$is_active = true; // bool | Optional. Filter by timers that are active.
$is_scheduled = true; // bool | Optional. Filter by timers that are scheduled.

try {
    $result = $apiInstance->getTimers($channel_id, $series_timer_id, $is_active, $is_scheduled);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getTimers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Optional. Filter by channel id. | [optional]
 **series_timer_id** | **string**| Optional. Filter by timers belonging to a series timer. | [optional]
 **is_active** | **bool**| Optional. Filter by timers that are active. | [optional]
 **is_scheduled** | **bool**| Optional. Filter by timers that are scheduled. | [optional]

### Return type

[**\Swagger\Client\Model\TimerInfoDtoQueryResult**](../Model/TimerInfoDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTunerHostTypes**
> \Swagger\Client\Model\NameIdPair[] getTunerHostTypes()

Get tuner host types.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getTunerHostTypes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->getTunerHostTypes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\NameIdPair[]**](../Model/NameIdPair.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **resetTuner**
> resetTuner($tuner_id)

Resets a tv tuner.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tuner_id = "tuner_id_example"; // string | Tuner id.

try {
    $apiInstance->resetTuner($tuner_id);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->resetTuner: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tuner_id** | **string**| Tuner id. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setChannelMapping**
> \Swagger\Client\Model\TunerChannelMapping setChannelMapping($body)

Set channel mappings.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\SetChannelMappingDto(); // \Swagger\Client\Model\SetChannelMappingDto | The set channel mapping dto.

try {
    $result = $apiInstance->setChannelMapping($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->setChannelMapping: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\SetChannelMappingDto**](../Model/SetChannelMappingDto.md)| The set channel mapping dto. |

### Return type

[**\Swagger\Client\Model\TunerChannelMapping**](../Model/TunerChannelMapping.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateSeriesTimer**
> updateSeriesTimer($timer_id, $body)

Updates a live tv series timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$timer_id = "timer_id_example"; // string | Timer id.
$body = new \Swagger\Client\Model\SeriesTimerInfoDto(); // \Swagger\Client\Model\SeriesTimerInfoDto | New series timer info.

try {
    $apiInstance->updateSeriesTimer($timer_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->updateSeriesTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **timer_id** | **string**| Timer id. |
 **body** | [**\Swagger\Client\Model\SeriesTimerInfoDto**](../Model/SeriesTimerInfoDto.md)| New series timer info. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateTimer**
> updateTimer($timer_id, $body)

Updates a live tv timer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\LiveTvApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$timer_id = "timer_id_example"; // string | Timer id.
$body = new \Swagger\Client\Model\TimerInfoDto(); // \Swagger\Client\Model\TimerInfoDto | New timer info.

try {
    $apiInstance->updateTimer($timer_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling LiveTvApi->updateTimer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **timer_id** | **string**| Timer id. |
 **body** | [**\Swagger\Client\Model\TimerInfoDto**](../Model/TimerInfoDto.md)| New timer info. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

