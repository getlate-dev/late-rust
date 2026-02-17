# \ApiKeysApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_api_key**](ApiKeysApi.md#create_api_key) | **POST** /v1/api-keys | Create key
[**delete_api_key**](ApiKeysApi.md#delete_api_key) | **DELETE** /v1/api-keys/{keyId} | Delete key
[**list_api_keys**](ApiKeysApi.md#list_api_keys) | **GET** /v1/api-keys | List keys



## create_api_key

> models::CreateApiKey201Response create_api_key(create_api_key_request)
Create key

Creates a new API key with an optional expiry. The full key value is only returned once in the response.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_api_key_request** | [**CreateApiKeyRequest**](CreateApiKeyRequest.md) |  | [required] |

### Return type

[**models::CreateApiKey201Response**](createApiKey_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_api_key

> models::DeleteAccountGroup200Response delete_api_key(key_id)
Delete key

Permanently revokes and deletes an API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**key_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_api_keys

> models::ListApiKeys200Response list_api_keys()
List keys

Returns all API keys for the authenticated user. Keys are returned with a preview only, not the full key value.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListApiKeys200Response**](listApiKeys_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

