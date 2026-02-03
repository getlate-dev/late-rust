# YouTubePlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> | Video title. Defaults to first line of content or \"Untitled Video\". Must be ≤ 100 characters. | [optional]
**visibility** | Option<**Visibility**> | Video visibility setting: - public: Anyone can search for and watch (default) - unlisted: Only people with the link can watch - private: Only you and people you specifically share with can watch  (enum: public, private, unlisted) | [optional][default to Public]
**made_for_kids** | Option<**bool**> | COPPA compliance: Audience designation for the video. - true: Video is made for kids (child-directed content) - false: Video is NOT made for kids (default)  This field maps to YouTube's `selfDeclaredMadeForKids` setting. Videos marked as made for kids have restricted features (no comments, no notifications, limited ad targeting).  IMPORTANT: If not specified, defaults to false. YouTube requires this to be explicitly set, otherwise the video may be blocked from views until configured in YouTube Studio.  | [optional][default to false]
**first_comment** | Option<**String**> | Optional first comment to post immediately after video upload. Up to 10,000 characters (YouTube's comment limit). | [optional]
**contains_synthetic_media** | Option<**bool**> | AI-generated content disclosure flag. Set to true if your video contains AI-generated or synthetic content that could be mistaken for real people, places, or events. This helps viewers understand when realistic content has been created or altered using AI. YouTube may add a label to videos when this is set. Added to YouTube Data API in October 2024.  | [optional][default to false]
**category_id** | Option<**String**> | YouTube video category ID. Defaults to '22' (People & Blogs). Common categories: 1 (Film & Animation), 2 (Autos & Vehicles), 10 (Music), 15 (Pets & Animals), 17 (Sports), 20 (Gaming), 22 (People & Blogs), 23 (Comedy), 24 (Entertainment), 25 (News & Politics), 26 (Howto & Style), 27 (Education), 28 (Science & Technology).  | [optional][default to 22]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


