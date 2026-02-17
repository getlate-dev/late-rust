# \AnalyticsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_analytics**](AnalyticsApi.md#get_analytics) | **GET** /v1/analytics | Get post analytics
[**get_follower_stats**](AnalyticsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats
[**get_linked_in_aggregate_analytics**](AnalyticsApi.md#get_linked_in_aggregate_analytics) | **GET** /v1/accounts/{accountId}/linkedin-aggregate-analytics | Get LinkedIn aggregate stats
[**get_linked_in_post_analytics**](AnalyticsApi.md#get_linked_in_post_analytics) | **GET** /v1/accounts/{accountId}/linkedin-post-analytics | Get LinkedIn post stats
[**get_you_tube_daily_views**](AnalyticsApi.md#get_you_tube_daily_views) | **GET** /v1/analytics/youtube/daily-views | Get YouTube daily views



## get_analytics

> models::GetAnalytics200Response get_analytics(post_id, platform, profile_id, source, from_date, to_date, limit, page, sort_by, order)
Get post analytics

Returns analytics for posts. With postId, returns a single post. Without it, returns a paginated list with overview stats. This endpoint returns External Post IDs by default. The postId parameter accepts both Late Post IDs and External Post IDs, auto-resolving Late IDs to External Post analytics. Use latePostId in responses to link back to your original post, or platformPostUrl as a stable identifier. isExternal indicates post origin (true = synced from platform). For follower stats, use /v1/accounts/follower-stats. LinkedIn personal accounts: per-post analytics only for Late-published posts. Telegram: not available. Data is cached and refreshed at most once per hour. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Returns analytics for a single post. Accepts both Late Post IDs and External Post IDs. Late IDs are auto-resolved to External Post analytics. |  |
**platform** | Option<**String**> | Filter by platform (default \"all\") |  |
**profile_id** | Option<**String**> | Filter by profile ID (default \"all\") |  |
**source** | Option<**String**> | Filter by post source: late (posted via Late API), external (synced from platform), all (default) |  |[default to all]
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
Get follower stats

Returns follower count history and growth metrics for connected social accounts. Requires analytics add-on subscription. Follower counts are refreshed once per day. 

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
Get LinkedIn aggregate stats

Returns aggregate analytics across all posts for a LinkedIn personal account. Org accounts should use /v1/analytics instead. Required scope: r_member_postAnalytics (missing scope returns 403). Aggregation: TOTAL (default, lifetime totals) or DAILY (time series). Use startDate/endDate to filter. MEMBERS_REACHED is not available with DAILY aggregation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the LinkedIn personal account | [required] |
**aggregation** | Option<**String**> | Type of aggregation: TOTAL (default, returns single totals) or DAILY (returns daily breakdown). Note: MEMBERS_REACHED is not available with DAILY aggregation.  |  |[default to TOTAL]
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
Get LinkedIn post stats

Returns analytics for a specific LinkedIn post using its URN. Works for both personal and organization accounts. Useful for fetching analytics of posts not published through Late. Personal accounts require r_member_postAnalytics scope and return impressions, reach, likes, comments, shares, and video views (clicks not available). Organization accounts require r_organization_social scope and additionally return clicks and engagement rate. 

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
Get YouTube daily views

Returns historical daily view counts for a specific YouTube video. Uses YouTube Analytics API v2 to fetch daily breakdowns including views, watch time, and subscriber changes.  Requires the yt-analytics.readonly OAuth scope. Existing YouTube accounts may need to re-authorize. If the scope is missing, the response includes a reauthorizeUrl. Data has a 2-3 day delay; endDate is automatically capped to 3 days ago. Maximum 90 days of historical data. Defaults to last 30 days. 

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

