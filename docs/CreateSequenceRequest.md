# CreateSequenceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | **String** |  | 
**platform** | **Platform** |  (enum: instagram, facebook, telegram, twitter, bluesky, reddit, whatsapp) | 
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**steps** | Option<[**Vec<models::CreateSequenceRequestStepsInner>**](CreateSequenceRequestStepsInner.md)> |  | [optional]
**exit_on_reply** | Option<**bool**> |  | [optional][default to true]
**exit_on_unsubscribe** | Option<**bool**> |  | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


