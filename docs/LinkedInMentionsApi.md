# \LinkedInMentionsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_linked_in_mentions**](LinkedInMentionsApi.md#get_linked_in_mentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve LinkedIn mention



## get_linked_in_mentions

> models::GetLinkedInMentions200Response get_linked_in_mentions(account_id, url, display_name)
Resolve LinkedIn mention

Converts a LinkedIn profile or company URL to a URN for @mentions in posts. Person mentions require org admin access. Use the returned mentionFormat in post content.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The LinkedIn account ID | [required] |
**url** | **String** | LinkedIn profile URL, company URL, or vanity name. | [required] |
**display_name** | Option<**String**> | Exact display name as shown on LinkedIn. Required for person mentions to be clickable. Optional for org mentions. |  |

### Return type

[**models::GetLinkedInMentions200Response**](getLinkedInMentions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

