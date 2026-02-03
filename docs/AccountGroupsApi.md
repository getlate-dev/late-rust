# \AccountGroupsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_account_group**](AccountGroupsApi.md#create_account_group) | **POST** /v1/account-groups | Create a new account group
[**delete_account_group**](AccountGroupsApi.md#delete_account_group) | **DELETE** /v1/account-groups/{groupId} | Delete an account group
[**list_account_groups**](AccountGroupsApi.md#list_account_groups) | **GET** /v1/account-groups | List account groups for the authenticated user
[**update_account_group**](AccountGroupsApi.md#update_account_group) | **PUT** /v1/account-groups/{groupId} | Update an account group



## create_account_group

> models::CreateAccountGroup201Response create_account_group(create_account_group_request)
Create a new account group

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_account_group_request** | [**CreateAccountGroupRequest**](CreateAccountGroupRequest.md) |  | [required] |

### Return type

[**models::CreateAccountGroup201Response**](createAccountGroup_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_account_group

> models::DeleteAccountGroup200Response delete_account_group(group_id)
Delete an account group

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_account_groups

> models::ListAccountGroups200Response list_account_groups()
List account groups for the authenticated user

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListAccountGroups200Response**](listAccountGroups_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_account_group

> models::UpdateAccountGroup200Response update_account_group(group_id, update_account_group_request)
Update an account group

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** |  | [required] |
**update_account_group_request** | [**UpdateAccountGroupRequest**](UpdateAccountGroupRequest.md) |  | [required] |

### Return type

[**models::UpdateAccountGroup200Response**](updateAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

