# \ProfilesApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_profile**](ProfilesApi.md#create_profile) | **POST** /v1/profiles | Create profile
[**delete_profile**](ProfilesApi.md#delete_profile) | **DELETE** /v1/profiles/{profileId} | Delete profile
[**get_profile**](ProfilesApi.md#get_profile) | **GET** /v1/profiles/{profileId} | Get profile
[**list_profiles**](ProfilesApi.md#list_profiles) | **GET** /v1/profiles | List profiles
[**update_profile**](ProfilesApi.md#update_profile) | **PUT** /v1/profiles/{profileId} | Update profile



## create_profile

> models::ProfileCreateResponse create_profile(create_profile_request)
Create profile

Creates a new profile with a name, optional description, and color.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_profile_request** | [**CreateProfileRequest**](CreateProfileRequest.md) |  | [required] |

### Return type

[**models::ProfileCreateResponse**](ProfileCreateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_profile

> models::DeleteAccountGroup200Response delete_profile(profile_id)
Delete profile

Permanently deletes a profile by ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_profile

> models::GetProfile200Response get_profile(profile_id)
Get profile

Returns a single profile by ID, including its name, color, and default status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |

### Return type

[**models::GetProfile200Response**](getProfile_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_profiles

> models::ProfilesListResponse list_profiles(include_over_limit)
List profiles

Returns profiles sorted by creation date. Use includeOverLimit=true to include profiles that exceed the plan limit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**include_over_limit** | Option<**bool**> | When true, includes over-limit profiles (marked with isOverLimit: true). |  |[default to false]

### Return type

[**models::ProfilesListResponse**](ProfilesListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_profile

> models::UpdateProfile200Response update_profile(profile_id, update_profile_request)
Update profile

Updates a profile's name, description, color, or default status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |
**update_profile_request** | [**UpdateProfileRequest**](UpdateProfileRequest.md) |  | [required] |

### Return type

[**models::UpdateProfile200Response**](updateProfile_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

