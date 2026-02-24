# WebhookPayloadCommentComment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform comment ID | [optional]
**post_id** | Option<**String**> | Internal post ID | [optional]
**platform_post_id** | Option<**String**> | Platform's post ID | [optional]
**platform** | Option<**Platform**> |  (enum: instagram, facebook, twitter, youtube, linkedin, bluesky, reddit) | [optional]
**text** | Option<**String**> | Comment text content | [optional]
**author** | Option<[**models::WebhookPayloadCommentCommentAuthor**](WebhookPayloadCommentCommentAuthor.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**is_reply** | Option<**bool**> | Whether this is a reply to another comment | [optional]
**parent_comment_id** | Option<**String**> | Parent comment ID if this is a reply | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


