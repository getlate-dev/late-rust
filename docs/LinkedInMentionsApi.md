# \LinkedInMentionsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_linked_in_mentions**](LinkedInMentionsApi.md#get_linked_in_mentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve LinkedIn mention



## get_linked_in_mentions

> models::GetLinkedInMentions200Response get_linked_in_mentions(account_id, url, display_name)
Resolve LinkedIn mention

Converts a LinkedIn profile or company URL to a URN for @mentions in posts. Supports person mentions (linkedin.com/in/username or just username) and org mentions (linkedin.com/company/name or company/name). Person mentions require admin access to at least one LinkedIn Organization. Org mentions work with any account. For person mentions to be clickable, provide the displayName parameter matching the exact name on their profile. Org names are fetched automatically. Use the returned mentionFormat directly in post content. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The LinkedIn account ID | [required] |
**url** | **String** | LinkedIn profile URL, company URL, or vanity name. Person examples: miquelpalet, linkedin.com/in/miquelpalet. Organization examples: company/microsoft, linkedin.com/company/microsoft.  | [required] |
**display_name** | Option<**String**> | The exact display name as shown on LinkedIn. Required for person mentions (for clickable mentions; if not provided, a name is derived from the vanity URL which may not match). Optional for organization mentions (company name is auto-retrieved from LinkedIn).  |  |

### Return type

[**models::GetLinkedInMentions200Response**](getLinkedInMentions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

