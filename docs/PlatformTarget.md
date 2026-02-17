# PlatformTarget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> | Supported values: twitter, threads, instagram, youtube, facebook, linkedin, pinterest, reddit, tiktok, bluesky, googlebusiness, telegram | [optional]
**account_id** | Option<[**models::PlatformTargetAccountId**](PlatformTargetAccountId.md)> |  | [optional]
**custom_content** | Option<**String**> | Platform-specific text override. When set, this content is used instead of the top-level post content for this platform. Useful for tailoring captions per platform (e.g. keeping tweets under 280 characters). | [optional]
**custom_media** | Option<[**Vec<models::MediaItem>**](MediaItem.md)> |  | [optional]
**scheduled_for** | Option<**String**> | Optional per-platform scheduled time override (uses post.scheduledFor when omitted) | [optional]
**platform_specific_data** | Option<[**models::PlatformTargetPlatformSpecificData**](PlatformTargetPlatformSpecificData.md)> |  | [optional]
**status** | Option<**String**> | Platform-specific status: pending, publishing, published, failed | [optional]
**platform_post_id** | Option<**String**> | The native post ID on the platform (populated after successful publish) | [optional]
**platform_post_url** | Option<**String**> | Public URL of the published post on the platform. Populated after successful publish. For immediate posts (publishNow=true),  this is included in the response. For scheduled posts, fetch the post  via GET /v1/posts/{postId} after the scheduled time.  | [optional]
**published_at** | Option<**String**> | Timestamp when the post was published to this platform | [optional]
**error_message** | Option<**String**> | Human-readable error message when status is failed. Contains platform-specific error details explaining why the publish failed. | [optional]
**error_category** | Option<**ErrorCategory**> | Error category for programmatic handling: auth_expired (token expired/revoked), user_content (wrong format/too long), user_abuse (rate limits/spam), account_issue (config problems), platform_rejected (policy violation), platform_error (5xx/maintenance), system_error (Late infra), unknown (enum: auth_expired, user_content, user_abuse, account_issue, platform_rejected, platform_error, system_error, unknown) | [optional]
**error_source** | Option<**ErrorSource**> | Who caused the error: user (fix content/reconnect), platform (outage/API change), system (Late issue, rare) (enum: user, platform, system) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


