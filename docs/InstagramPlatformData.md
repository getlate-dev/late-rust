# InstagramPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content_type** | Option<**ContentType**> | Set to 'story' to publish as a Story. Default posts become Reels or feed depending on media. (enum: story) | [optional]
**share_to_feed** | Option<**bool**> | For Reels only. When true (default), the Reel appears on both the Reels tab and your main profile feed. Set to false to post to the Reels tab only. | [optional][default to true]
**collaborators** | Option<**Vec<String>**> | Up to 3 Instagram usernames to invite as collaborators (feed/Reels only) | [optional]
**first_comment** | Option<**String**> | Optional first comment to add after the post is created (not applied to Stories) | [optional]
**trial_params** | Option<[**models::InstagramPlatformDataTrialParams**](InstagramPlatformDataTrialParams.md)> |  | [optional]
**user_tags** | Option<[**Vec<models::InstagramPlatformDataUserTagsInner>**](InstagramPlatformDataUserTagsInner.md)> | Tag Instagram users in photos by username and position. Not supported for stories or videos. For carousels, use mediaIndex to target specific slides (defaults to 0). Tags on video items are silently skipped. | [optional]
**audio_name** | Option<**String**> | Custom name for original audio in Reels. Replaces the default \"Original Audio\" label. Can only be set once. | [optional]
**thumb_offset** | Option<**i32**> | Millisecond offset from video start for the Reel thumbnail. Ignored if a custom thumbnail URL is provided. Defaults to 0. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


