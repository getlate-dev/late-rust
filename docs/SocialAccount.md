# SocialAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**profile_id** | Option<[**models::SocialAccountProfileId**](SocialAccountProfileId.md)> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**profile_url** | Option<**String**> | Full profile URL for the connected account. Available for all platforms: - Twitter/X: https://x.com/{username} - Instagram: https://instagram.com/{username} - TikTok: https://tiktok.com/@{username} - YouTube: https://youtube.com/@{handle} or https://youtube.com/channel/{id} - LinkedIn Personal: https://www.linkedin.com/in/{vanityName}/ - LinkedIn Organization: https://www.linkedin.com/company/{vanityName}/ - Threads: https://threads.net/@{username} - Pinterest: https://pinterest.com/{username} - Reddit: https://reddit.com/user/{username} - Bluesky: https://bsky.app/profile/{handle} - Facebook: https://facebook.com/{username} or https://facebook.com/{pageId} - Google Business: Google Maps URL for the business location  | [optional]
**is_active** | Option<**bool**> |  | [optional]
**followers_count** | Option<**f64**> | Follower count (only included if user has analytics add-on) | [optional]
**followers_last_updated** | Option<**String**> | Last time follower count was updated (only included if user has analytics add-on) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


