# Swagger\Client\PlaylistsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addToPlaylist**](PlaylistsApi.md#addtoplaylist) | **POST** /Playlists/{playlistId}/Items | Adds items to a playlist.
[**createPlaylist**](PlaylistsApi.md#createplaylist) | **POST** /Playlists | Creates a new playlist.
[**getPlaylistItems**](PlaylistsApi.md#getplaylistitems) | **GET** /Playlists/{playlistId}/Items | Gets the original items of a playlist.
[**moveItem**](PlaylistsApi.md#moveitem) | **POST** /Playlists/{playlistId}/Items/{itemId}/Move/{newIndex} | Moves a playlist item.
[**removeFromPlaylist**](PlaylistsApi.md#removefromplaylist) | **DELETE** /Playlists/{playlistId}/Items | Removes items from a playlist.

# **addToPlaylist**
> addToPlaylist($playlist_id, $ids, $user_id)

Adds items to a playlist.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaylistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$playlist_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The playlist id.
$ids = array("ids_example"); // string[] | Item id, comma delimited.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The userId.

try {
    $apiInstance->addToPlaylist($playlist_id, $ids, $user_id);
} catch (Exception $e) {
    echo 'Exception when calling PlaylistsApi->addToPlaylist: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playlist_id** | [**string**](../Model/.md)| The playlist id. |
 **ids** | [**string[]**](../Model/string.md)| Item id, comma delimited. | [optional]
 **user_id** | [**string**](../Model/.md)| The userId. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createPlaylist**
> \Swagger\Client\Model\PlaylistCreationResult createPlaylist($body, $name, $ids, $user_id, $media_type)

Creates a new playlist.

For backwards compatibility parameters can be sent via Query or Body, with Query having higher precedence.  Query parameters are obsolete.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaylistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CreatePlaylistDto(); // \Swagger\Client\Model\CreatePlaylistDto | The create playlist payload.
$name = "name_example"; // string | The playlist name.
$ids = array("ids_example"); // string[] | The item ids.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The user id.
$media_type = "media_type_example"; // string | The media type.

try {
    $result = $apiInstance->createPlaylist($body, $name, $ids, $user_id, $media_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlaylistsApi->createPlaylist: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CreatePlaylistDto**](../Model/CreatePlaylistDto.md)| The create playlist payload. | [optional]
 **name** | **string**| The playlist name. | [optional]
 **ids** | [**string[]**](../Model/string.md)| The item ids. | [optional]
 **user_id** | [**string**](../Model/.md)| The user id. | [optional]
 **media_type** | **string**| The media type. | [optional]

### Return type

[**\Swagger\Client\Model\PlaylistCreationResult**](../Model/PlaylistCreationResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPlaylistItems**
> \Swagger\Client\Model\BaseItemDtoQueryResult getPlaylistItems($playlist_id, $user_id, $start_index, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Gets the original items of a playlist.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaylistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$playlist_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The playlist id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getPlaylistItems($playlist_id, $user_id, $start_index, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlaylistsApi->getPlaylistItems: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playlist_id** | [**string**](../Model/.md)| The playlist id. |
 **user_id** | [**string**](../Model/.md)| User id. |
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **enable_images** | **bool**| Optional. Include image information in output. | [optional]
 **enable_user_data** | **bool**| Optional. Include user data. | [optional]
 **image_type_limit** | **int**| Optional. The max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **moveItem**
> moveItem($playlist_id, $item_id, $new_index)

Moves a playlist item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaylistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$playlist_id = "playlist_id_example"; // string | The playlist id.
$item_id = "item_id_example"; // string | The item id.
$new_index = 56; // int | The new index.

try {
    $apiInstance->moveItem($playlist_id, $item_id, $new_index);
} catch (Exception $e) {
    echo 'Exception when calling PlaylistsApi->moveItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playlist_id** | **string**| The playlist id. |
 **item_id** | **string**| The item id. |
 **new_index** | **int**| The new index. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeFromPlaylist**
> removeFromPlaylist($playlist_id, $entry_ids)

Removes items from a playlist.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PlaylistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$playlist_id = "playlist_id_example"; // string | The playlist id.
$entry_ids = array("entry_ids_example"); // string[] | The item ids, comma delimited.

try {
    $apiInstance->removeFromPlaylist($playlist_id, $entry_ids);
} catch (Exception $e) {
    echo 'Exception when calling PlaylistsApi->removeFromPlaylist: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playlist_id** | **string**| The playlist id. |
 **entry_ids** | [**string[]**](../Model/string.md)| The item ids, comma delimited. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

