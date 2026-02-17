# \InvitesApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_invite_token**](InvitesApi.md#create_invite_token) | **POST** /v1/invite/tokens | Create invite token



## create_invite_token

> models::CreateInviteToken201Response create_invite_token(create_invite_token_request)
Create invite token

Generate a secure invite link to grant team members access to your profiles. Invites expire after 7 days and are single-use. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_invite_token_request** | [**CreateInviteTokenRequest**](CreateInviteTokenRequest.md) |  | [required] |

### Return type

[**models::CreateInviteToken201Response**](createInviteToken_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

