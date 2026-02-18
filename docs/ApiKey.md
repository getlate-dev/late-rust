# ApiKey

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**key_preview** | Option<**String**> |  | [optional]
**expires_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**key** | Option<**String**> | Returned only once, on creation | [optional]
**scope** | Option<**Scope**> | 'full' grants access to all profiles, 'profiles' restricts to specific profiles (enum: full, profiles) | [optional][default to Full]
**profile_ids** | Option<[**Vec<models::ApiKeyProfileIdsInner>**](ApiKeyProfileIdsInner.md)> | Profiles this key can access (populated with name and color). Only present when scope is 'profiles'. | [optional]
**permission** | Option<**Permission**> | 'read-write' allows all operations, 'read' restricts to GET requests only (enum: read-write, read) | [optional][default to ReadWrite]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


