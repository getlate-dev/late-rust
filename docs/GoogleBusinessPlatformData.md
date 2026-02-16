# GoogleBusinessPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**location_id** | Option<**String**> | Target Google Business location ID for multi-location posting. Format: \"locations/123456789\" If omitted, uses the selected/default location on the connection. Use GET /api/v1/accounts/{id}/gmb-locations to list available locations.  | [optional]
**language_code** | Option<**String**> | BCP 47 language code for the post content (e.g., \"en\", \"de\", \"es\", \"fr\"). If omitted, the language is automatically detected from the post text. Setting this explicitly is recommended when auto-detection may not be accurate (e.g., very short posts, mixed-language content, or transliterated text).  | [optional]
**call_to_action** | Option<[**models::GoogleBusinessPlatformDataCallToAction**](GoogleBusinessPlatformDataCallToAction.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


