# \RedditSearchApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_reddit_feed**](RedditSearchApi.md#get_reddit_feed) | **GET** /v1/reddit/feed | Get subreddit feed
[**search_reddit**](RedditSearchApi.md#search_reddit) | **GET** /v1/reddit/search | Search posts



## get_reddit_feed

> models::GetRedditFeed200Response get_reddit_feed(account_id, subreddit, sort, limit, after, t)
Get subreddit feed

Fetch posts from a subreddit feed. Supports sorting, time filtering, and cursor-based pagination.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**subreddit** | Option<**String**> |  |  |
**sort** | Option<**String**> |  |  |[default to hot]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |
**t** | Option<**String**> |  |  |

### Return type

[**models::GetRedditFeed200Response**](getRedditFeed_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_reddit

> models::SearchReddit200Response search_reddit(account_id, q, subreddit, restrict_sr, sort, limit, after)
Search posts

Search Reddit posts using a connected account. Optionally scope to a specific subreddit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**q** | **String** |  | [required] |
**subreddit** | Option<**String**> |  |  |
**restrict_sr** | Option<**String**> |  |  |
**sort** | Option<**String**> |  |  |[default to new]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**models::SearchReddit200Response**](searchReddit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

