# Swagger\Client\VideoAttachmentsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAttachment**](VideoAttachmentsApi.md#getattachment) | **GET** /Videos/{videoId}/{mediaSourceId}/Attachments/{index} | Get video attachment.

# **getAttachment**
> string getAttachment($video_id, $media_source_id, $index)

Get video attachment.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\VideoAttachmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$video_id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | Video ID.
$media_source_id = "media_source_id_example"; // string | Media Source ID.
$index = 56; // int | Attachment Index.

try {
    $result = $apiInstance->getAttachment($video_id, $media_source_id, $index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoAttachmentsApi->getAttachment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **video_id** | [**string**](../Model/.md)| Video ID. |
 **media_source_id** | **string**| Media Source ID. |
 **index** | **int**| Attachment Index. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json, application/json; profile=\"CamelCase\", application/json; profile=\"PascalCase\"

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

