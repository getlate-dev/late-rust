# RedditPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subreddit** | Option<**String**> | Target subreddit name (without \"r/\" prefix). Overrides the default subreddit configured on the account connection. Use GET /api/v1/accounts/{id}/reddit-subreddits to list available subreddits.  | [optional]
**title** | Option<**String**> | Post title. Defaults to the first line of content, truncated to 300 characters. | [optional]
**url** | Option<**String**> | URL for link posts. If provided (and forceSelf is not true), creates a link post instead of a text post. | [optional]
**force_self** | Option<**bool**> | When true, creates a text/self post even when a URL or media is provided. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


