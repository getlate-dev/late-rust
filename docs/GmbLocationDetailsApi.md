# \GmbLocationDetailsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_google_business_location_details**](GmbLocationDetailsApi.md#get_google_business_location_details) | **GET** /v1/accounts/{accountId}/gmb-location-details | Get Google Business Profile location details
[**update_google_business_location_details**](GmbLocationDetailsApi.md#update_google_business_location_details) | **PUT** /v1/accounts/{accountId}/gmb-location-details | Update Google Business Profile location details



## get_google_business_location_details

> models::GetGoogleBusinessLocationDetails200Response get_google_business_location_details(account_id, read_mask)
Get Google Business Profile location details

Fetches detailed location information including opening hours, special hours, business description, phone numbers, website, categories, and more.  Use the `readMask` query parameter to request specific fields. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Late account ID (from /v1/accounts) | [required] |
**read_mask** | Option<**String**> | Comma-separated fields to return. Defaults to common fields. Available: name, title, phoneNumbers, categories, storefrontAddress, websiteUri, regularHours, specialHours, serviceArea, profile, openInfo, metadata, moreHours  |  |

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
Update Google Business Profile location details

Updates location details such as opening hours, special hours, business description, phone, and website.  The `updateMask` field is required and specifies which fields to update.  Common update masks: - `regularHours` - Update opening hours - `specialHours` - Update holiday/special hours - `profile.description` - Update business description - `websiteUri` - Update website URL - `phoneNumbers` - Update phone numbers - `regularHours,specialHours` - Update both at once 

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

