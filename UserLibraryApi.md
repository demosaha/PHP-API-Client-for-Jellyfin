# Swagger\Client\UserLibraryApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteUserItemRating**](UserLibraryApi.md#deleteuseritemrating) | **DELETE** /Users/{userId}/Items/{itemId}/Rating | Deletes a user&#x27;s saved personal rating for an item.
[**getIntros**](UserLibraryApi.md#getintros) | **GET** /Users/{userId}/Items/{itemId}/Intros | Gets intros to play before the main media item plays.
[**getItem**](UserLibraryApi.md#getitem) | **GET** /Users/{userId}/Items/{itemId} | Gets an item from a user&#x27;s library.
[**getLatestMedia**](UserLibraryApi.md#getlatestmedia) | **GET** /Users/{userId}/Items/Latest | Gets latest media.
[**getLocalTrailers**](UserLibraryApi.md#getlocaltrailers) | **GET** /Users/{userId}/Items/{itemId}/LocalTrailers | Gets local trailers for an item.
[**getRootFolder**](UserLibraryApi.md#getrootfolder) | **GET** /Users/{userId}/Items/Root | Gets the root folder from a user&#x27;s library.
[**getSpecialFeatures**](UserLibraryApi.md#getspecialfeatures) | **GET** /Users/{userId}/Items/{itemId}/SpecialFeatures | Gets special features for an item.
[**markFavoriteItem**](UserLibraryApi.md#markfavoriteitem) | **POST** /Users/{userId}/FavoriteItems/{itemId} | Marks an item as a favorite.
[**unmarkFavoriteItem**](UserLibraryApi.md#unmarkfavoriteitem) | **DELETE** /Users/{userId}/FavoriteItems/{itemId} | Unmarks item as a favorite.
[**updateUserItemRating**](UserLibraryApi.md#updateuseritemrating) | **POST** /Users/{userId}/Items/{itemId}/Rating | Updates a user&#x27;s rating for an item.

# **deleteUserItemRating**
> \Swagger\Client\Model\UserItemDataDto deleteUserItemRating($user_id, $item_id)

Deletes a user's saved personal rating for an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->deleteUserItemRating($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->deleteUserItemRating: ', $e->getMessage(), PHP_EOL;
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

# **getIntros**
> \Swagger\Client\Model\BaseItemDtoQueryResult getIntros($user_id, $item_id)

Gets intros to play before the main media item plays.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->getIntros($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->getIntros: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getItem**
> \Swagger\Client\Model\BaseItemDto getItem($user_id, $item_id)

Gets an item from a user's library.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->getItem($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->getItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLatestMedia**
> \Swagger\Client\Model\BaseItemDto[] getLatestMedia($user_id, $parent_id, $fields, $include_item_types, $is_played, $enable_images, $image_type_limit, $enable_image_types, $enable_user_data, $limit, $group_items)

Gets latest media.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Specify this to localize the search to a specific item or folder. Omit to use the root.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$include_item_types = array("include_item_types_example"); // string[] | Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited.
$is_played = true; // bool | Filter by items that are played, or not.
$enable_images = true; // bool | Optional. include image information in output.
$image_type_limit = 56; // int | Optional. the max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$enable_user_data = true; // bool | Optional. include user data.
$limit = 20; // int | Return item limit.
$group_items = true; // bool | Whether or not to group items into a parent container.

try {
    $result = $apiInstance->getLatestMedia($user_id, $parent_id, $fields, $include_item_types, $is_played, $enable_images, $image_type_limit, $enable_image_types, $enable_user_data, $limit, $group_items);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->getLatestMedia: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **parent_id** | [**string**](../Model/.md)| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **include_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited. | [optional]
 **is_played** | **bool**| Filter by items that are played, or not. | [optional]
 **enable_images** | **bool**| Optional. include image information in output. | [optional]
 **image_type_limit** | **int**| Optional. the max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **enable_user_data** | **bool**| Optional. include user data. | [optional]
 **limit** | **int**| Return item limit. | [optional] [default to 20]
 **group_items** | **bool**| Whether or not to group items into a parent container. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDto[]**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLocalTrailers**
> \Swagger\Client\Model\BaseItemDto[] getLocalTrailers($user_id, $item_id)

Gets local trailers for an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->getLocalTrailers($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->getLocalTrailers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |

### Return type

[**\Swagger\Client\Model\BaseItemDto[]**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRootFolder**
> \Swagger\Client\Model\BaseItemDto getRootFolder($user_id)

Gets the root folder from a user's library.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.

try {
    $result = $apiInstance->getRootFolder($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->getRootFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getSpecialFeatures**
> \Swagger\Client\Model\BaseItemDto[] getSpecialFeatures($user_id, $item_id)

Gets special features for an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->getSpecialFeatures($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->getSpecialFeatures: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |

### Return type

[**\Swagger\Client\Model\BaseItemDto[]**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **markFavoriteItem**
> \Swagger\Client\Model\UserItemDataDto markFavoriteItem($user_id, $item_id)

Marks an item as a favorite.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->markFavoriteItem($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->markFavoriteItem: ', $e->getMessage(), PHP_EOL;
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

# **unmarkFavoriteItem**
> \Swagger\Client\Model\UserItemDataDto unmarkFavoriteItem($user_id, $item_id)

Unmarks item as a favorite.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.

try {
    $result = $apiInstance->unmarkFavoriteItem($user_id, $item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->unmarkFavoriteItem: ', $e->getMessage(), PHP_EOL;
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

# **updateUserItemRating**
> \Swagger\Client\Model\UserItemDataDto updateUserItemRating($user_id, $item_id, $likes)

Updates a user's rating for an item.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\UserLibraryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Item id.
$likes = true; // bool | Whether this M:Jellyfin.Api.Controllers.UserLibraryController.UpdateUserItemRating(System.Guid,System.Guid,System.Nullable{System.Boolean}) is likes.

try {
    $result = $apiInstance->updateUserItemRating($user_id, $item_id, $likes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserLibraryApi->updateUserItemRating: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| User id. |
 **item_id** | [**string**](../Model/.md)| Item id. |
 **likes** | **bool**| Whether this M:Jellyfin.Api.Controllers.UserLibraryController.UpdateUserItemRating(System.Guid,System.Guid,System.Nullable{System.Boolean}) is likes. | [optional]

### Return type

[**\Swagger\Client\Model\UserItemDataDto**](../Model/UserItemDataDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

