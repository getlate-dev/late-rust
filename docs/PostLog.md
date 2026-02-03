# PostLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**post_id** | Option<[**models::PostLogPostId**](PostLogPostId.md)> |  | [optional]
**user_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: tiktok, instagram, facebook, youtube, linkedin, twitter, threads, pinterest, reddit, bluesky, googlebusiness, telegram, snapchat) | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**action** | Option<**Action**> | Type of action logged: - `publish` - Initial publish attempt - `retry` - Retry after failure - `media_upload` - Media upload step - `rate_limit_pause` - Account paused due to rate limits - `token_refresh` - Token was refreshed - `cancelled` - Post was cancelled  (enum: publish, retry, media_upload, rate_limit_pause, token_refresh, cancelled) | [optional]
**status** | Option<**Status**> |  (enum: success, failed, pending, skipped) | [optional]
**status_code** | Option<**i32**> | HTTP status code from platform API | [optional]
**endpoint** | Option<**String**> | Platform API endpoint called | [optional]
**request** | Option<[**models::PostLogRequest**](PostLogRequest.md)> |  | [optional]
**response** | Option<[**models::PostLogResponse**](PostLogResponse.md)> |  | [optional]
**duration_ms** | Option<**i32**> | How long the operation took in milliseconds | [optional]
**attempt_number** | Option<**i32**> | Attempt number (1 for first try, 2+ for retries) | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


