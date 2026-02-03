# \AnalyticsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_analytics**](AnalyticsApi.md#get_analytics) | **GET** /v1/analytics | Unified analytics for posts
[**get_follower_stats**](AnalyticsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats and growth metrics
[**get_linked_in_aggregate_analytics**](AnalyticsApi.md#get_linked_in_aggregate_analytics) | **GET** /v1/accounts/{accountId}/linkedin-aggregate-analytics | Get aggregate analytics for a LinkedIn personal account
[**get_linked_in_post_analytics**](AnalyticsApi.md#get_linked_in_post_analytics) | **GET** /v1/accounts/{accountId}/linkedin-post-analytics | Get analytics for a specific LinkedIn post by URN
[**get_you_tube_daily_views**](AnalyticsApi.md#get_you_tube_daily_views) | **GET** /v1/analytics/youtube/daily-views | YouTube daily views breakdown



## get_analytics

> models::GetAnalytics200Response get_analytics(post_id, platform, profile_id, source, from_date, to_date, limit, page, sort_by, order)
Unified analytics for posts

Returns analytics for posts. If postId is provided, returns analytics for a single post. Otherwise returns a paginated list of posts with overview stats.  **Important: Understanding Post IDs**  This endpoint uses two types of posts: - **Late Posts** - Posts scheduled/created via the Late API (e.g., via `POST /v1/posts`) - **External Posts** - Posts synced from social platforms for analytics tracking  When you schedule a post via Late and it gets published, **both** records exist: 1. The original Late Post (returned when you created the post) 2. An External Post (created when we sync analytics from the platform)  **List endpoint behavior:** - Returns External Post IDs (`_id` field) - Use the `isExternal` field to identify post origin:   - `isExternal: true` - Synced from platform (may have been originally scheduled via Late)   - `isExternal: false` - Late-scheduled post (shown when querying by Late post ID)  **Single post behavior (`postId` parameter):** - Accepts **both** Late Post IDs and External Post IDs - If you pass a Late Post ID, the API automatically resolves it to the corresponding External Post analytics - Both return the same analytics data for the same underlying social media post  **Correlating posts:** Use `latePostId` to link analytics entries back to the original post created via `POST /v1/posts`. This field contains the Late Post ID when the external post originated from Late. Alternatively, use `platformPostUrl` (e.g., `https://www.instagram.com/reel/ABC123/`) as a stable identifier.  **Note:** For follower count history and growth metrics, use the dedicated `/v1/accounts/follower-stats` endpoint.  **LinkedIn Analytics:** - **Personal Accounts:** Per-post analytics available for posts published through Late. External posts cannot be synced due to LinkedIn API restrictions. - **Organization Accounts:** Full analytics support including external post syncing.  **Telegram Analytics:** - **Not available.** The Telegram Bot API does not provide message view counts, forwards, or engagement metrics. This is a Telegram platform limitation, not a Late limitation. View counts are only visible to channel admins in the Telegram app.  **Data Freshness:** Analytics data is cached and refreshed at most once per hour. When you call this endpoint, if the cache is older than 60 minutes, a background refresh is triggered and you'll see updated data on subsequent requests. There is no rate limit on API requests. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Returns analytics for a single post. Accepts both Late Post IDs (from `POST /v1/posts`)  and External Post IDs (from this endpoint's list response). The API automatically  resolves Late Post IDs to their corresponding External Post analytics.  |  |
**platform** | Option<**String**> | Filter by platform (default \"all\") |  |
**profile_id** | Option<**String**> | Filter by profile ID (default \"all\") |  |
**source** | Option<**String**> | Filter by post source: - `late` - Only posts scheduled/published via Late API - `external` - Only posts synced from the platform (not posted via Late) - `all` - All posts (default)  |  |[default to all]
**from_date** | Option<**String**> | Inclusive lower bound |  |
**to_date** | Option<**String**> | Inclusive upper bound |  |
**limit** | Option<**i32**> | Page size (default 50) |  |[default to 50]
**page** | Option<**i32**> | Page number (default 1) |  |[default to 1]
**sort_by** | Option<**String**> | Sort by date or engagement |  |[default to date]
**order** | Option<**String**> | Sort order |  |[default to desc]

### Return type

[**models::GetAnalytics200Response**](getAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_follower_stats

> models::GetFollowerStats200Response get_follower_stats(account_ids, profile_id, from_date, to_date, granularity)
Get follower stats and growth metrics

Returns follower count history and growth metrics for connected social accounts. **Requires analytics add-on subscription.**  **Data Freshness:** Follower counts are automatically refreshed once per day. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<**String**> | Comma-separated list of account IDs (optional, defaults to all user's accounts) |  |
**profile_id** | Option<**String**> | Filter by profile ID |  |
**from_date** | Option<**String**> | Start date in YYYY-MM-DD format (defaults to 30 days ago) |  |
**to_date** | Option<**String**> | End date in YYYY-MM-DD format (defaults to today) |  |
**granularity** | Option<**String**> | Data aggregation level |  |[default to daily]

### Return type

[**models::GetFollowerStats200Response**](getFollowerStats_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_aggregate_analytics

> models::GetLinkedInAggregateAnalytics200Response get_linked_in_aggregate_analytics(account_id, aggregation, start_date, end_date, metrics)
Get aggregate analytics for a LinkedIn personal account

Returns aggregate analytics across ALL posts for a LinkedIn personal account. Uses LinkedIn's `memberCreatorPostAnalytics` API with `q=me` finder.  **Important:** This endpoint only works for LinkedIn **personal** accounts. Organization accounts should use the standard `/v1/analytics` endpoint for per-post analytics.  **Required Scope:** `r_member_postAnalytics`  If the connected account doesn't have this scope, you'll receive a 403 error with instructions to reconnect.  **Aggregation Options:** - `TOTAL` (default): Returns lifetime totals for all metrics - `DAILY`: Returns daily breakdown of metrics over time  **Available Metrics:** - `IMPRESSION`: Number of times posts were displayed - `MEMBERS_REACHED`: Unique members who saw posts (NOT available with DAILY aggregation) - `REACTION`: Total reactions (likes, celebrates, etc.) - `COMMENT`: Total comments - `RESHARE`: Total reshares/reposts  **Date Range Filtering:** Use `startDate` and `endDate` parameters to filter analytics to a specific time period. If omitted, returns lifetime analytics.  **LinkedIn API Limitation:** The combination of `MEMBERS_REACHED` + `DAILY` aggregation is not supported by LinkedIn's API. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the LinkedIn personal account | [required] |
**aggregation** | Option<**String**> | Type of aggregation for the analytics data. - `TOTAL` (default): Returns single totals for each metric - `DAILY`: Returns daily breakdown of metrics  Note: `MEMBERS_REACHED` metric is not available with `DAILY` aggregation.  |  |[default to TOTAL]
**start_date** | Option<**String**> | Start date for analytics data in YYYY-MM-DD format. If provided without endDate, endDate defaults to today. If omitted entirely, returns lifetime analytics.  |  |
**end_date** | Option<**String**> | End date for analytics data in YYYY-MM-DD format (exclusive). If provided without startDate, startDate defaults to 30 days before endDate.  |  |
**metrics** | Option<**String**> | Comma-separated list of metrics to fetch. If omitted, fetches all available metrics. Valid values: IMPRESSION, MEMBERS_REACHED, REACTION, COMMENT, RESHARE  |  |

### Return type

[**models::GetLinkedInAggregateAnalytics200Response**](getLinkedInAggregateAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_post_analytics

> models::GetLinkedInPostAnalytics200Response get_linked_in_post_analytics(account_id, urn)
Get analytics for a specific LinkedIn post by URN

Returns analytics for a specific LinkedIn post using its URN. Works for both personal and organization accounts.  This is useful for fetching analytics of posts that weren't published through Late, as long as you have the post URN.  **For Personal Accounts:** - Uses `memberCreatorPostAnalytics` API + `memberCreatorVideoAnalytics` for video posts - Requires `r_member_postAnalytics` scope - Available metrics: impressions, reach, likes, comments, shares, video views (video posts only) - **Clicks are NOT available** for personal accounts  **For Organization Accounts:** - Uses `organizationalEntityShareStatistics` API + `videoAnalytics` for video posts - Requires `r_organization_social` scope - Available metrics: impressions, reach, clicks, likes, comments, shares, video views (video posts only), engagement rate 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the LinkedIn account | [required] |
**urn** | **String** | The LinkedIn post URN | [required] |

### Return type

[**models::GetLinkedInPostAnalytics200Response**](getLinkedInPostAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_daily_views

> models::YouTubeDailyViewsResponse get_you_tube_daily_views(video_id, account_id, start_date, end_date)
YouTube daily views breakdown

Returns historical daily view counts for a specific YouTube video. Uses YouTube Analytics API v2 to fetch daily breakdowns including views, watch time, and subscriber changes.  **Required Scope:** This endpoint requires the `yt-analytics.readonly` OAuth scope. Existing YouTube accounts may need to re-authorize to grant this permission. If the scope is missing, the response will include a `reauthorizeUrl`.  **Data Latency:** YouTube Analytics data has a 2-3 day delay. The `endDate` is automatically capped to 3 days ago.  **Date Range:** Maximum 90 days of historical data available. Defaults to last 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** | The YouTube video ID (e.g., \"dQw4w9WgXcQ\") | [required] |
**account_id** | **String** | The Late account ID for the YouTube account | [required] |
**start_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**end_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to 3 days ago (YouTube data latency). |  |

### Return type

[**models::YouTubeDailyViewsResponse**](YouTubeDailyViewsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

