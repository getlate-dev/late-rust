# SendInboxMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | 
**message** | Option<**String**> | Message text | [optional]
**quick_replies** | Option<[**Vec<models::SendInboxMessageRequestQuickRepliesInner>**](SendInboxMessageRequestQuickRepliesInner.md)> | Quick reply buttons. Mutually exclusive with buttons. Max 13 items. | [optional]
**buttons** | Option<[**Vec<models::SendInboxMessageRequestButtonsInner>**](SendInboxMessageRequestButtonsInner.md)> | Action buttons. Mutually exclusive with quickReplies. Max 3 items. | [optional]
**template** | Option<[**models::SendInboxMessageRequestTemplate**](SendInboxMessageRequestTemplate.md)> |  | [optional]
**reply_markup** | Option<[**models::SendInboxMessageRequestReplyMarkup**](SendInboxMessageRequestReplyMarkup.md)> |  | [optional]
**messaging_type** | Option<**MessagingType**> | Facebook messaging type. Required when using messageTag. (enum: RESPONSE, UPDATE, MESSAGE_TAG) | [optional]
**message_tag** | Option<**MessageTag**> | Facebook message tag for messaging outside 24h window. Requires messagingType MESSAGE_TAG. Instagram only supports HUMAN_AGENT. (enum: CONFIRMED_EVENT_UPDATE, POST_PURCHASE_UPDATE, ACCOUNT_UPDATE, HUMAN_AGENT) | [optional]
**reply_to** | Option<**String**> | Platform message ID to reply to (Telegram only). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


