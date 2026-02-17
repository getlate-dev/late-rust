# YouTubePlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> | Video title. Defaults to first line of content or \"Untitled Video\". Must be ≤ 100 characters. | [optional]
**visibility** | Option<**Visibility**> | Video visibility: public (default, anyone can watch), unlisted (link only), private (invite only) (enum: public, private, unlisted) | [optional][default to Public]
**made_for_kids** | Option<**bool**> | COPPA compliance flag. Set true for child-directed content (restricts comments, notifications, ad targeting). Defaults to false. YouTube may block views if not explicitly set. | [optional][default to false]
**first_comment** | Option<**String**> | Optional first comment to post immediately after video upload. Up to 10,000 characters (YouTube's comment limit). | [optional]
**contains_synthetic_media** | Option<**bool**> | AI-generated content disclosure. Set true if the video contains synthetic content that could be mistaken for real. YouTube may add a label. | [optional][default to false]
**category_id** | Option<**String**> | YouTube video category ID. Defaults to 22 (People & Blogs). Common: 1 (Film), 2 (Autos), 10 (Music), 15 (Pets), 17 (Sports), 20 (Gaming), 23 (Comedy), 24 (Entertainment), 25 (News), 26 (Howto), 27 (Education), 28 (Science & Tech). | [optional][default to 22]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


