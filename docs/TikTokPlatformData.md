# TikTokPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**draft** | Option<**bool**> | When true, sends the post to the TikTok Creator Inbox as a draft instead of publishing immediately. | [optional]
**privacy_level** | Option<**String**> | One of the values returned by the TikTok creator info API for the account | [optional]
**allow_comment** | Option<**bool**> | Allow comments on the post | [optional]
**allow_duet** | Option<**bool**> | Allow duets (required for video posts) | [optional]
**allow_stitch** | Option<**bool**> | Allow stitches (required for video posts) | [optional]
**commercial_content_type** | Option<**CommercialContentType**> | Type of commercial content disclosure (enum: none, brand_organic, brand_content) | [optional]
**brand_partner_promote** | Option<**bool**> | Whether the post promotes a brand partner | [optional]
**is_brand_organic_post** | Option<**bool**> | Whether the post is a brand organic post | [optional]
**content_preview_confirmed** | Option<**bool**> | User has confirmed they previewed the content | [optional]
**express_consent_given** | Option<**bool**> | User has given express consent for posting | [optional]
**media_type** | Option<**MediaType**> | Optional override. Defaults based on provided media items. (enum: video, photo) | [optional]
**video_cover_timestamp_ms** | Option<**i32**> | Optional for video posts. Timestamp in milliseconds to select which frame to use as thumbnail (defaults to 1000ms/1 second). | [optional]
**photo_cover_index** | Option<**i32**> | Optional for photo carousels. Index of image to use as cover, 0-based (defaults to 0/first image). | [optional]
**auto_add_music** | Option<**bool**> | When true, TikTok may add recommended music (photos only) | [optional]
**video_made_with_ai** | Option<**bool**> | Set true to disclose AI-generated content | [optional]
**description** | Option<**String**> | Optional long-form description for photo posts (max 4000 chars). Recommended when content exceeds 90 chars, as photo titles are auto-truncated. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


