# \CustomFieldsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clear_contact_field_value**](CustomFieldsApi.md#clear_contact_field_value) | **DELETE** /v1/contacts/{contactId}/fields/{slug} | Clear a custom field value
[**create_custom_field**](CustomFieldsApi.md#create_custom_field) | **POST** /v1/custom-fields | Create a custom field definition
[**delete_custom_field**](CustomFieldsApi.md#delete_custom_field) | **DELETE** /v1/custom-fields/{fieldId} | Delete a custom field definition
[**list_custom_fields**](CustomFieldsApi.md#list_custom_fields) | **GET** /v1/custom-fields | List custom field definitions
[**set_contact_field_value**](CustomFieldsApi.md#set_contact_field_value) | **PUT** /v1/contacts/{contactId}/fields/{slug} | Set a custom field value
[**update_custom_field**](CustomFieldsApi.md#update_custom_field) | **PATCH** /v1/custom-fields/{fieldId} | Update a custom field definition



## clear_contact_field_value

> clear_contact_field_value(contact_id, slug)
Clear a custom field value

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**contact_id** | **String** |  | [required] |
**slug** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_custom_field

> create_custom_field(create_custom_field_request)
Create a custom field definition

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_custom_field_request** | [**CreateCustomFieldRequest**](CreateCustomFieldRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_custom_field

> delete_custom_field(field_id)
Delete a custom field definition

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**field_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_custom_fields

> list_custom_fields(profile_id)
List custom field definitions

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_contact_field_value

> set_contact_field_value(contact_id, slug, set_contact_field_value_request)
Set a custom field value

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**contact_id** | **String** |  | [required] |
**slug** | **String** |  | [required] |
**set_contact_field_value_request** | [**SetContactFieldValueRequest**](SetContactFieldValueRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_custom_field

> update_custom_field(field_id, update_custom_field_request)
Update a custom field definition

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**field_id** | **String** |  | [required] |
**update_custom_field_request** | Option<[**UpdateCustomFieldRequest**](UpdateCustomFieldRequest.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

