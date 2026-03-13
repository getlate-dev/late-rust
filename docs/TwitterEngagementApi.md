# \TwitterEngagementApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bookmark_post**](TwitterEngagementApi.md#bookmark_post) | **POST** /v1/twitter/bookmark | Bookmark a tweet
[**follow_user**](TwitterEngagementApi.md#follow_user) | **POST** /v1/twitter/follow | Follow a user
[**remove_bookmark**](TwitterEngagementApi.md#remove_bookmark) | **DELETE** /v1/twitter/bookmark | Remove bookmark
[**retweet_post**](TwitterEngagementApi.md#retweet_post) | **POST** /v1/twitter/retweet | Retweet a post
[**undo_retweet**](TwitterEngagementApi.md#undo_retweet) | **DELETE** /v1/twitter/retweet | Undo retweet
[**unfollow_user**](TwitterEngagementApi.md#unfollow_user) | **DELETE** /v1/twitter/follow | Unfollow a user



## bookmark_post

> models::BookmarkPost200Response bookmark_post(bookmark_post_request)
Bookmark a tweet

Bookmark a tweet by ID. Requires the bookmark.write OAuth scope. Rate limit: 50 requests per 15-min window. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bookmark_post_request** | [**BookmarkPostRequest**](BookmarkPostRequest.md) |  | [required] |

### Return type

[**models::BookmarkPost200Response**](bookmarkPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## follow_user

> models::FollowUser200Response follow_user(follow_user_request)
Follow a user

Follow a user on X/Twitter. Requires the follows.write OAuth scope. For protected accounts, a follow request is sent instead (pending_follow will be true). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**follow_user_request** | [**FollowUserRequest**](FollowUserRequest.md) |  | [required] |

### Return type

[**models::FollowUser200Response**](followUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_bookmark

> models::RemoveBookmark200Response remove_bookmark(account_id, tweet_id)
Remove bookmark

Remove a bookmark from a tweet. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tweet_id** | **String** | The ID of the tweet to unbookmark | [required] |

### Return type

[**models::RemoveBookmark200Response**](removeBookmark_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## retweet_post

> models::RetweetPost200Response retweet_post(retweet_post_request)
Retweet a post

Retweet (repost) a tweet by ID. Rate limit: 50 requests per 15-min window. Shares the 300/3hr creation limit with tweet creation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**retweet_post_request** | [**RetweetPostRequest**](RetweetPostRequest.md) |  | [required] |

### Return type

[**models::RetweetPost200Response**](retweetPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## undo_retweet

> models::UndoRetweet200Response undo_retweet(account_id, tweet_id)
Undo retweet

Undo a retweet (un-repost a tweet). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tweet_id** | **String** | The ID of the original tweet to un-retweet | [required] |

### Return type

[**models::UndoRetweet200Response**](undoRetweet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unfollow_user

> models::UnfollowUser200Response unfollow_user(account_id, target_user_id)
Unfollow a user

Unfollow a user on X/Twitter. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**target_user_id** | **String** | The Twitter ID of the user to unfollow | [required] |

### Return type

[**models::UnfollowUser200Response**](unfollowUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

