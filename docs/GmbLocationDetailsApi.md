# \GmbLocationDetailsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_google_business_location_details**](GmbLocationDetailsApi.md#get_google_business_location_details) | **GET** /v1/accounts/{accountId}/gmb-location-details | Get location details
[**update_google_business_location_details**](GmbLocationDetailsApi.md#update_google_business_location_details) | **PUT** /v1/accounts/{accountId}/gmb-location-details | Update location details



## get_google_business_location_details

> models::GetGoogleBusinessLocationDetails200Response get_google_business_location_details(account_id, read_mask)
Get location details

Returns detailed GBP location info (hours, description, phone, website, categories). Use readMask to request specific fields.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Late account ID (from /v1/accounts) | [required] |
**read_mask** | Option<**String**> | Comma-separated fields to return. Available: name, title, phoneNumbers, categories, storefrontAddress, websiteUri, regularHours, specialHours, serviceArea, profile, openInfo, metadata, moreHours. |  |

### Return type

[**models::GetGoogleBusinessLocationDetails200Response**](getGoogleBusinessLocationDetails_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_google_business_location_details

> models::UpdateGoogleBusinessLocationDetails200Response update_google_business_location_details(account_id, update_google_business_location_details_request)
Update location details

Updates GBP location details (hours, description, phone, website). The updateMask field is required and specifies which fields to update.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Late account ID (from /v1/accounts) | [required] |
**update_google_business_location_details_request** | [**UpdateGoogleBusinessLocationDetailsRequest**](UpdateGoogleBusinessLocationDetailsRequest.md) |  | [required] |

### Return type

[**models::UpdateGoogleBusinessLocationDetails200Response**](updateGoogleBusinessLocationDetails_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

