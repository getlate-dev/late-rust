# \GmbAttributesApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_google_business_attributes**](GmbAttributesApi.md#get_google_business_attributes) | **GET** /v1/accounts/{accountId}/gmb-attributes | Get attributes
[**update_google_business_attributes**](GmbAttributesApi.md#update_google_business_attributes) | **PUT** /v1/accounts/{accountId}/gmb-attributes | Update attributes



## get_google_business_attributes

> models::GetGoogleBusinessAttributes200Response get_google_business_attributes(account_id)
Get attributes

Fetches location attributes such as amenities, services, and accessibility features. Common attributes include dining options (has_dine_in, has_takeout, has_delivery), amenities (has_outdoor_seating, has_wifi), accessibility, and payment types. Available attributes vary by business category. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetGoogleBusinessAttributes200Response**](getGoogleBusinessAttributes_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_google_business_attributes

> models::UpdateGoogleBusinessAttributes200Response update_google_business_attributes(account_id, update_google_business_attributes_request)
Update attributes

Updates location attributes (amenities, services, etc.).  The attributeMask specifies which attributes to update (comma-separated). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_google_business_attributes_request** | [**UpdateGoogleBusinessAttributesRequest**](UpdateGoogleBusinessAttributesRequest.md) |  | [required] |

### Return type

[**models::UpdateGoogleBusinessAttributes200Response**](updateGoogleBusinessAttributes_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

