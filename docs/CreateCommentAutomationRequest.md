# CreateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | **String** | Instagram or Facebook account ID | 
**platform_post_id** | **String** | Platform media/post ID | 
**post_id** | Option<**String**> | Zernio post ID (optional) | [optional]
**post_title** | Option<**String**> | Post content snippet for display | [optional]
**name** | **String** | Automation label | 
**keywords** | Option<**Vec<String>**> | Trigger keywords (empty = any comment triggers) | [optional]
**match_mode** | Option<**MatchMode**> |  (enum: exact, contains) | [optional][default to Contains]
**dm_message** | **String** | DM text to send to commenter | 
**comment_reply** | Option<**String**> | Optional public reply to the comment | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


