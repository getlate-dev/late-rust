# \UsersApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_user**](UsersApi.md#get_user) | **GET** /v1/users/{userId} | Get user
[**list_users**](UsersApi.md#list_users) | **GET** /v1/users | List users



## get_user

> models::GetUser200Response get_user(user_id)
Get user

Returns a single user's details by ID, including name, email, and role.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |

### Return type

[**models::GetUser200Response**](getUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_users

> models::ListUsers200Response list_users()
List users

Returns all users in the workspace including roles and profile access. Also returns the currentUserId of the caller.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListUsers200Response**](listUsers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

