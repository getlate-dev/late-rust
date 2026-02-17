# \PostsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_upload_posts**](PostsApi.md#bulk_upload_posts) | **POST** /v1/posts/bulk-upload | Bulk upload from CSV
[**create_post**](PostsApi.md#create_post) | **POST** /v1/posts | Create post
[**delete_post**](PostsApi.md#delete_post) | **DELETE** /v1/posts/{postId} | Delete post
[**get_post**](PostsApi.md#get_post) | **GET** /v1/posts/{postId} | Get post
[**list_posts**](PostsApi.md#list_posts) | **GET** /v1/posts | List posts
[**retry_post**](PostsApi.md#retry_post) | **POST** /v1/posts/{postId}/retry | Retry failed post
[**unpublish_post**](PostsApi.md#unpublish_post) | **POST** /v1/posts/{postId}/unpublish | Unpublish post
[**update_post**](PostsApi.md#update_post) | **PUT** /v1/posts/{postId} | Update post



## bulk_upload_posts

> models::BulkUploadPosts200Response bulk_upload_posts(dry_run, file)
Bulk upload from CSV

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dry_run** | Option<**bool**> |  |  |[default to false]
**file** | Option<**std::path::PathBuf**> |  |  |

### Return type

[**models::BulkUploadPosts200Response**](bulkUploadPosts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_post

> models::PostCreateResponse create_post(create_post_request)
Create post

**Getting Post URLs:** - Immediate posts (`publishNow: true`): response includes `platformPostUrl` in `post.platforms[]`. - Scheduled posts: fetch via `GET /v1/posts/{postId}` after publish time for `platformPostUrl`.  **Content requirements:** - `content` is optional when media is attached, all platforms have `customContent`, or posting to YouTube only. - Text-only posts require `content`. Stories ignore captions.  **Platform constraints:** - YouTube: video required, optional thumbnail via `MediaItem.thumbnail` - Instagram/TikTok: media required; TikTok cannot mix videos and images - Instagram carousels: up to 10 items; Threads carousels: up to 10 images only - Facebook Stories: single image or video, set `contentType: 'story'` - LinkedIn: up to 20 images or a single PDF (max 100MB) - Pinterest: single image or video, `boardId` required - Bluesky: up to 4 images, auto-recompressed to ~1MB - Snapchat: single image or video, set `contentType` in platformSpecificData 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_post_request** | [**CreatePostRequest**](CreatePostRequest.md) |  | [required] |

### Return type

[**models::PostCreateResponse**](PostCreateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_post

> models::PostDeleteResponse delete_post(post_id)
Delete post

Delete a draft or scheduled post from Late. Only posts that have not been published can be deleted. To remove a published post from a social media platform, use the [Unpublish endpoint](#tag/Posts/operation/unpublishPost) instead. When deleting a scheduled or draft post that consumed upload quota, the quota will be automatically refunded. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |

### Return type

[**models::PostDeleteResponse**](PostDeleteResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post

> models::PostGetResponse get_post(post_id)
Get post

Fetch a single post by ID. For published posts, this returns `platformPostUrl`  for each platform - useful for retrieving post URLs after scheduled posts publish. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |

### Return type

[**models::PostGetResponse**](PostGetResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_posts

> models::PostsListResponse list_posts(page, limit, status, platform, profile_id, created_by, date_from, date_to, include_hidden)
List posts

**Getting Post URLs:** For published posts, each platform entry includes `platformPostUrl` with the public URL. Use `status=published` filter to fetch only published posts with their URLs.  Notes and constraints by platform when interpreting the response: - YouTube: posts always include at least one video in mediaItems. - Instagram/TikTok: posts always include media; drafts may omit media until finalized in client. - TikTok: mediaItems will not mix photos and videos in the same post. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> | Page size |  |[default to 10]
**status** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**created_by** | Option<**String**> |  |  |
**date_from** | Option<**String**> |  |  |
**date_to** | Option<**String**> |  |  |
**include_hidden** | Option<**bool**> |  |  |[default to false]

### Return type

[**models::PostsListResponse**](PostsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## retry_post

> models::PostRetryResponse retry_post(post_id)
Retry failed post

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |

### Return type

[**models::PostRetryResponse**](PostRetryResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unpublish_post

> models::UnpublishPost200Response unpublish_post(post_id, unpublish_post_request)
Unpublish post

Permanently deletes a published post from the specified social media platform. The post record in Late is kept but its platform status is updated to \"cancelled\". This does not delete the post from Late, only from the platform.  **Supported platforms:** Threads, Facebook, Twitter/X, LinkedIn, YouTube, Pinterest, Reddit, Bluesky, Google Business, Telegram.  **Not supported:** - **Instagram:** No deletion API available. Posts must be deleted manually. - **TikTok:** No deletion API available. Posts must be deleted manually. - **Snapchat:** No deletion API available. Posts must be deleted manually.  **Platform notes:** - **Threaded posts (Twitter, Threads, Bluesky):** If the post was published as a thread, all items in the thread are deleted (not just the first one). Posts published before this feature was added will only have the first item deleted. - **Telegram:** Messages older than 48 hours may fail to delete (Telegram Bot API limitation). - **YouTube:** This permanently deletes the video from YouTube. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**unpublish_post_request** | [**UnpublishPostRequest**](UnpublishPostRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_post

> models::PostUpdateResponse update_post(post_id, update_post_request)
Update post

Update an existing post. Only draft, scheduled, failed, and partial posts can be edited. Published, publishing, and cancelled posts cannot be modified. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**update_post_request** | [**UpdatePostRequest**](UpdatePostRequest.md) |  | [required] |

### Return type

[**models::PostUpdateResponse**](PostUpdateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

