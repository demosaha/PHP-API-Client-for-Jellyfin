# Swagger\Client\InstantMixApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getInstantMixFromAlbum**](InstantMixApi.md#getinstantmixfromalbum) | **GET** /Albums/{id}/InstantMix | Creates an instant playlist based on a given song.
[**getInstantMixFromArtists**](InstantMixApi.md#getinstantmixfromartists) | **GET** /Artists/{id}/InstantMix | Creates an instant playlist based on a given song.
[**getInstantMixFromItem**](InstantMixApi.md#getinstantmixfromitem) | **GET** /Items/{id}/InstantMix | Creates an instant playlist based on a given song.
[**getInstantMixFromMusicGenre**](InstantMixApi.md#getinstantmixfrommusicgenre) | **GET** /MusicGenres/{name}/InstantMix | Creates an instant playlist based on a given song.
[**getInstantMixFromMusicGenres**](InstantMixApi.md#getinstantmixfrommusicgenres) | **GET** /MusicGenres/{id}/InstantMix | Creates an instant playlist based on a given song.
[**getInstantMixFromPlaylist**](InstantMixApi.md#getinstantmixfromplaylist) | **GET** /Playlists/{id}/InstantMix | Creates an instant playlist based on a given song.
[**getInstantMixFromSong**](InstantMixApi.md#getinstantmixfromsong) | **GET** /Songs/{id}/InstantMix | Creates an instant playlist based on a given song.

# **getInstantMixFromAlbum**
> \Swagger\Client\Model\BaseItemDtoQueryResult getInstantMixFromAlbum($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Creates an instant playlist based on a given song.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\InstantMixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getInstantMixFromAlbum($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantMixApi->getInstantMixFromAlbum: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| The item id. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
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

# **getInstantMixFromArtists**
> \Swagger\Client\Model\BaseItemDtoQueryResult getInstantMixFromArtists($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Creates an instant playlist based on a given song.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\InstantMixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getInstantMixFromArtists($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantMixApi->getInstantMixFromArtists: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| The item id. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
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

# **getInstantMixFromItem**
> \Swagger\Client\Model\BaseItemDtoQueryResult getInstantMixFromItem($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Creates an instant playlist based on a given song.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\InstantMixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getInstantMixFromItem($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantMixApi->getInstantMixFromItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| The item id. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
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

# **getInstantMixFromMusicGenre**
> \Swagger\Client\Model\BaseItemDtoQueryResult getInstantMixFromMusicGenre($name, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Creates an instant playlist based on a given song.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\InstantMixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | The genre name.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getInstantMixFromMusicGenre($name, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantMixApi->getInstantMixFromMusicGenre: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| The genre name. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
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

# **getInstantMixFromMusicGenres**
> \Swagger\Client\Model\BaseItemDtoQueryResult getInstantMixFromMusicGenres($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Creates an instant playlist based on a given song.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\InstantMixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getInstantMixFromMusicGenres($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantMixApi->getInstantMixFromMusicGenres: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| The item id. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
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

# **getInstantMixFromPlaylist**
> \Swagger\Client\Model\BaseItemDtoQueryResult getInstantMixFromPlaylist($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Creates an instant playlist based on a given song.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\InstantMixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getInstantMixFromPlaylist($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantMixApi->getInstantMixFromPlaylist: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| The item id. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
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

# **getInstantMixFromSong**
> \Swagger\Client\Model\BaseItemDtoQueryResult getInstantMixFromSong($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types)

Creates an instant playlist based on a given song.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\InstantMixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The item id.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.
$limit = 56; // int | Optional. The maximum number of records to return.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$enable_images = true; // bool | Optional. Include image information in output.
$enable_user_data = true; // bool | Optional. Include user data.
$image_type_limit = 56; // int | Optional. The max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.

try {
    $result = $apiInstance->getInstantMixFromSong($id, $user_id, $limit, $fields, $enable_images, $enable_user_data, $image_type_limit, $enable_image_types);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstantMixApi->getInstantMixFromSong: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| The item id. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]
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

