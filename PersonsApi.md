# Swagger\Client\PersonsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPerson**](PersonsApi.md#getperson) | **GET** /Persons/{name} | Get person by name.
[**getPersons**](PersonsApi.md#getpersons) | **GET** /Persons | Gets all persons.

# **getPerson**
> \Swagger\Client\Model\BaseItemDto getPerson($name, $user_id)

Get person by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PersonsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | Person name.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. Filter by user id, and attach user data.

try {
    $result = $apiInstance->getPerson($name, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonsApi->getPerson: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| Person name. |
 **user_id** | [**string**](../Model/.md)| Optional. Filter by user id, and attach user data. | [optional]

### Return type

[**\Swagger\Client\Model\BaseItemDto**](../Model/BaseItemDto.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPersons**
> \Swagger\Client\Model\BaseItemDtoQueryResult getPersons($limit, $search_term, $fields, $filters, $is_favorite, $enable_user_data, $image_type_limit, $enable_image_types, $exclude_person_types, $person_types, $appears_in_item_id, $user_id, $enable_images)

Gets all persons.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: CustomAuthentication
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Emby-Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Emby-Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PersonsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 56; // int | Optional. The maximum number of records to return.
$search_term = "search_term_example"; // string | The search term.
$fields = array(new \Swagger\Client\Model\ItemFields()); // \Swagger\Client\Model\ItemFields[] | Optional. Specify additional fields of information to return in the output.
$filters = array(new \Swagger\Client\Model\ItemFilter()); // \Swagger\Client\Model\ItemFilter[] | Optional. Specify additional filters to apply.
$is_favorite = true; // bool | Optional filter by items that are marked as favorite, or not. userId is required.
$enable_user_data = true; // bool | Optional, include user data.
$image_type_limit = 56; // int | Optional, the max number of images to return, per image type.
$enable_image_types = array(new \Swagger\Client\Model\ImageType()); // \Swagger\Client\Model\ImageType[] | Optional. The image types to include in the output.
$exclude_person_types = array("exclude_person_types_example"); // string[] | Optional. If specified results will be filtered to exclude those containing the specified PersonType. Allows multiple, comma-delimited.
$person_types = array("person_types_example"); // string[] | Optional. If specified results will be filtered to include only those containing the specified PersonType. Allows multiple, comma-delimited.
$appears_in_item_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Optional. If specified, person results will be filtered on items related to said persons.
$user_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | User id.
$enable_images = true; // bool | Optional, include image information in output.

try {
    $result = $apiInstance->getPersons($limit, $search_term, $fields, $filters, $is_favorite, $enable_user_data, $image_type_limit, $enable_image_types, $exclude_person_types, $person_types, $appears_in_item_id, $user_id, $enable_images);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PersonsApi->getPersons: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Optional. The maximum number of records to return. | [optional]
 **search_term** | **string**| The search term. | [optional]
 **fields** | [**\Swagger\Client\Model\ItemFields[]**](../Model/\Swagger\Client\Model\ItemFields.md)| Optional. Specify additional fields of information to return in the output. | [optional]
 **filters** | [**\Swagger\Client\Model\ItemFilter[]**](../Model/\Swagger\Client\Model\ItemFilter.md)| Optional. Specify additional filters to apply. | [optional]
 **is_favorite** | **bool**| Optional filter by items that are marked as favorite, or not. userId is required. | [optional]
 **enable_user_data** | **bool**| Optional, include user data. | [optional]
 **image_type_limit** | **int**| Optional, the max number of images to return, per image type. | [optional]
 **enable_image_types** | [**\Swagger\Client\Model\ImageType[]**](../Model/\Swagger\Client\Model\ImageType.md)| Optional. The image types to include in the output. | [optional]
 **exclude_person_types** | [**string[]**](../Model/string.md)| Optional. If specified results will be filtered to exclude those containing the specified PersonType. Allows multiple, comma-delimited. | [optional]
 **person_types** | [**string[]**](../Model/string.md)| Optional. If specified results will be filtered to include only those containing the specified PersonType. Allows multiple, comma-delimited. | [optional]
 **appears_in_item_id** | [**string**](../Model/.md)| Optional. If specified, person results will be filtered on items related to said persons. | [optional]
 **user_id** | [**string**](../Model/.md)| User id. | [optional]
 **enable_images** | **bool**| Optional, include image information in output. | [optional] [default to true]

### Return type

[**\Swagger\Client\Model\BaseItemDtoQueryResult**](../Model/BaseItemDtoQueryResult.md)

### Authorization

[CustomAuthentication](../../README.md#CustomAuthentication)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

