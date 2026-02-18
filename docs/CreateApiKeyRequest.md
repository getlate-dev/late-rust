# CreateApiKeyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**expires_in** | Option<**i32**> | Days until expiry | [optional]
**scope** | Option<**Scope**> | 'full' grants access to all profiles (default), 'profiles' restricts to specific profiles (enum: full, profiles) | [optional][default to Full]
**profile_ids** | Option<**Vec<String>**> | Profile IDs this key can access. Required when scope is 'profiles'. | [optional]
**permission** | Option<**Permission**> | 'read-write' allows all operations (default), 'read' restricts to GET requests only (enum: read-write, read) | [optional][default to ReadWrite]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


