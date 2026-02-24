# UpdateWebhookSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **String** | Webhook ID to update (required) | 
**name** | Option<**String**> | Webhook name (max 50 characters) | [optional]
**url** | Option<**String**> | Webhook endpoint URL (must be HTTPS in production) | [optional]
**secret** | Option<**String**> | Secret key for HMAC-SHA256 signature verification | [optional]
**events** | Option<**Vec<Events>**> | Events to subscribe to (enum: post.scheduled, post.published, post.failed, post.partial, account.connected, account.disconnected, message.received, comment.received) | [optional]
**is_active** | Option<**bool**> | Enable or disable webhook delivery | [optional]
**custom_headers** | Option<**std::collections::HashMap<String, String>**> | Custom headers to include in webhook requests | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


