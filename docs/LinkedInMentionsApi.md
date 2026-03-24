# \LinkedInMentionsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_linked_in_mentions**](LinkedInMentionsApi.md#get_linked_in_mentions) | **GET** /v1/accounts/{accountId}/linkedin-mentions | Resolve LinkedIn mention



## get_linked_in_mentions

> models::GetLinkedInMentions200Response get_linked_in_mentions(account_id, url, display_name)
Resolve LinkedIn mention

Converts a LinkedIn profile or company URL to a URN for @mentions in posts.  **How to use LinkedIn @mentions (2-step workflow):**  1. Call this endpoint with the LinkedIn profile/company URL to get the mention URN and format. 2. Embed the returned `mentionFormat` (e.g. `@[Vincent Jong](urn:li:person:xxx)`) directly in your post's `content` field.  **Example:** - Resolve: `GET /v1/accounts/{id}/linkedin-mentions?url=linkedin.com/in/vincentjong&displayName=Vincent Jong` - Returns: `mentionFormat: \"@[Vincent Jong](urn:li:person:xxx)\"` - Use in post content: `\"Great talk with @[Vincent Jong](urn:li:person:xxx) today!\"`  **Important:** The `mentions` array field in POST /v1/posts is stored for reference only and does NOT trigger @mentions on LinkedIn. You must embed the mention format directly in the content text.  **Requirements:** - Person mentions require the LinkedIn account to be admin of at least one organization. - Organization mentions (e.g. @Microsoft) work without this requirement. - For person mentions to be clickable, the `displayName` parameter must exactly match the name shown on their LinkedIn profile. 

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

