# \CommentsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_inbox_comment**](CommentsApi.md#delete_inbox_comment) | **DELETE** /v1/inbox/comments/{postId} | Delete a comment
[**get_inbox_post_comments**](CommentsApi.md#get_inbox_post_comments) | **GET** /v1/inbox/comments/{postId} | Get comments for a post
[**hide_inbox_comment**](CommentsApi.md#hide_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/hide | Hide a comment
[**like_inbox_comment**](CommentsApi.md#like_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/like | Like a comment
[**list_inbox_comments**](CommentsApi.md#list_inbox_comments) | **GET** /v1/inbox/comments | List posts with comments across all accounts
[**reply_to_inbox_post**](CommentsApi.md#reply_to_inbox_post) | **POST** /v1/inbox/comments/{postId} | Reply to a post or comment
[**send_private_reply_to_comment**](CommentsApi.md#send_private_reply_to_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/private-reply | Send private reply to comment author
[**unhide_inbox_comment**](CommentsApi.md#unhide_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/hide | Unhide a comment
[**unlike_inbox_comment**](CommentsApi.md#unlike_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/like | Unlike a comment



## delete_inbox_comment

> models::DeleteInboxComment200Response delete_inbox_comment(post_id, account_id, comment_id)
Delete a comment

Delete a comment on a post. Supported by Facebook, Instagram, Bluesky, Reddit, YouTube, LinkedIn, and TikTok. Requires accountId and commentId query parameters. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The post identifier. Accepts a Late post ID or a platform-specific post ID. | [required] |
**account_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |

### Return type

[**models::DeleteInboxComment200Response**](deleteInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_post_comments

> models::GetInboxPostComments200Response get_inbox_post_comments(post_id, account_id, subreddit, limit, cursor, comment_id)
Get comments for a post

Fetch comments for a specific post. Requires accountId query parameter.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The post identifier. Accepts a Late post ID (MongoDB ObjectId) which is automatically resolved to the platform-specific post ID, or a platform-specific post ID directly (e.g. tweet ID, Facebook Graph ID, YouTube video ID). | [required] |
**account_id** | **String** |  | [required] |
**subreddit** | Option<**String**> | (Reddit only) Subreddit name |  |
**limit** | Option<**i32**> | Maximum number of comments to return |  |[default to 25]
**cursor** | Option<**String**> | Pagination cursor |  |
**comment_id** | Option<**String**> | (Reddit only) Get replies to a specific comment |  |

### Return type

[**models::GetInboxPostComments200Response**](getInboxPostComments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## hide_inbox_comment

> models::HideInboxComment200Response hide_inbox_comment(post_id, comment_id, hide_inbox_comment_request)
Hide a comment

Hide a comment on a post. Supported by Facebook, Instagram, and Threads. Hidden comments are only visible to the commenter and page admin. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**hide_inbox_comment_request** | [**HideInboxCommentRequest**](HideInboxCommentRequest.md) |  | [required] |

### Return type

[**models::HideInboxComment200Response**](hideInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## like_inbox_comment

> models::LikeInboxComment200Response like_inbox_comment(post_id, comment_id, like_inbox_comment_request)
Like a comment

Like or upvote a comment on a post.  **Supported platforms:** Facebook, Twitter/X, Bluesky, Reddit  For Bluesky, the `cid` (content identifier) is required in the request body. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**like_inbox_comment_request** | [**LikeInboxCommentRequest**](LikeInboxCommentRequest.md) |  | [required] |

### Return type

[**models::LikeInboxComment200Response**](likeInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_comments

> models::ListInboxComments200Response list_inbox_comments(profile_id, platform, min_comments, since, sort_by, sort_order, limit, cursor, account_id)
List posts with comments across all accounts

Fetch posts with their comment counts from all connected accounts. Aggregates data from multiple accounts in a single API call.  **Supported platforms:** Facebook, Instagram, Twitter/X, Bluesky, Threads, YouTube, LinkedIn, Reddit, TikTok (write-only) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform |  |
**min_comments** | Option<**i32**> | Minimum comment count |  |
**since** | Option<**String**> | Posts created after this date |  |
**sort_by** | Option<**String**> | Sort field |  |[default to date]
**sort_order** | Option<**String**> | Sort order |  |[default to desc]
**limit** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Filter by specific social account ID |  |

### Return type

[**models::ListInboxComments200Response**](listInboxComments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_to_inbox_post

> models::ReplyToInboxPost200Response reply_to_inbox_post(post_id, reply_to_inbox_post_request)
Reply to a post or comment

Post a reply to a post or specific comment. Requires accountId in request body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The post identifier. Accepts a Late post ID or a platform-specific post ID. | [required] |
**reply_to_inbox_post_request** | [**ReplyToInboxPostRequest**](ReplyToInboxPostRequest.md) |  | [required] |

### Return type

[**models::ReplyToInboxPost200Response**](replyToInboxPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_private_reply_to_comment

> models::SendPrivateReplyToComment200Response send_private_reply_to_comment(post_id, comment_id, send_private_reply_to_comment_request)
Send private reply to comment author

Send a private direct message to the author of a comment on your post. This is useful for handling customer inquiries or sensitive matters privately.  **Supported platforms:** Instagram, Facebook  **Limitations:** - Only ONE private reply per comment (platform API restriction) - Must be sent within 7 days of the comment being posted - Only works for comments on posts owned by the connected account - Text only (no media attachments) - Instagram: message goes to the user's Inbox (if they follow you) or Message Requests (if they don't). Requires `instagram_business_manage_messages` permission. - Facebook: message opens a Messenger conversation with the commenter. Requires `pages_messaging` permission.  **Note:** Both permissions are already included in Late's OAuth flow. This does not create a conversation thread until the user replies back. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The media/post ID (Instagram media ID or Facebook post ID) | [required] |
**comment_id** | **String** | The comment ID to send a private reply to | [required] |
**send_private_reply_to_comment_request** | [**SendPrivateReplyToCommentRequest**](SendPrivateReplyToCommentRequest.md) |  | [required] |

### Return type

[**models::SendPrivateReplyToComment200Response**](sendPrivateReplyToComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unhide_inbox_comment

> models::HideInboxComment200Response unhide_inbox_comment(post_id, comment_id, account_id)
Unhide a comment

Unhide a previously hidden comment. Supported by Facebook, Instagram, and Threads. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::HideInboxComment200Response**](hideInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unlike_inbox_comment

> models::UnlikeInboxComment200Response unlike_inbox_comment(post_id, comment_id, account_id, like_uri)
Unlike a comment

Remove a like from a comment.  **Supported platforms:** Facebook, Twitter/X, Bluesky, Reddit  For Bluesky, the `likeUri` query parameter is required. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**like_uri** | Option<**String**> | (Bluesky only) The like URI returned when liking |  |

### Return type

[**models::UnlikeInboxComment200Response**](unlikeInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

