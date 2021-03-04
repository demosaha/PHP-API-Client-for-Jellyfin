# Swagger\Client\TrailersApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTrailers**](TrailersApi.md#gettrailers) | **GET** /Trailers | Finds movies and trailers similar to a given trailer.

# **getTrailers**
> \Swagger\Client\Model\BaseItemDtoQueryResult getTrailers($user_id, $max_official_rating, $has_theme_song, $has_theme_video, $has_subtitles, $has_special_feature, $has_trailer, $adjacent_to, $parent_index_number, $has_parental_rating, $is_hd, $is4_k, $location_types, $exclude_location_types, $is_missing, $is_unaired, $min_community_rating, $min_critic_rating, $min_premiere_date, $min_date_last_saved, $min_date_last_saved_for_user, $max_premiere_date, $has_overview, $has_imdb_id, $has_tmdb_id, $has_tvdb_id, $exclude_item_ids, $start_index, $limit, $recursive, $search_term, $sort_order, $parent_id, $fields, $exclude_item_types, $filters, $is_favorite, $media_types, $image_types, $sort_by, $is_played, $genres, $official_ratings, $tags, $years, $enable_user_data, $image_type_limit, $enable_image_types, $person, $person_ids, $person_types, $studios, $artists, $exclude_artist_ids, $artist_ids, $album_artist_ids, $contributing_artist_ids, $albums, $album_ids, $ids, $video_types, $min_official_rating, $is_locked, $is_place_holder, $has_official_rating, $collapse_box_set_items, $min_width, $min_height, $max_width, $max_height, $is3_d, $series_status, $name_starts_with_or_greater, $name_starts_with, $name_less_than, $studio_ids, $genre_ids, $enable_total_record_count, $enable_images)

