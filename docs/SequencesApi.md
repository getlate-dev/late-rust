# \SequencesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_sequence**](SequencesApi.md#activate_sequence) | **POST** /v1/sequences/{sequenceId}/activate | Activate a sequence
[**create_sequence**](SequencesApi.md#create_sequence) | **POST** /v1/sequences | Create a sequence
[**delete_sequence**](SequencesApi.md#delete_sequence) | **DELETE** /v1/sequences/{sequenceId} | Delete a sequence
[**enroll_contacts**](SequencesApi.md#enroll_contacts) | **POST** /v1/sequences/{sequenceId}/enroll | Enroll contacts in a sequence
[**get_sequence**](SequencesApi.md#get_sequence) | **GET** /v1/sequences/{sequenceId} | Get sequence with steps
[**list_sequence_enrollments**](SequencesApi.md#list_sequence_enrollments) | **GET** /v1/sequences/{sequenceId}/enrollments | List enrollments for a sequence
[**list_sequences**](SequencesApi.md#list_sequences) | **GET** /v1/sequences | List sequences
[**pause_sequence**](SequencesApi.md#pause_sequence) | **POST** /v1/sequences/{sequenceId}/pause | Pause a sequence
[**unenroll_contact**](SequencesApi.md#unenroll_contact) | **DELETE** /v1/sequences/{sequenceId}/enroll/{contactId} | Unenroll a contact from a sequence
[**update_sequence**](SequencesApi.md#update_sequence) | **PATCH** /v1/sequences/{sequenceId} | Update a sequence



## activate_sequence

> models::ActivateSequence200Response activate_sequence(sequence_id)
Activate a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::ActivateSequence200Response**](activateSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_sequence

> create_sequence(create_sequence_request)
Create a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_sequence_request** | [**CreateSequenceRequest**](CreateSequenceRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_sequence

> delete_sequence(sequence_id)
Delete a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enroll_contacts

> models::EnrollContacts200Response enroll_contacts(sequence_id, enroll_contacts_request)
Enroll contacts in a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |
**enroll_contacts_request** | [**EnrollContactsRequest**](EnrollContactsRequest.md) |  | [required] |

### Return type

[**models::EnrollContacts200Response**](enrollContacts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sequence

> models::GetSequence200Response get_sequence(sequence_id)
Get sequence with steps

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::GetSequence200Response**](getSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sequence_enrollments

> models::ListSequenceEnrollments200Response list_sequence_enrollments(sequence_id, status, limit, skip)
List enrollments for a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListSequenceEnrollments200Response**](listSequenceEnrollments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sequences

> models::ListSequences200Response list_sequences(profile_id, status, limit, skip)
List sequences

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile. Omit to list across all profiles |  |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListSequences200Response**](listSequences_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pause_sequence

> models::ActivateSequence200Response pause_sequence(sequence_id)
Pause a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::ActivateSequence200Response**](activateSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unenroll_contact

> unenroll_contact(sequence_id, contact_id)
Unenroll a contact from a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |
**contact_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_sequence

> models::UpdateSequence200Response update_sequence(sequence_id)
Update a sequence

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::UpdateSequence200Response**](updateSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

