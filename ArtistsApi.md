# Swagger\Client\ArtistsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAlbumArtists**](ArtistsApi.md#getalbumartists) | **GET** /Artists/AlbumArtists | Gets all album artists from a given item, folder, or the entire library.
[**getArtistByName**](ArtistsApi.md#getartistbyname) | **GET** /Artists/{name} | Gets an artist by name.
[**getArtists**](ArtistsApi.md#getartists) | **GET** /Artists | Gets all artists from a given item, folder, or the entire library.

# **getAlbumArtists**
> \Swagger\Client\Model\BaseItemDtoQueryResult getAlbumArtists($min_community_rating, $start_index, $limit, $search_term, $parent_id, $fields, $exclude_item_types, $include_item_types, $filters, $is_favorite, $media_types, $genres, $genre_ids, $official_ratings, $tags, $years, $enable_user_data, $image_type_limit, $enable_image_types, $person, $person_ids, $person_types, $studios, $studio_ids, $user_id, $name_starts_with_or_greater, $name_starts_with, $name_less_than, $enable_images, $enable_total_record_count)

Gets all album artists from a given item, folder, or the entire library.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ArtistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$min_community_rating = 1.2; // double | Optional filter by minimum community rating.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$search_term = "search_term_example"; // string | Optional. Search term.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Specify this to localize the search to a specific item or folder. Omit to use the root.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$exclude_item_types = array("exclude_item_types_example"); // string[] | Optional. If specified, results will be filtered out based on item type. This allows multiple, comma delimited.
$include_item_types = array("include_item_types_example"); // string[] | Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited.
$filters = array(new \Swagger\Client\Model\ItemFilter()); // \Swagger\Client\Model\ItemFilter[] | Optional. Specify additional filters to apply.
$is_favorite = true; // bool | Optional filter by items that are marked as favorite, or not.
$media_types = array("media_types_example"); // string[] | Optional filter by MediaType. Allows multiple, comma delimited.
$genres = array("genres_example"); // string[] | Optional. If specified, results will be filtered based on genre. This allows multiple, pipe delimited.
$genre_ids = array("genre_ids_example"); // string[] | Optional. If specified, results will be filtered based on genre id. This allows multiple, pipe delimited.
$official_ratings = array("official_ratings_example"); // string[] | Optional. If specified, results will be filtered based on OfficialRating. This allows multiple, pipe delimited.
$tags = array("tags_example"); // string[] | Optional. If specified, results will be filtered based on tag. This allows multiple, pipe delimited.
$years = array(56); // int[] | Optional. If specified, results will be filtered based on production year. This allows multiple, comma delimited.
$enable_user_data = true; // bool | Optional, include user data.
$image_type_limit = 56; // int | Optional, the max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$person = "person_example"; // string | Optional. If specified, results will be filtered to include only those containing the specified person.
$person_ids = array("person_ids_example"); // string[] | Optional. If specified, results will be filtered to include only those containing the specified person ids.
$person_types = array("person_types_example"); // string[] | Optional. If specified, along with Person, results will be filtered to include only those containing the specified person and PersonType. Allows multiple, comma-delimited.
$studios = array("studios_example"); // string[] | Optional. If specified, results will be filtered based on studio. This allows multiple, pipe delimited.
$studio_ids = array("studio_ids_example"); // string[] | Optional. If specified, results will be filtered based on studio id. This allows multiple, pipe delimited.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$name_starts_with_or_greater = "name_starts_with_or_greater_example"; // string | Optional filter by items whose name is sorted equally or greater than a given input string.
$name_starts_with = "name_starts_with_example"; // string | Optional filter by items whose name is sorted equally than a given input string.
$name_less_than = "name_less_than_example"; // string | Optional filter by items whose name is equally or lesser than a given input string.
$enable_images = true; // bool | Optional, include image information in output.
$enable_total_record_count = true; // bool | Total record count.

try {
    $result = $apiInstance->getAlbumArtists($min_community_rating, $start_index, $limit, $search_term, $parent_id, $fields, $exclude_item_types, $include_item_types, $filters, $is_favorite, $media_types, $genres, $genre_ids, $official_ratings, $tags, $years, $enable_user_data, $image_type_limit, $enable_image_types, $person, $person_ids, $person_types, $studios, $studio_ids, $user_id, $name_starts_with_or_greater, $name_starts_with, $name_less_than, $enable_images, $enable_total_record_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArtistsApi->getAlbumArtists: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **min_community_rating** | **double**| Optional filter by minimum community rating. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **search_term** | **string**| Optional. Search term. | [optional]
 **parent_id** | [**string**](../Model/.md)| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **exclude_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered out based on item type. This allows multiple, comma delimited. | [optional]
 **include_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited. | [optional]
 **filters** | [**\Swagger\Client\Model\ItemFilter[]**](../Model/\Swagger\Client\Model\ItemFilter.md)| Optional. Specify additional filters to apply. | [optional]
 **is_favorite** | **bool**| Optional filter by items that are marked as favorite, or not. | [optional]
 **media_types** | [**string[]**](../Model/string.md)| Optional filter by MediaType. Allows multiple, comma delimited. | [optional]
 **genres** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on genre. This allows multiple, pipe delimited. | [optional]
 **genre_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on genre id. This allows multiple, pipe delimited. | [optional]
 **official_ratings** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on OfficialRating. This allows multiple, pipe delimited. | [optional]
 **tags** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on tag. This allows multiple, pipe delimited. | [optional]
 **years** | [**int[]**](../Model/int.md)| Optional. If specified, results will be filtered based on production year. This allows multiple, comma delimited. | [optional]
 **enable_user_data** | **bool**| Optional, include user data. | [optional]
 **image_type_limit** | **int**| Optional, the max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **person** | **string**| Optional. If specified, results will be filtered to include only those containing the specified person. | [optional]
 **person_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered to include only those containing the specified person ids. | [optional]
 **person_types** | [**string[]**](../Model/string.md)| Optional. If specified, along with Person, results will be filtered to include only those containing the specified person and PersonType. Allows multiple, comma-delimited. | [optional]
 **studios** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on studio. This allows multiple, pipe delimited. | [optional]
 **studio_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on studio id. This allows multiple, pipe delimited. | [optional]
 **user_id** | [**string**](../Model/.md)| User id. | [optional]
 **name_starts_with_or_greater** | **string**| Optional filter by items whose name is sorted equally or greater than a given input string. | [optional]
 **name_starts_with** | **string**| Optional filter by items whose name is sorted equally than a given input string. | [optional]
 **name_less_than** | **string**| Optional filter by items whose name is equally or lesser than a given input string. | [optional]
 **enable_images** | **bool**| Optional, include image information in output. | [optional] [default to true]
 **enable_total_record_count** | **bool**| Total record count. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getArtistByName**
> \Swagger\Client\Model\BaseItemDto getArtistByName($name, $user_id)

Gets an artist by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ArtistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | Studio name.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.

try {
    $result = $apiInstance->getArtistByName($name, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArtistsApi->getArtistByName: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Studio name. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getArtists**
> \Swagger\Client\Model\BaseItemDtoQueryResult getArtists($min_community_rating, $start_index, $limit, $search_term, $parent_id, $fields, $exclude_item_types, $include_item_types, $filters, $is_favorite, $media_types, $genres, $genre_ids, $official_ratings, $tags, $years, $enable_user_data, $image_type_limit, $enable_image_types, $person, $person_ids, $person_types, $studios, $studio_ids, $user_id, $name_starts_with_or_greater, $name_starts_with, $name_less_than, $enable_images, $enable_total_record_count)

Gets all artists from a given item, folder, or the entire library.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\ArtistsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$min_community_rating = 1.2; // double | Optional filter by minimum community rating.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$search_term = "search_term_example"; // string | Optional. Search term.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Specify this to localize the search to a specific item or folder. Omit to use the root.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$exclude_item_types = array("exclude_item_types_example"); // string[] | Optional. If specified, results will be filtered out based on item type. This allows multiple, comma delimited.
$include_item_types = array("include_item_types_example"); // string[] | Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited.
$filters = array(new \Swagger\Client\Model\ItemFilter()); // \Swagger\Client\Model\ItemFilter[] | Optional. Specify additional filters to apply.
$is_favorite = true; // bool | Optional filter by items that are marked as favorite, or not.
$media_types = array("media_types_example"); // string[] | Optional filter by MediaType. Allows multiple, comma delimited.
$genres = array("genres_example"); // string[] | Optional. If specified, results will be filtered based on genre. This allows multiple, pipe delimited.
$genre_ids = array("genre_ids_example"); // string[] | Optional. If specified, results will be filtered based on genre id. This allows multiple, pipe delimited.
$official_ratings = array("official_ratings_example"); // string[] | Optional. If specified, results will be filtered based on OfficialRating. This allows multiple, pipe delimited.
$tags = array("tags_example"); // string[] | Optional. If specified, results will be filtered based on tag. This allows multiple, pipe delimited.
$years = array(56); // int[] | Optional. If specified, results will be filtered based on production year. This allows multiple, comma delimited.
$enable_user_data = true; // bool | Optional, include user data.
$image_type_limit = 56; // int | Optional, the max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$person = "person_example"; // string | Optional. If specified, results will be filtered to include only those containing the specified person.
$person_ids = array("person_ids_example"); // string[] | Optional. If specified, results will be filtered to include only those containing the specified person ids.
$person_types = array("person_types_example"); // string[] | Optional. If specified, along with Person, results will be filtered to include only those containing the specified person and PersonType. Allows multiple, comma-delimited.
$studios = array("studios_example"); // string[] | Optional. If specified, results will be filtered based on studio. This allows multiple, pipe delimited.
$studio_ids = array("studio_ids_example"); // string[] | Optional. If specified, results will be filtered based on studio id. This allows multiple, pipe delimited.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$name_starts_with_or_greater = "name_starts_with_or_greater_example"; // string | Optional filter by items whose name is sorted equally or greater than a given input string.
$name_starts_with = "name_starts_with_example"; // string | Optional filter by items whose name is sorted equally than a given input string.
$name_less_than = "name_less_than_example"; // string | Optional filter by items whose name is equally or lesser than a given input string.
$enable_images = true; // bool | Optional, include image information in output.
$enable_total_record_count = true; // bool | Total record count.

try {
    $result = $apiInstance->getArtists($min_community_rating, $start_index, $limit, $search_term, $parent_id, $fields, $exclude_item_types, $include_item_types, $filters, $is_favorite, $media_types, $genres, $genre_ids, $official_ratings, $tags, $years, $enable_user_data, $image_type_limit, $enable_image_types, $person, $person_ids, $person_types, $studios, $studio_ids, $user_id, $name_starts_with_or_greater, $name_starts_with, $name_less_than, $enable_images, $enable_total_record_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArtistsApi->getArtists: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **min_community_rating** | **double**| Optional filter by minimum community rating. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **search_term** | **string**| Optional. Search term. | [optional]
 **parent_id** | [**string**](../Model/.md)| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **exclude_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered out based on item type. This allows multiple, comma delimited. | [optional]
 **include_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited. | [optional]
 **filters** | [**\Swagger\Client\Model\ItemFilter[]**](../Model/\Swagger\Client\Model\ItemFilter.md)| Optional. Specify additional filters to apply. | [optional]
 **is_favorite** | **bool**| Optional filter by items that are marked as favorite, or not. | [optional]
 **media_types** | [**string[]**](../Model/string.md)| Optional filter by MediaType. Allows multiple, comma delimited. | [optional]
 **genres** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on genre. This allows multiple, pipe delimited. | [optional]
 **genre_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on genre id. This allows multiple, pipe delimited. | [optional]
 **official_ratings** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on OfficialRating. This allows multiple, pipe delimited. | [optional]
 **tags** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on tag. This allows multiple, pipe delimited. | [optional]
 **years** | [**int[]**](../Model/int.md)| Optional. If specified, results will be filtered based on production year. This allows multiple, comma delimited. | [optional]
 **enable_user_data** | **bool**| Optional, include user data. | [optional]
 **image_type_limit** | **int**| Optional, the max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **person** | **string**| Optional. If specified, results will be filtered to include only those containing the specified person. | [optional]
 **person_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered to include only those containing the specified person ids. | [optional]
 **person_types** | [**string[]**](../Model/string.md)| Optional. If specified, along with Person, results will be filtered to include only those containing the specified person and PersonType. Allows multiple, comma-delimited. | [optional]
 **studios** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on studio. This allows multiple, pipe delimited. | [optional]
 **studio_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on studio id. This allows multiple, pipe delimited. | [optional]
 **user_id** | [**string**](../Model/.md)| User id. | [optional]
 **name_starts_with_or_greater** | **string**| Optional filter by items whose name is sorted equally or greater than a given input string. | [optional]
 **name_starts_with** | **string**| Optional filter by items whose name is sorted equally than a given input string. | [optional]
 **name_less_than** | **string**| Optional filter by items whose name is equally or lesser than a given input string. | [optional]
 **enable_images** | **bool**| Optional, include image information in output. | [optional] [default to true]
 **enable_total_record_count** | **bool**| Total record count. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