Finds movies and trailers similar to a given trailer.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\TrailersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | The user id.
$max_official_rating = "max_official_rating_example"; // string | Optional filter by maximum official rating (PG, PG-13, TV-MA, etc).
$has_theme_song = true; // bool | Optional filter by items with theme songs.
$has_theme_video = true; // bool | Optional filter by items with theme videos.
$has_subtitles = true; // bool | Optional filter by items with subtitles.
$has_special_feature = true; // bool | Optional filter by items with special features.
$has_trailer = true; // bool | Optional filter by items with trailers.
$adjacent_to = "adjacent_to_example"; // string | Optional. Return items that are siblings of a supplied item.
$parent_index_number = 56; // int | Optional filter by parent index number.
$has_parental_rating = true; // bool | Optional filter by items that have or do not have a parental rating.
$is_hd = true; // bool | Optional filter by items that are HD or not.
$is4_k = true; // bool | Optional filter by items that are 4K or not.
$location_types = array(new \Swagger\Client\Model\LocationType()); // \Swagger\Client\Model\LocationType[] | Optional. If specified, results will be filtered based on LocationType. This allows multiple, comma delimited.
$exclude_location_types = array(new \Swagger\Client\Model\LocationType()); // \Swagger\Client\Model\LocationType[] | Optional. If specified, results will be filtered based on the LocationType. This allows multiple, comma delimited.
$is_missing = true; // bool | Optional filter by items that are missing episodes or not.
$is_unaired = true; // bool | Optional filter by items that are unaired episodes or not.
$min_community_rating = 1.2; // double | Optional filter by minimum community rating.
$min_critic_rating = 1.2; // double | Optional filter by minimum critic rating.
$min_premiere_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The minimum premiere date. Format = ISO.
$min_date_last_saved = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The minimum last saved date. Format = ISO.
$min_date_last_saved_for_user = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The minimum last saved date for the current user. Format = ISO.
$max_premiere_date = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional. The maximum premiere date. Format = ISO.
$has_overview = true; // bool | Optional filter by items that have an overview or not.
$has_imdb_id = true; // bool | Optional filter by items that have an imdb id or not.
$has_tmdb_id = true; // bool | Optional filter by items that have a tmdb id or not.
$has_tvdb_id = true; // bool | Optional filter by items that have a tvdb id or not.
$exclude_item_ids = array("exclude_item_ids_example"); // string[] | Optional. If specified, results will be filtered by excluding item ids. This allows multiple, comma delimited.
$start_index = 56; // int | Optional. The record index to start at. All items with a lower index will be dropped from the results.
$limit = 56; // int | Optional. The maximum number of records to return.
$recursive = true; // bool | When searching within folders, this determines whether or not the search will be recursive. true/false.
$search_term = "search_term_example"; // string | Optional. Filter based on a search term.
$sort_order = "sort_order_example"; // string | Sort Order - Ascending,Descending.
$parent_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Specify this to localize the search to a specific item or folder. Omit to use the root.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output. This allows multiple, comma delimited. Options: Budget, Chapters, DateCreated, Genres, HomePageUrl, IndexOptions, MediaStreams, Overview, ParentId, Path, People, ProviderIds, PrimaryImageAspectRatio, Revenue, SortName, Studios, Taglines.
$exclude_item_types = array("exclude_item_types_example"); // string[] | Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited.
$filters = array(new \Swagger\Client\Model\ItemFilter()); // \Swagger\Client\Model\ItemFilter[] | Optional. Specify additional filters to apply. This allows multiple, comma delimited. Options: IsFolder, IsNotFolder, IsUnplayed, IsPlayed, IsFavorite, IsResumable, Likes, Dislikes.
$is_favorite = true; // bool | Optional filter by items that are marked as favorite, or not.
$media_types = array("media_types_example"); // string[] | Optional filter by MediaType. Allows multiple, comma delimited.
$image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. If specified, results will be filtered based on those containing image types. This allows multiple, comma delimited.
$sort_by = "sort_by_example"; // string | Optional. Specify one or more sort orders, comma delimited. Options: Album, AlbumArtist, Artist, Budget, CommunityRating, CriticRating, DateCreated, DatePlayed, PlayCount, PremiereDate, ProductionYear, SortName, Random, Revenue, Runtime.
$is_played = true; // bool | Optional filter by items that are played, or not.
$genres = array("genres_example"); // string[] | Optional. If specified, results will be filtered based on genre. This allows multiple, pipe delimited.
$official_ratings = array("official_ratings_example"); // string[] | Optional. If specified, results will be filtered based on OfficialRating. This allows multiple, pipe delimited.
$tags = array("tags_example"); // string[] | Optional. If specified, results will be filtered based on tag. This allows multiple, pipe delimited.
$years = array(56); // int[] | Optional. If specified, results will be filtered based on production year. This allows multiple, comma delimited.
$enable_user_data = true; // bool | Optional, include user data.
$image_type_limit = 56; // int | Optional, the max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$person = "person_example"; // string | Optional. If specified, results will be filtered to include only those containing the specified person.
$person_ids = array("person_ids_example"); // string[] | Optional. If specified, results will be filtered to include only those containing the specified person id.
$person_types = array("person_types_example"); // string[] | Optional. If specified, along with Person, results will be filtered to include only those containing the specified person and PersonType. Allows multiple, comma-delimited.
$studios = array("studios_example"); // string[] | Optional. If specified, results will be filtered based on studio. This allows multiple, pipe delimited.
$artists = array("artists_example"); // string[] | Optional. If specified, results will be filtered based on artists. This allows multiple, pipe delimited.
$exclude_artist_ids = array("exclude_artist_ids_example"); // string[] | Optional. If specified, results will be filtered based on artist id. This allows multiple, pipe delimited.
$artist_ids = array("artist_ids_example"); // string[] | Optional. If specified, results will be filtered to include only those containing the specified artist id.
$album_artist_ids = array("album_artist_ids_example"); // string[] | Optional. If specified, results will be filtered to include only those containing the specified album artist id.
$contributing_artist_ids = array("contributing_artist_ids_example"); // string[] | Optional. If specified, results will be filtered to include only those containing the specified contributing artist id.
$albums = array("albums_example"); // string[] | Optional. If specified, results will be filtered based on album. This allows multiple, pipe delimited.
$album_ids = array("album_ids_example"); // string[] | Optional. If specified, results will be filtered based on album id. This allows multiple, pipe delimited.
$ids = array("ids_example"); // string[] | Optional. If specific items are needed, specify a list of item id's to retrieve. This allows multiple, comma delimited.
$video_types = array(new \Swagger\Client\Model\VideoType()); // \Swagger\Client\Model\VideoType[] | Optional filter by VideoType (videofile, dvd, bluray, iso). Allows multiple, comma delimited.
$min_official_rating = "min_official_rating_example"; // string | Optional filter by minimum official rating (PG, PG-13, TV-MA, etc).
$is_locked = true; // bool | Optional filter by items that are locked.
$is_place_holder = true; // bool | Optional filter by items that are placeholders.
$has_official_rating = true; // bool | Optional filter by items that have official ratings.
$collapse_box_set_items = true; // bool | Whether or not to hide items behind their boxsets.
$min_width = 56; // int | Optional. Filter by the minimum width of the item.
$min_height = 56; // int | Optional. Filter by the minimum height of the item.
$max_width = 56; // int | Optional. Filter by the maximum width of the item.
$max_height = 56; // int | Optional. Filter by the maximum height of the item.
$is3_d = true; // bool | Optional filter by items that are 3D, or not.
$series_status = array(new \Swagger\Client\Model\SeriesStatus()); // \Swagger\Client\Model\SeriesStatus[] | Optional filter by Series Status. Allows multiple, comma delimited.
$name_starts_with_or_greater = "name_starts_with_or_greater_example"; // string | Optional filter by items whose name is sorted equally or greater than a given input string.
$name_starts_with = "name_starts_with_example"; // string | Optional filter by items whose name is sorted equally than a given input string.
$name_less_than = "name_less_than_example"; // string | Optional filter by items whose name is equally or lesser than a given input string.
$studio_ids = array("studio_ids_example"); // string[] | Optional. If specified, results will be filtered based on studio id. This allows multiple, pipe delimited.
$genre_ids = array("genre_ids_example"); // string[] | Optional. If specified, results will be filtered based on genre id. This allows multiple, pipe delimited.
$enable_total_record_count = true; // bool | Optional. Enable the total record count.
$enable_images = true; // bool | Optional, include image information in output.

