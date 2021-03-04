# Swagger\Client\ImageApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteItemImage**](ImageApi.md#deleteitemimage) | **DELETE** /Items/{itemId}/Images/{imageType} | Delete an item&#x27;s image.
[**deleteItemImageByIndex**](ImageApi.md#deleteitemimagebyindex) | **DELETE** /Items/{itemId}/Images/{imageType}/{imageIndex} | Delete an item&#x27;s image.
[**deleteUserImage**](ImageApi.md#deleteuserimage) | **DELETE** /Users/{userId}/Images/{imageType} | Delete the user&#x27;s image.
[**deleteUserImageByIndex**](ImageApi.md#deleteuserimagebyindex) | **DELETE** /Users/{userId}/Images/{imageType}/{index} | Delete the user&#x27;s image.
[**getArtistImage**](ImageApi.md#getartistimage) | **GET** /Artists/{name}/Images/{imageType}/{imageIndex} | Get artist image by name.
[**getGenreImage**](ImageApi.md#getgenreimage) | **GET** /Genres/{name}/Images/{imageType} | Get genre image by name.
[**getGenreImageByIndex**](ImageApi.md#getgenreimagebyindex) | **GET** /Genres/{name}/Images/{imageType}/{imageIndex} | Get genre image by name.
[**getItemImage**](ImageApi.md#getitemimage) | **GET** /Items/{itemId}/Images/{imageType} | Gets the item&#x27;s image.
[**getItemImage2**](ImageApi.md#getitemimage2) | **GET** /Items/{itemId}/Images/{imageType}/{imageIndex}/{tag}/{format}/{maxWidth}/{maxHeight}/{percentPlayed}/{unplayedCount} | Gets the item&#x27;s image.
[**getItemImageByIndex**](ImageApi.md#getitemimagebyindex) | **GET** /Items/{itemId}/Images/{imageType}/{imageIndex} | Gets the item&#x27;s image.
[**getItemImageInfos**](ImageApi.md#getitemimageinfos) | **GET** /Items/{itemId}/Images | Get item image infos.
[**getMusicGenreImage**](ImageApi.md#getmusicgenreimage) | **GET** /MusicGenres/{name}/Images/{imageType} | Get music genre image by name.
[**getMusicGenreImageByIndex**](ImageApi.md#getmusicgenreimagebyindex) | **GET** /MusicGenres/{name}/Images/{imageType}/{imageIndex} | Get music genre image by name.
[**getPersonImage**](ImageApi.md#getpersonimage) | **GET** /Persons/{name}/Images/{imageType} | Get person image by name.
[**getPersonImageByIndex**](ImageApi.md#getpersonimagebyindex) | **GET** /Persons/{name}/Images/{imageType}/{imageIndex} | Get person image by name.
[**getStudioImage**](ImageApi.md#getstudioimage) | **GET** /Studios/{name}/Images/{imageType} | Get studio image by name.
[**getStudioImageByIndex**](ImageApi.md#getstudioimagebyindex) | **GET** /Studios/{name}/Images/{imageType}/{imageIndex} | Get studio image by name.
[**getUserImage**](ImageApi.md#getuserimage) | **GET** /Users/{userId}/Images/{imageType} | Get user profile image.
[**getUserImageByIndex**](ImageApi.md#getuserimagebyindex) | **GET** /Users/{userId}/Images/{imageType}/{imageIndex} | Get user profile image.
[**headArtistImage**](ImageApi.md#headartistimage) | **HEAD** /Artists/{name}/Images/{imageType}/{imageIndex} | Get artist image by name.
[**headGenreImage**](ImageApi.md#headgenreimage) | **HEAD** /Genres/{name}/Images/{imageType} | Get genre image by name.
[**headGenreImageByIndex**](ImageApi.md#headgenreimagebyindex) | **HEAD** /Genres/{name}/Images/{imageType}/{imageIndex} | Get genre image by name.
[**headItemImage**](ImageApi.md#headitemimage) | **HEAD** /Items/{itemId}/Images/{imageType} | Gets the item&#x27;s image.
[**headItemImage2**](ImageApi.md#headitemimage2) | **HEAD** /Items/{itemId}/Images/{imageType}/{imageIndex}/{tag}/{format}/{maxWidth}/{maxHeight}/{percentPlayed}/{unplayedCount} | Gets the item&#x27;s image.
[**headItemImageByIndex**](ImageApi.md#headitemimagebyindex) | **HEAD** /Items/{itemId}/Images/{imageType}/{imageIndex} | Gets the item&#x27;s image.
[**headMusicGenreImage**](ImageApi.md#headmusicgenreimage) | **HEAD** /MusicGenres/{name}/Images/{imageType} | Get music genre image by name.
[**headMusicGenreImageByIndex**](ImageApi.md#headmusicgenreimagebyindex) | **HEAD** /MusicGenres/{name}/Images/{imageType}/{imageIndex} | Get music genre image by name.
[**headPersonImage**](ImageApi.md#headpersonimage) | **HEAD** /Persons/{name}/Images/{imageType} | Get person image by name.
[**headPersonImageByIndex**](ImageApi.md#headpersonimagebyindex) | **HEAD** /Persons/{name}/Images/{imageType}/{imageIndex} | Get person image by name.
[**headStudioImage**](ImageApi.md#headstudioimage) | **HEAD** /Studios/{name}/Images/{imageType} | Get studio image by name.
[**headStudioImageByIndex**](ImageApi.md#headstudioimagebyindex) | **HEAD** /Studios/{name}/Images/{imageType}/{imageIndex} | Get studio image by name.
[**headUserImage**](ImageApi.md#headuserimage) | **HEAD** /Users/{userId}/Images/{imageType} | Get user profile image.
[**headUserImageByIndex**](ImageApi.md#headuserimagebyindex) | **HEAD** /Users/{userId}/Images/{imageType}/{imageIndex} | Get user profile image.
[**postUserImage**](ImageApi.md#postuserimage) | **POST** /Users/{userId}/Images/{imageType} | Sets the user image.
[**postUserImageByIndex**](ImageApi.md#postuserimagebyindex) | **POST** /Users/{userId}/Images/{imageType}/{index} | Sets the user image.
[**setItemImage**](ImageApi.md#setitemimage) | **POST** /Items/{itemId}/Images/{imageType} | Set item image.
[**setItemImageByIndex**](ImageApi.md#setitemimagebyindex) | **POST** /Items/{itemId}/Images/{imageType}/{imageIndex} | Set item image.
[**updateItemImageIndex**](ImageApi.md#updateitemimageindex) | **POST** /Items/{itemId}/Images/{imageType}/{imageIndex}/Index | Updates the index for an item image.

# **deleteItemImage**
> deleteItemImage($item_id, $image_type, $image_index)

Delete an item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | The image index.

try {
    $apiInstance->deleteItemImage($item_id, $image_type, $image_index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->deleteItemImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| The image index. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteItemImageByIndex**
> deleteItemImageByIndex($item_id, $image_type, $image_index)

Delete an item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | The image index.

try {
    $apiInstance->deleteItemImageByIndex($item_id, $image_type, $image_index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->deleteItemImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| The image index. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteUserImage**
> deleteUserImage($user_id, $image_type, $index)

Delete the user's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User Id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | (Unused) Image type.
$index = 56; // int | (Unused) Image index.

try {
    $apiInstance->deleteUserImage($user_id, $image_type, $index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->deleteUserImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User Id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| (Unused) Image type. |
 **index** | **int**| (Unused) Image index. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteUserImageByIndex**
> deleteUserImageByIndex($user_id, $image_type, $index)

Delete the user's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User Id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | (Unused) Image type.
$index = 56; // int | (Unused) Image index.

try {
    $apiInstance->deleteUserImageByIndex($user_id, $image_type, $index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->deleteUserImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User Id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| (Unused) Image type. |
 **index** | **int**| (Unused) Image index. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getArtistImage**
> string getArtistImage($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get artist image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Artist name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getArtistImage($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getArtistImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Artist name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getGenreImage**
> string getGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->getGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getGenreImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getGenreImageByIndex**
> string getGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getGenreImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getItemImage**
> string getItemImage($item_id, $image_type, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer, $image_index)

Gets the item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->getItemImage($item_id, $image_type, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getItemImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getItemImage2**
> string getItemImage2($item_id, $image_type, $max_width, $max_height, $tag, $format, $percent_played, $unplayed_count, $image_index, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Gets the item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$image_index = 56; // int | Image index.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getItemImage2($item_id, $image_type, $max_width, $max_height, $tag, $format, $percent_played, $unplayed_count, $image_index, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getItemImage2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **max_width** | **int**| The maximum image width to return. |
 **max_height** | **int**| The maximum image height to return. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. |
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. |
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. |
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. |
 **image_index** | **int**| Image index. |
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getItemImageByIndex**
> string getItemImageByIndex($item_id, $image_type, $image_index, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer)

Gets the item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getItemImageByIndex($item_id, $image_type, $image_index, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getItemImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getItemImageInfos**
> \Swagger\Client\Model\ImageInfo[] getItemImageInfos($item_id)

Get item image infos.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->getItemImageInfos($item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getItemImageInfos: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |

### Return type

[**\Swagger\Client\Model\ImageInfo[]**](../Model/ImageInfo.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMusicGenreImage**
> string getMusicGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get music genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Music genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->getMusicGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getMusicGenreImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Music genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMusicGenreImageByIndex**
> string getMusicGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get music genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Music genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getMusicGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getMusicGenreImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Music genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPersonImage**
> string getPersonImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get person image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Person name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->getPersonImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getPersonImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Person name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPersonImageByIndex**
> string getPersonImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get person image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Person name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getPersonImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getPersonImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Person name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getStudioImage**
> string getStudioImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get studio image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Studio name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->getStudioImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getStudioImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Studio name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getStudioImageByIndex**
> string getStudioImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get studio image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Studio name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getStudioImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getStudioImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Studio name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserImage**
> string getUserImage($user_id, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get user profile image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->getUserImage($user_id, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getUserImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserImageByIndex**
> string getUserImageByIndex($user_id, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get user profile image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->getUserImageByIndex($user_id, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->getUserImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headArtistImage**
> string headArtistImage($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get artist image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Artist name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headArtistImage($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headArtistImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Artist name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headGenreImage**
> string headGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->headGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headGenreImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headGenreImageByIndex**
> string headGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headGenreImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headItemImage**
> string headItemImage($item_id, $image_type, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer, $image_index)

Gets the item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->headItemImage($item_id, $image_type, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headItemImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headItemImage2**
> string headItemImage2($item_id, $image_type, $max_width, $max_height, $tag, $format, $percent_played, $unplayed_count, $image_index, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Gets the item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$image_index = 56; // int | Image index.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headItemImage2($item_id, $image_type, $max_width, $max_height, $tag, $format, $percent_played, $unplayed_count, $image_index, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headItemImage2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **max_width** | **int**| The maximum image width to return. |
 **max_height** | **int**| The maximum image height to return. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. |
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. |
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. |
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. |
 **image_index** | **int**| Image index. |
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headItemImageByIndex**
> string headItemImageByIndex($item_id, $image_type, $image_index, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer)

Gets the item's image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headItemImageByIndex($item_id, $image_type, $image_index, $max_width, $max_height, $width, $height, $quality, $tag, $crop_whitespace, $format, $add_played_indicator, $percent_played, $unplayed_count, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headItemImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Optional. The MediaBrowser.Model.Drawing.ImageFormat of the returned image. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headMusicGenreImage**
> string headMusicGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get music genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Music genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->headMusicGenreImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headMusicGenreImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Music genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headMusicGenreImageByIndex**
> string headMusicGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get music genre image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Music genre name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headMusicGenreImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headMusicGenreImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Music genre name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headPersonImage**
> string headPersonImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get person image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Person name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->headPersonImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headPersonImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Person name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headPersonImageByIndex**
> string headPersonImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get person image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Person name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headPersonImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headPersonImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Person name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headStudioImage**
> string headStudioImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get studio image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Studio name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->headStudioImage($name, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headStudioImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Studio name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headStudioImageByIndex**
> string headStudioImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get studio image by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$name = "name_example"; // string | Studio name.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headStudioImageByIndex($name, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headStudioImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Studio name. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headUserImage**
> string headUserImage($user_id, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index)

Get user profile image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.
$image_index = 56; // int | Image index.

try {
    $result = $apiInstance->headUserImage($user_id, $image_type, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer, $image_index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headUserImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]
 **image_index** | **int**| Image index. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **headUserImageByIndex**
> string headUserImageByIndex($user_id, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer)

Get user profile image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Image index.
$tag = "tag_example"; // string | Optional. Supply the cache tag from the item object to receive strong caching headers.
$format = new \Swagger\Client\Model\ImageFormat(); // \Swagger\Client\Model\ImageFormat | Determines the output format of the image - original,gif,jpg,png.
$max_width = 56; // int | The maximum image width to return.
$max_height = 56; // int | The maximum image height to return.
$percent_played = 1.2; // double | Optional. Percent to render for the percent played overlay.
$unplayed_count = 56; // int | Optional. Unplayed count overlay to render.
$width = 56; // int | The fixed image width to return.
$height = 56; // int | The fixed image height to return.
$quality = 56; // int | Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases.
$crop_whitespace = true; // bool | Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art.
$add_played_indicator = true; // bool | Optional. Add a played indicator.
$blur = 56; // int | Optional. Blur image.
$background_color = "background_color_example"; // string | Optional. Apply a background color for transparent images.
$foreground_layer = "foreground_layer_example"; // string | Optional. Apply a foreground layer on top of the image.

try {
    $result = $apiInstance->headUserImageByIndex($user_id, $image_type, $image_index, $tag, $format, $max_width, $max_height, $percent_played, $unplayed_count, $width, $height, $quality, $crop_whitespace, $add_played_indicator, $blur, $background_color, $foreground_layer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->headUserImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Image index. |
 **tag** | **string**| Optional. Supply the cache tag from the item object to receive strong caching headers. | [optional]
 **format** | [**\Swagger\Client\Model\ImageFormat**](../Model/.md)| Determines the output format of the image - original,gif,jpg,png. | [optional]
 **max_width** | **int**| The maximum image width to return. | [optional]
 **max_height** | **int**| The maximum image height to return. | [optional]
 **percent_played** | **double**| Optional. Percent to render for the percent played overlay. | [optional]
 **unplayed_count** | **int**| Optional. Unplayed count overlay to render. | [optional]
 **width** | **int**| The fixed image width to return. | [optional]
 **height** | **int**| The fixed image height to return. | [optional]
 **quality** | **int**| Optional. Quality setting, from 0-100. Defaults to 90 and should suffice in most cases. | [optional]
 **crop_whitespace** | **bool**| Optional. Specify if whitespace should be cropped out of the image. True/False. If unspecified, whitespace will be cropped from logos and clear art. | [optional]
 **add_played_indicator** | **bool**| Optional. Add a played indicator. | [optional]
 **blur** | **int**| Optional. Blur image. | [optional]
 **background_color** | **string**| Optional. Apply a background color for transparent images. | [optional]
 **foreground_layer** | **string**| Optional. Apply a foreground layer on top of the image. | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/_*, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUserImage**
> postUserImage($user_id, $image_type, $index)

Sets the user image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User Id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | (Unused) Image type.
$index = 56; // int | (Unused) Image index.

try {
    $apiInstance->postUserImage($user_id, $image_type, $index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->postUserImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User Id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| (Unused) Image type. |
 **index** | **int**| (Unused) Image index. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUserImageByIndex**
> postUserImageByIndex($user_id, $image_type, $index)

Sets the user image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User Id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | (Unused) Image type.
$index = 56; // int | (Unused) Image index.

try {
    $apiInstance->postUserImageByIndex($user_id, $image_type, $index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->postUserImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User Id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| (Unused) Image type. |
 **index** | **int**| (Unused) Image index. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setItemImage**
> setItemImage($item_id, $image_type)

Set item image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.

try {
    $apiInstance->setItemImage($item_id, $image_type);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->setItemImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setItemImageByIndex**
> setItemImageByIndex($item_id, $image_type, $image_index)

Set item image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | (Unused) Image index.

try {
    $apiInstance->setItemImageByIndex($item_id, $image_type, $image_index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->setItemImageByIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| (Unused) Image index. |

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateItemImageIndex**
> updateItemImageIndex($item_id, $image_type, $image_index, $new_index)

Updates the index for an item image.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$image_type = new \Swagger\Client\Model\ImageType(); // \Swagger\Client\Model\ImageType | Image type.
$image_index = 56; // int | Old image index.
$new_index = 56; // int | New image index.

try {
    $apiInstance->updateItemImageIndex($item_id, $image_type, $image_index, $new_index);
} catch (Exception $e) {
    echo 'Exception when calling ImageApi->updateItemImageIndex: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item_id** | [**string**](../Model/.md)| Item id. |
 **image_type** | [**\Swagger\Client\Model\ImageType**](../Model/.md)| Image type. |
 **image_index** | **int**| Old image index. |
 **new_index** | **int**| New image index. | [optional]

### Return type

void (empty response body)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

