# PlatformTarget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> | Supported values: twitter, threads, instagram, youtube, facebook, linkedin, pinterest, reddit, tiktok, bluesky, googlebusiness, telegram | [optional]
**account_id** | Option<[**models::PlatformTargetAccountId**](PlatformTargetAccountId.md)> |  | [optional]
**custom_content** | Option<**String**> |  | [optional]
**custom_media** | Option<[**Vec<models::MediaItem>**](MediaItem.md)> |  | [optional]
**scheduled_for** | Option<**String**> | Optional per-platform scheduled time override (uses post.scheduledFor when omitted) | [optional]
**platform_specific_data** | Option<[**models::PlatformTargetPlatformSpecificData**](PlatformTargetPlatformSpecificData.md)> |  | [optional]
**status** | Option<**String**> | Platform-specific status: pending, publishing, published, failed | [optional]
**platform_post_id** | Option<**String**> | The native post ID on the platform (populated after successful publish) | [optional]
**platform_post_url** | Option<**String**> | Public URL of the published post on the platform. Populated after successful publish. For immediate posts (publishNow=true),  this is included in the response. For scheduled posts, fetch the post  via GET /v1/posts/{postId} after the scheduled time.  | [optional]
**published_at** | Option<**String**> | Timestamp when the post was published to this platform | [optional]
**error_message** | Option<**String**> | Human-readable error message when status is 'failed'. Contains platform-specific error details explaining why the publish failed. Examples: - \"Instagram access token has expired. Please reconnect your account.\" - \"Post text exceeds the 500 character limit for Threads.\" - \"You do not have enough karma to post in this subreddit.\" - \"Video is too long for Reels. Facebook Reels must be 90 seconds or less.\"  | [optional]
**error_category** | Option<**ErrorCategory**> | Error category for programmatic handling: - auth_expired: Token expired or revoked, account needs reconnection - user_content: Content doesn't meet platform requirements (too long, wrong format, etc.) - user_abuse: Rate limits, spam detection, excessive posting - account_issue: Account configuration problems (missing board, inactive account) - platform_rejected: Platform rules violated (banned, suspended, policy violation) - platform_error: Platform-side issues (5xx errors, maintenance) - system_error: Late infrastructure issues (timeouts, network errors) - unknown: Unclassified error  (enum: auth_expired, user_content, user_abuse, account_issue, platform_rejected, platform_error, system_error, unknown) | [optional]
**error_source** | Option<**ErrorSource**> | Who/what caused the error: - user: User action required (fix content, reconnect account) - platform: Platform-side issue (outage, API change) - system: Late system issue (rare)  (enum: user, platform, system) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


