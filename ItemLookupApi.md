# Swagger\Client\ItemLookupApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**applySearchCriteria**](ItemLookupApi.md#applysearchcriteria) | **POST** /Items/RemoteSearch/Apply/{itemId} | Applies search criteria to an item and refreshes metadata.
[**getBookRemoteSearchResults**](ItemLookupApi.md#getbookremotesearchresults) | **POST** /Items/RemoteSearch/Book | Get book remote search.
[**getBoxSetRemoteSearchResults**](ItemLookupApi.md#getboxsetremotesearchresults) | **POST** /Items/RemoteSearch/BoxSet | Get box set remote search.
[**getExternalIdInfos**](ItemLookupApi.md#getexternalidinfos) | **GET** /Items/{itemId}/ExternalIdInfos | Get the item&#x27;s external id info.
[**getMovieRemoteSearchResults**](ItemLookupApi.md#getmovieremotesearchresults) | **POST** /Items/RemoteSearch/Movie | Get movie remote search.
[**getMusicAlbumRemoteSearchResults**](ItemLookupApi.md#getmusicalbumremotesearchresults) | **POST** /Items/RemoteSearch/MusicAlbum | Get music album remote search.
[**getMusicArtistRemoteSearchResults**](ItemLookupApi.md#getmusicartistremotesearchresults) | **POST** /Items/RemoteSearch/MusicArtist | Get music artist remote search.
[**getMusicVideoRemoteSearchResults**](ItemLookupApi.md#getmusicvideoremotesearchresults) | **POST** /Items/RemoteSearch/MusicVideo | Get music video remote search.
[**getPersonRemoteSearchResults**](ItemLookupApi.md#getpersonremotesearchresults) | **POST** /Items/RemoteSearch/Person | Get person remote search.
[**getRemoteSearchImage**](ItemLookupApi.md#getremotesearchimage) | **GET** /Items/RemoteSearch/Image | Gets a remote image.
[**getSeriesRemoteSearchResults**](ItemLookupApi.md#getseriesremotesearchresults) | **POST** /Items/RemoteSearch/Series | Get series remote search.
[**getTrailerRemoteSearchResults**](ItemLookupApi.md#gettrailerremotesearchresults) | **POST** /Items/RemoteSearch/Trailer | Get trailer remote search.

# **applySearchCriteria**
> applySearchCriteria($body, $item_id, $replace_all_images)

Applies search criteria to an item and refreshes metadata.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\RemoteSearchResult(); // \Swagger\Client\Model\RemoteSearchResult | The remote search result.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$replace_all_images = true; // bool | Optional. Whether or not to replace all images. Default: True.

try {
    $apiInstance->applySearchCriteria($body, $item_id, $replace_all_images);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->applySearchCriteria: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\RemoteSearchResult**](../Model/RemoteSearchResult.md)| The remote search result. |
 **item_id** | [**string**](../Model/.md)| Item id. |
 **replace_all_images** | **bool**| Optional. Whether or not to replace all images. Default: True. | [optional] [default to true]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBookRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getBookRemoteSearchResults($body)

Get book remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\BookInfoRemoteSearchQuery(); // \Swagger\Client\Model\BookInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getBookRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getBookRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\BookInfoRemoteSearchQuery**](../Model/BookInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBoxSetRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getBoxSetRemoteSearchResults($body)

Get box set remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\BoxSetInfoRemoteSearchQuery(); // \Swagger\Client\Model\BoxSetInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getBoxSetRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getBoxSetRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\BoxSetInfoRemoteSearchQuery**](../Model/BoxSetInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getExternalIdInfos**
> \Swagger\Client\Model\ExternalIdInfo[] getExternalIdInfos($item_id)

Get the item's external id info.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->getExternalIdInfos($item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getExternalIdInfos: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |

### Return type

[**\Swagger\Client\Model\ExternalIdInfo[]**](../Model/ExternalIdInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMovieRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getMovieRemoteSearchResults($body)

Get movie remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\MovieInfoRemoteSearchQuery(); // \Swagger\Client\Model\MovieInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getMovieRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getMovieRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\MovieInfoRemoteSearchQuery**](../Model/MovieInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMusicAlbumRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getMusicAlbumRemoteSearchResults($body)

Get music album remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\AlbumInfoRemoteSearchQuery(); // \Swagger\Client\Model\AlbumInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getMusicAlbumRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getMusicAlbumRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\AlbumInfoRemoteSearchQuery**](../Model/AlbumInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMusicArtistRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getMusicArtistRemoteSearchResults($body)

Get music artist remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ArtistInfoRemoteSearchQuery(); // \Swagger\Client\Model\ArtistInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getMusicArtistRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getMusicArtistRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\ArtistInfoRemoteSearchQuery**](../Model/ArtistInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMusicVideoRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getMusicVideoRemoteSearchResults($body)

Get music video remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\MusicVideoInfoRemoteSearchQuery(); // \Swagger\Client\Model\MusicVideoInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getMusicVideoRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getMusicVideoRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\MusicVideoInfoRemoteSearchQuery**](../Model/MusicVideoInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPersonRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getPersonRemoteSearchResults($body)

Get person remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PersonLookupInfoRemoteSearchQuery(); // \Swagger\Client\Model\PersonLookupInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getPersonRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getPersonRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PersonLookupInfoRemoteSearchQuery**](../Model/PersonLookupInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRemoteSearchImage**
> string getRemoteSearchImage($image_url, $provider_name)

Gets a remote image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = "image_url_example"; // string | The image url.
$provider_name = "provider_name_example"; // string | The provider name.

try {
    $result = $apiInstance->getRemoteSearchImage($image_url, $provider_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getRemoteSearchImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **image_url** | **string**| The image url. |
 **provider_name** | **string**| The provider name. |

### Return type

**string**

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSeriesRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getSeriesRemoteSearchResults($body)

Get series remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\SeriesInfoRemoteSearchQuery(); // \Swagger\Client\Model\SeriesInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getSeriesRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getSeriesRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\SeriesInfoRemoteSearchQuery**](../Model/SeriesInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTrailerRemoteSearchResults**
> \Swagger\Client\Model\RemoteSearchResult[] getTrailerRemoteSearchResults($body)

Get trailer remote search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ItemLookupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TrailerInfoRemoteSearchQuery(); // \Swagger\Client\Model\TrailerInfoRemoteSearchQuery | Remote search query.

try {
    $result = $apiInstance->getTrailerRemoteSearchResults($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemLookupApi->getTrailerRemoteSearchResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TrailerInfoRemoteSearchQuery**](../Model/TrailerInfoRemoteSearchQuery.md)| Remote search query. |

### Return type

[**\Swagger\Client\Model\RemoteSearchResult[]**](../Model/RemoteSearchResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

