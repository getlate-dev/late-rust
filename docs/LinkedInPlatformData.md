# LinkedInPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization_urn** | Option<**String**> | Target LinkedIn Organization URN for multi-organization posting. Format: \"urn:li:organization:123456789\" If omitted, uses the selected/default organization on the connection. Use GET /api/v1/accounts/{id}/linkedin-organizations to list available organizations.  | [optional]
**first_comment** | Option<**String**> | Optional first comment to add after the post is created | [optional]
**disable_link_preview** | Option<**bool**> | Set to true to disable automatic link previews for URLs in the post content (default is false) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


