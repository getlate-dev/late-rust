# \GmbMediaApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_google_business_media**](GmbMediaApi.md#create_google_business_media) | **POST** /v1/accounts/{accountId}/gmb-media | Upload photo
[**delete_google_business_media**](GmbMediaApi.md#delete_google_business_media) | **DELETE** /v1/accounts/{accountId}/gmb-media | Delete photo
[**list_google_business_media**](GmbMediaApi.md#list_google_business_media) | **GET** /v1/accounts/{accountId}/gmb-media | List media



## create_google_business_media

> models::CreateGoogleBusinessMedia200Response create_google_business_media(account_id, create_google_business_media_request)
Upload photo

Creates a media item (photo) for a location from a publicly accessible URL.  Categories determine where the photo appears: - `COVER` - Cover photo - `PROFILE` - Profile photo - `LOGO` - Business logo - `EXTERIOR` - Exterior shots - `INTERIOR` - Interior shots - `FOOD_AND_DRINK` - Food and drink photos - `MENU` - Menu photos - `PRODUCT` - Product photos - `TEAMS` - Team/staff photos - `ADDITIONAL` - Other photos 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**create_google_business_media_request** | [**CreateGoogleBusinessMediaRequest**](CreateGoogleBusinessMediaRequest.md) |  | [required] |

### Return type

[**models::CreateGoogleBusinessMedia200Response**](createGoogleBusinessMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_google_business_media

> models::DeleteGoogleBusinessMedia200Response delete_google_business_media(account_id, media_id)
Delete photo

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**media_id** | **String** | The media item ID to delete | [required] |

### Return type

[**models::DeleteGoogleBusinessMedia200Response**](deleteGoogleBusinessMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_google_business_media

> models::ListGoogleBusinessMedia200Response list_google_business_media(account_id, page_size, page_token)
List media

Lists media items (photos) for a Google Business Profile location. Returns photo URLs, descriptions, categories, and metadata. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**page_size** | Option<**i32**> | Number of items to return (max 100) |  |[default to 100]
**page_token** | Option<**String**> | Pagination token from previous response |  |

### Return type

[**models::ListGoogleBusinessMedia200Response**](listGoogleBusinessMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

