# \PostsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_upload_posts**](PostsApi.md#bulk_upload_posts) | **POST** /v1/posts/bulk-upload | Validate and schedule multiple posts from CSV
[**create_post**](PostsApi.md#create_post) | **POST** /v1/posts | Create a draft, scheduled, or immediate post
[**delete_post**](PostsApi.md#delete_post) | **DELETE** /v1/posts/{postId} | Delete a post
[**get_post**](PostsApi.md#get_post) | **GET** /v1/posts/{postId} | Get a single post
[**list_posts**](PostsApi.md#list_posts) | **GET** /v1/posts | List posts visible to the authenticated user
[**retry_post**](PostsApi.md#retry_post) | **POST** /v1/posts/{postId}/retry | Retry publishing a failed or partial post
[**unpublish_post**](PostsApi.md#unpublish_post) | **POST** /v1/posts/{postId}/unpublish | Delete a published post from a social media platform
[**update_post**](PostsApi.md#update_post) | **PUT** /v1/posts/{postId} | Update a post



## bulk_upload_posts

> models::BulkUploadPosts200Response bulk_upload_posts(dry_run, file)
Validate and schedule multiple posts from CSV

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
Create a draft, scheduled, or immediate post

**Getting Post URLs:** - For immediate posts (`publishNow: true`): The response includes `platformPostUrl` in each platform entry under `post.platforms[]`. - For scheduled posts: Fetch the post via `GET /v1/posts/{postId}` after the scheduled time; `platformPostUrl` will be populated once published.  **Content/Caption requirements:** - `content` (caption/description) is optional when:   - Media is attached (`mediaItems` or per-platform `customMedia`)   - All platforms have `customContent` set   - Posting only to YouTube (title is used instead) - Text-only posts (no media) require `content` - Stories do not use captions (content is ignored) - Reels, feed posts, and other media posts can have optional captions  Platform constraints: - YouTube requires a video in mediaItems; optional custom thumbnail via MediaItem.thumbnail. - Instagram and TikTok require media; do not mix videos and images for TikTok. - Instagram carousels support up to 10 items; Stories publish as 'story'. - Threads carousels support up to 10 images (no videos in carousels); single posts support one image or video. - Facebook Stories require media (single image or video); set contentType to 'story' in platformSpecificData. - LinkedIn multi-image supports up to 20 images; single PDF documents supported (max 100MB, ~300 pages, cannot mix with other media). - Pinterest supports single image via image_url or a single video per Pin; boardId is required. - Bluesky supports up to 4 images per post. Images may be automatically recompressed to ≤ ~1MB to satisfy Bluesky's blob limit. When no media is attached, a link preview may be generated for URLs in the text. - Snapchat requires media (single image or video); set contentType to 'story', 'saved_story', or 'spotlight' in platformSpecificData. Stories are ephemeral (24h), Saved Stories are permanent, Spotlight is for video content.  **Multi-page/multi-location posting:** Some platforms allow posting to multiple pages, organizations, or locations from a single account connection. Use the same accountId multiple times with different targets in platformSpecificData: - Facebook: `pageId` - post to multiple Facebook Pages (list via GET /v1/accounts/{id}/facebook-page) - LinkedIn: `organizationUrn` - post to multiple organizations (list via GET /v1/accounts/{id}/linkedin-organizations) - Google Business: `locationId` - post to multiple locations (list via GET /v1/accounts/{id}/gmb-locations) - Reddit: `subreddit` - post to multiple subreddits from the same account 

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
Delete a post

Delete a post. Published posts cannot be deleted.  When deleting a scheduled or draft post that consumed upload quota, the quota will be automatically refunded. 

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
Get a single post

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
List posts visible to the authenticated user

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
Retry publishing a failed or partial post

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
Delete a published post from a social media platform

Permanently deletes a published post from the specified social media platform. The post record in Late is kept but its platform status is set to \"cancelled\".  **Supported platforms:** Threads, Facebook, Twitter/X, LinkedIn, YouTube, Pinterest, Reddit, Bluesky, Google Business, Telegram.  **Not supported:** - **Instagram:** No deletion API available. Posts must be deleted manually. - **TikTok:** No deletion API available. Posts must be deleted manually. - **Snapchat:** No deletion API available. Posts must be deleted manually.  **Platform notes:** - **Telegram:** Messages older than 48 hours may fail to delete (Telegram Bot API limitation). - **YouTube:** This permanently deletes the video from YouTube. 

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
Update a post

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

