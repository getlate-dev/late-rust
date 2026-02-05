# UpdateGoogleBusinessLocationDetailsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**update_mask** | **String** | Required. Comma-separated fields to update (e.g. 'regularHours', 'specialHours', 'profile.description') | 
**regular_hours** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestRegularHours**](UpdateGoogleBusinessLocationDetailsRequestRegularHours.md)> |  | [optional]
**special_hours** | Option<[**models::GetGoogleBusinessLocationDetails200ResponseSpecialHours**](GetGoogleBusinessLocationDetails200ResponseSpecialHours.md)> |  | [optional]
**profile** | Option<[**models::UpdateGoogleBusinessLocationDetailsRequestProfile**](UpdateGoogleBusinessLocationDetailsRequestProfile.md)> |  | [optional]
**website_uri** | Option<**String**> |  | [optional]
**phone_numbers** | Option<[**models::GetGoogleBusinessLocationDetails200ResponsePhoneNumbers**](GetGoogleBusinessLocationDetails200ResponsePhoneNumbers.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