try {
    $result = $apiInstance->getTrailers($user_id, $max_official_rating, $has_theme_song, $has_theme_video, $has_subtitles, $has_special_feature, $has_trailer, $adjacent_to, $parent_index_number, $has_parental_rating, $is_hd, $is4_k, $location_types, $exclude_location_types, $is_missing, $is_unaired, $min_community_rating, $min_critic_rating, $min_premiere_date, $min_date_last_saved, $min_date_last_saved_for_user, $max_premiere_date, $has_overview, $has_imdb_id, $has_tmdb_id, $has_tvdb_id, $exclude_item_ids, $start_index, $limit, $recursive, $search_term, $sort_order, $parent_id, $fields, $exclude_item_types, $filters, $is_favorite, $media_types, $image_types, $sort_by, $is_played, $genres, $official_ratings, $tags, $years, $enable_user_data, $image_type_limit, $enable_image_types, $person, $person_ids, $person_types, $studios, $artists, $exclude_artist_ids, $artist_ids, $album_artist_ids, $contributing_artist_ids, $albums, $album_ids, $ids, $video_types, $min_official_rating, $is_locked, $is_place_holder, $has_official_rating, $collapse_box_set_items, $min_width, $min_height, $max_width, $max_height, $is3_d, $series_status, $name_starts_with_or_greater, $name_starts_with, $name_less_than, $studio_ids, $genre_ids, $enable_total_record_count, $enable_images);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrailersApi->getTrailers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | [**string**](../Model/.md)| The user id. | [optional]
 **max_official_rating** | **string**| Optional filter by maximum official rating (PG, PG-13, TV-MA, etc). | [optional]
 **has_theme_song** | **bool**| Optional filter by items with theme songs. | [optional]
 **has_theme_video** | **bool**| Optional filter by items with theme videos. | [optional]
 **has_subtitles** | **bool**| Optional filter by items with subtitles. | [optional]
 **has_special_feature** | **bool**| Optional filter by items with special features. | [optional]
 **has_trailer** | **bool**| Optional filter by items with trailers. | [optional]
 **adjacent_to** | **string**| Optional. Return items that are siblings of a supplied item. | [optional]
 **parent_index_number** | **int**| Optional filter by parent index number. | [optional]
 **has_parental_rating** | **bool**| Optional filter by items that have or do not have a parental rating. | [optional]
 **is_hd** | **bool**| Optional filter by items that are HD or not. | [optional]
 **is4_k** | **bool**| Optional filter by items that are 4K or not. | [optional]
 **location_types** | [**\Swagger\Client\Model\LocationType[]**](../Model/\Swagger\Client\Model\LocationType.md)| Optional. If specified, results will be filtered based on LocationType. This allows multiple, comma delimited. | [optional]
 **exclude_location_types** | [**\Swagger\Client\Model\LocationType[]**](../Model/\Swagger\Client\Model\LocationType.md)| Optional. If specified, results will be filtered based on the LocationType. This allows multiple, comma delimited. | [optional]
 **is_missing** | **bool**| Optional filter by items that are missing episodes or not. | [optional]
 **is_unaired** | **bool**| Optional filter by items that are unaired episodes or not. | [optional]
 **min_community_rating** | **double**| Optional filter by minimum community rating. | [optional]
 **min_critic_rating** | **double**| Optional filter by minimum critic rating. | [optional]
 **min_premiere_date** | **\DateTime**| Optional. The minimum premiere date. Format &#x3D; ISO. | [optional]
 **min_date_last_saved** | **\DateTime**| Optional. The minimum last saved date. Format &#x3D; ISO. | [optional]
 **min_date_last_saved_for_user** | **\DateTime**| Optional. The minimum last saved date for the current user. Format &#x3D; ISO. | [optional]
 **max_premiere_date** | **\DateTime**| Optional. The maximum premiere date. Format &#x3D; ISO. | [optional]
 **has_overview** | **bool**| Optional filter by items that have an overview or not. | [optional]
 **has_imdb_id** | **bool**| Optional filter by items that have an imdb id or not. | [optional]
 **has_tmdb_id** | **bool**| Optional filter by items that have a tmdb id or not. | [optional]
 **has_tvdb_id** | **bool**| Optional filter by items that have a tvdb id or not. | [optional]
 **exclude_item_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered by excluding item ids. This allows multiple, comma delimited. | [optional]
 **start_index** | **int**| Optional. The record index to start at. All items with a lower index will be dropped from the results. | [optional]
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **recursive** | **bool**| When searching within folders, this determines whether or not the search will be recursive. true/false. | [optional]
 **search_term** | **string**| Optional. Filter based on a search term. | [optional]
 **sort_order** | **string**| Sort Order - Ascending,Descending. | [optional]
 **parent_id** | [**string**](../Model/.md)| Specify this to localize the search to a specific item or folder. Omit to use the root. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. This allows multiple, comma delimited. Options: Budget, Chapters, DateCreated, Genres, HomePageUrl, IndexOptions, MediaStreams, Overview, ParentId, Path, People, ProviderIds, PrimaryImageAspectRatio, Revenue, SortName, Studios, Taglines. | [optional]
 **exclude_item_types** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on item type. This allows multiple, comma delimited. | [optional]
 **filters** | [**\Swagger\Client\Model\ItemFilter[]**](../Model/\Swagger\Client\Model\ItemFilter.md)| Optional. Specify additional filters to apply. This allows multiple, comma delimited. Options: IsFolder, IsNotFolder, IsUnplayed, IsPlayed, IsFavorite, IsResumable, Likes, Dislikes. | [optional]
 **is_favorite** | **bool**| Optional filter by items that are marked as favorite, or not. | [optional]
 **media_types** | [**string[]**](../Model/string.md)| Optional filter by MediaType. Allows multiple, comma delimited. | [optional]
 **image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. If specified, results will be filtered based on those containing image types. This allows multiple, comma delimited. | [optional]
 **sort_by** | **string**| Optional. Specify one or more sort orders, comma delimited. Options: Album, AlbumArtist, Artist, Budget, CommunityRating, CriticRating, DateCreated, DatePlayed, PlayCount, PremiereDate, ProductionYear, SortName, Random, Revenue, Runtime. | [optional]
 **is_played** | **bool**| Optional filter by items that are played, or not. | [optional]
 **genres** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on genre. This allows multiple, pipe delimited. | [optional]
 **official_ratings** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on OfficialRating. This allows multiple, pipe delimited. | [optional]
 **tags** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on tag. This allows multiple, pipe delimited. | [optional]
 **years** | [**int[]**](../Model/int.md)| Optional. If specified, results will be filtered based on production year. This allows multiple, comma delimited. | [optional]
 **enable_user_data** | **bool**| Optional, include user data. | [optional]
 **image_type_limit** | **int**| Optional, the max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **person** | **string**| Optional. If specified, results will be filtered to include only those containing the specified person. | [optional]
 **person_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered to include only those containing the specified person id. | [optional]
 **person_types** | [**string[]**](../Model/string.md)| Optional. If specified, along with Person, results will be filtered to include only those containing the specified person and PersonType. Allows multiple, comma-delimited. | [optional]
 **studios** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on studio. This allows multiple, pipe delimited. | [optional]
 **artists** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on artists. This allows multiple, pipe delimited. | [optional]
 **exclude_artist_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on artist id. This allows multiple, pipe delimited. | [optional]
 **artist_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered to include only those containing the specified artist id. | [optional]
 **album_artist_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered to include only those containing the specified album artist id. | [optional]
 **contributing_artist_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered to include only those containing the specified contributing artist id. | [optional]
 **albums** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on album. This allows multiple, pipe delimited. | [optional]
 **album_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on album id. This allows multiple, pipe delimited. | [optional]
 **ids** | [**string[]**](../Model/string.md)| Optional. If specific items are needed, specify a list of item id&#x27;s to retrieve. This allows multiple, comma delimited. | [optional]
 **video_types** | [**\Swagger\Client\Model\VideoType[]**](../Model/\Swagger\Client\Model\VideoType.md)| Optional filter by VideoType (videofile, dvd, bluray, iso). Allows multiple, comma delimited. | [optional]
 **min_official_rating** | **string**| Optional filter by minimum official rating (PG, PG-13, TV-MA, etc). | [optional]
 **is_locked** | **bool**| Optional filter by items that are locked. | [optional]
 **is_place_holder** | **bool**| Optional filter by items that are placeholders. | [optional]
 **has_official_rating** | **bool**| Optional filter by items that have official ratings. | [optional]
 **collapse_box_set_items** | **bool**| Whether or not to hide items behind their boxsets. | [optional]
 **min_width** | **int**| Optional. Filter by the minimum width of the item. | [optional]
 **min_height** | **int**| Optional. Filter by the minimum height of the item. | [optional]
 **max_width** | **int**| Optional. Filter by the maximum width of the item. | [optional]
 **max_height** | **int**| Optional. Filter by the maximum height of the item. | [optional]
 **is3_d** | **bool**| Optional filter by items that are 3D, or not. | [optional]
 **series_status** | [**\Swagger\Client\Model\SeriesStatus[]**](../Model/\Swagger\Client\Model\SeriesStatus.md)| Optional filter by Series Status. Allows multiple, comma delimited. | [optional]
 **name_starts_with_or_greater** | **string**| Optional filter by items whose name is sorted equally or greater than a given input string. | [optional]
 **name_starts_with** | **string**| Optional filter by items whose name is sorted equally than a given input string. | [optional]
 **name_less_than** | **string**| Optional filter by items whose name is equally or lesser than a given input string. | [optional]
 **studio_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on studio id. This allows multiple, pipe delimited. | [optional]
 **genre_ids** | [**string[]**](../Model/string.md)| Optional. If specified, results will be filtered based on genre id. This allows multiple, pipe delimited. | [optional]
 **enable_total_record_count** | **bool**| Optional. Enable the total record count. | [optional] [default to true]
 **enable_images** | **bool**| Optional, include image information in output. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

