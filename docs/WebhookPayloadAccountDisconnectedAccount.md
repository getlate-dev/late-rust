# WebhookPayloadAccountDisconnectedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> | The account's unique identifier (same as used in /v1/accounts/{accountId}) | [optional]
**profile_id** | Option<**String**> | The profile's unique identifier this account belongs to | [optional]
**platform** | Option<**String**> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**disconnection_type** | Option<**DisconnectionType**> | Whether the disconnection was intentional (user action) or unintentional (token expired/revoked) (enum: intentional, unintentional) | [optional]
**reason** | Option<**String**> | Human-readable reason for the disconnection | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


