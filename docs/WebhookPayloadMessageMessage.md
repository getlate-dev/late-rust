# WebhookPayloadMessageMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Internal message ID | [optional]
**conversation_id** | Option<**String**> | Internal conversation ID | [optional]
**platform** | Option<**Platform**> |  (enum: instagram, facebook, telegram, bluesky, reddit) | [optional]
**platform_message_id** | Option<**String**> | Platform's message ID | [optional]
**direction** | Option<**Direction**> |  (enum: incoming) | [optional]
**text** | Option<**String**> | Message text content | [optional]
**attachments** | Option<[**Vec<models::WebhookPayloadMessageMessageAttachmentsInner>**](WebhookPayloadMessageMessageAttachmentsInner.md)> |  | [optional]
**sender** | Option<[**models::WebhookPayloadMessageMessageSender**](WebhookPayloadMessageMessageSender.md)> |  | [optional]
**sent_at** | Option<**String**> |  | [optional]
**is_read** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


