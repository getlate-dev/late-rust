# \MediaApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_media_presigned_url**](MediaApi.md#get_media_presigned_url) | **POST** /v1/media/presign | Get presigned upload URL



## get_media_presigned_url

> models::GetMediaPresignedUrl200Response get_media_presigned_url(get_media_presigned_url_request)
Get presigned upload URL

Get a presigned URL to upload files directly to cloud storage (up to 5GB). Returns an uploadUrl and publicUrl. PUT your file to the uploadUrl, then use the publicUrl in your posts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**get_media_presigned_url_request** | [**GetMediaPresignedUrlRequest**](GetMediaPresignedUrlRequest.md) |  | [required] |

### Return type

[**models::GetMediaPresignedUrl200Response**](getMediaPresignedUrl_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

