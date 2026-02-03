# \LinkedInMentionsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_linked_in_mentions**](LinkedInMentionsApi.md#get_linked_in_mentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve a LinkedIn profile or company URL to a URN for @mentions



## get_linked_in_mentions

> models::GetLinkedInMentions200Response get_linked_in_mentions(account_id, url, display_name)
Resolve a LinkedIn profile or company URL to a URN for @mentions

Converts a LinkedIn profile URL (person) or company page URL (organization) to a URN that can be used to @mention them in posts.  **Supports both:** - **Person mentions:** `linkedin.com/in/username` or just `username` - **Organization mentions:** `linkedin.com/company/company-name` or `company/company-name`  **⚠️ Organization Admin Required for Person Mentions Only:** Person mentions require the connected LinkedIn account to have admin access to at least one LinkedIn Organization (Company Page). Organization mentions do NOT have this requirement - any LinkedIn account can tag companies.  **IMPORTANT - Display Name Requirement:** For **person mentions** to be clickable, the display name must **exactly match** what appears on their LinkedIn profile. - Organization mentions automatically retrieve the company name from LinkedIn API - Person mentions require the exact name, so provide the `displayName` parameter  **Mention Format:** Use the returned `mentionFormat` value directly in your post content: ``` Great insights from @[Miquel Palet](urn:li:person:4qj5ox-agD) on this topic! Excited to partner with @[Microsoft](urn:li:organization:1035)! ``` 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The LinkedIn account ID | [required] |
**url** | **String** | LinkedIn profile URL, company URL, or vanity name. - Person: `miquelpalet`, `linkedin.com/in/miquelpalet` - Organization: `company/microsoft`, `linkedin.com/company/microsoft`  | [required] |
**display_name** | Option<**String**> | The exact display name as shown on LinkedIn. - **Person mentions:** Required for clickable mentions. If not provided, a name is derived from the vanity URL which may not match exactly. - **Organization mentions:** Optional. If not provided, the company name is automatically retrieved from LinkedIn.  |  |

### Return type

[**models::GetLinkedInMentions200Response**](getLinkedInMentions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

