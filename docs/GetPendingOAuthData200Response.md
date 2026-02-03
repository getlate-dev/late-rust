# GetPendingOAuthData200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> | The platform (e.g., \"linkedin\") | [optional]
**profile_id** | Option<**String**> | The Late profile ID | [optional]
**temp_token** | Option<**String**> | Temporary access token for the platform | [optional]
**refresh_token** | Option<**String**> | Refresh token (if available) | [optional]
**expires_in** | Option<**f64**> | Token expiry in seconds | [optional]
**user_profile** | Option<**serde_json::Value**> | User profile data (id, username, displayName, profilePicture) | [optional]
**selection_type** | Option<**SelectionType**> | Type of selection data (enum: organizations, pages, boards, locations, profiles) | [optional]
**organizations** | Option<[**Vec<models::GetPendingOAuthData200ResponseOrganizationsInner>**](GetPendingOAuthData200ResponseOrganizationsInner.md)> | LinkedIn organizations (when selectionType is \"organizations\") | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


