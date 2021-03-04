# Swagger\Client\SearchApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](SearchApi.md#get) | **GET** /Search/Hints | Gets the search hint result.

# **get**
> \Swagger\Client\Model\SearchHintResult get($search_term, $start_index, $limit, $user_id, $include_item_types, $exclude_item_types, $media_types, $parent_id, $is_movie, $is_series, $is_news, $is_kids, $is_sports, $include_people, $include_media, $include_genres, $include_studios, $include_artists)

Gets the search hint result.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$search_term = "search_term_example"; // string | The search term to filter on.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Supply a user id to search within a user's library or omit to search all.
$include_item_types = array("include_item_types_example"); // string[] | If specified, only results with the specified item types are returned. This allows multiple, comma delimeted.
$exclude_item_types = array("exclude_item_types_example"); // string[] | If specified, results with these item types are filtered out. This allows multiple, comma delimeted.
$media_types = array("media_types_example"); // string[] | If specified, only results with the specified media types are returned. This allows multiple, comma delimeted.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | If specified, only children of the parent are returned.
$is_movie = true; // bool | Optional filter for movies.
$is_series = true; // bool | Optional filter for series.
$is_news = true; // bool | Optional filter for news.
$is_kids = true; // bool | Optional filter for kids.
$is_sports = true; // bool | Optional filter for sports.
$include_people = true; // bool | Optional filter whether to include people.
$include_media = true; // bool | Optional filter whether to include media.
$include_genres = true; // bool | Optional filter whether to include genres.
$include_studios = true; // bool | Optional filter whether to include studios.
$include_artists = true; // bool | Optional filter whether to include artists.

try {
    $result = $apiInstance->get($search_term, $start_index, $limit, $user_id, $include_item_types, $exclude_item_types, $media_types, $parent_id, $is_movie, $is_series, $is_news, $is_kids, $is_sports, $include_people, $include_media, $include_genres, $include_studios, $include_artists);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search_term** | **string**| The search term to filter on. |
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **user_id** | [**string**](../Model/.md)| Optional. Supply a user id to search within a user&#x27;s library or omit to search all. | [optional]
 **include_item_types** | [**string[]**](../Model/string.md)| If specified, only results with the specified item types are returned. This allows multiple, comma delimeted. | [optional]
 **exclude_item_types** | [**string[]**](../Model/string.md)| If specified, results with these item types are filtered out. This allows multiple, comma delimeted. | [optional]
 **media_types** | [**string[]**](../Model/string.md)| If specified, only results with the specified media types are returned. This allows multiple, comma delimeted. | [optional]
 **parent_id** | [**string**](../Model/.md)| If specified, only children of the parent are returned. | [optional]
 **is_movie** | **bool**| Optional filter for movies. | [optional]
 **is_series** | **bool**| Optional filter for series. | [optional]
 **is_news** | **bool**| Optional filter for news. | [optional]
 **is_kids** | **bool**| Optional filter for kids. | [optional]
 **is_sports** | **bool**| Optional filter for sports. | [optional]
 **include_people** | **bool**| Optional filter whether to include people. | [optional] [default to true]
 **include_media** | **bool**| Optional filter whether to include media. | [optional] [default to true]
 **include_genres** | **bool**| Optional filter whether to include genres. | [optional] [default to true]
 **include_studios** | **bool**| Optional filter whether to include studios. | [optional] [default to true]
 **include_artists** | **bool**| Optional filter whether to include artists. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\SearchHintResult**](../Model/SearchHintResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

