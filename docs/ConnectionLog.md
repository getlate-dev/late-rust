# ConnectionLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**user_id** | Option<**String**> | User who owns the connection (may be null for early OAuth failures) | [optional]
**profile_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | The social account ID (present on successful connections and disconnects) | [optional]
**platform** | Option<**Platform**> |  (enum: tiktok, instagram, facebook, youtube, linkedin, twitter, threads, pinterest, reddit, bluesky, googlebusiness, telegram, snapchat) | [optional]
**event_type** | Option<**EventType**> | Type of connection event: connect_success, connect_failed, disconnect, reconnect_success, reconnect_failed (enum: connect_success, connect_failed, disconnect, reconnect_success, reconnect_failed) | [optional]
**connection_method** | Option<**ConnectionMethod**> | How the connection was initiated (enum: oauth, credentials, invitation) | [optional]
**error** | Option<[**models::ConnectionLogError**](ConnectionLogError.md)> |  | [optional]
**success** | Option<[**models::ConnectionLogSuccess**](ConnectionLogSuccess.md)> |  | [optional]
**context** | Option<[**models::ConnectionLogContext**](ConnectionLogContext.md)> |  | [optional]
**duration_ms** | Option<**i32**> | How long the operation took in milliseconds | [optional]
**metadata** | Option<**serde_json::Value**> | Additional metadata | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


