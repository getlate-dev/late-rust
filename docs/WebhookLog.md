# WebhookLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**webhook_id** | Option<**String**> | ID of the webhook that was triggered | [optional]
**webhook_name** | Option<**String**> | Name of the webhook that was triggered | [optional]
**event** | Option<**Event**> |  (enum: post.scheduled, post.published, post.failed, post.partial, account.connected, account.disconnected, message.received, comment.received, webhook.test) | [optional]
**url** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: success, failed) | [optional]
**status_code** | Option<**i32**> | HTTP status code from webhook endpoint | [optional]
**request_payload** | Option<**serde_json::Value**> | Payload sent to webhook endpoint | [optional]
**response_body** | Option<**String**> | Response body from webhook endpoint (truncated to 10KB) | [optional]
**error_message** | Option<**String**> | Error message if delivery failed | [optional]
**attempt_number** | Option<**i32**> | Delivery attempt number (max 3 retries) | [optional]
**response_time** | Option<**i32**> | Response time in milliseconds | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


