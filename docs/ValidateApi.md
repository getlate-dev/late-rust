# \ValidateApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**validate_media**](ValidateApi.md#validate_media) | **POST** /v1/tools/validate/media | Validate media URL
[**validate_post**](ValidateApi.md#validate_post) | **POST** /v1/tools/validate/post | Validate post content
[**validate_post_length**](ValidateApi.md#validate_post_length) | **POST** /v1/tools/validate/post-length | Validate post character count
[**validate_subreddit**](ValidateApi.md#validate_subreddit) | **GET** /v1/tools/validate/subreddit | Check subreddit existence



## validate_media

> models::ValidateMedia200Response validate_media(validate_media_request)
Validate media URL

Check if a media URL is accessible and return metadata (content type, file size) plus per-platform size limit comparisons.  Performs a HEAD request (with GET fallback) to detect content type and size. Rejects private/localhost URLs for SSRF protection.  Platform limits are sourced from each platform's actual upload constraints. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_media_request** | [**ValidateMediaRequest**](ValidateMediaRequest.md) |  | [required] |

### Return type

[**models::ValidateMedia200Response**](validateMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_post

> models::ValidatePost200Response validate_post(validate_post_request)
Validate post content

Dry-run the full post validation pipeline without publishing. Catches issues like missing media for Instagram/TikTok/YouTube, hashtag limits, invalid thread formats, Facebook Reel requirements, and character limit violations.  Accepts the same body as `POST /v1/posts`. Does NOT validate accounts, process media, or track usage. This is content-only validation.  Returns errors for failures and warnings for near-limit content (>90% of character limit). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_post_request** | [**ValidatePostRequest**](ValidatePostRequest.md) |  | [required] |

### Return type

[**models::ValidatePost200Response**](validatePost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_post_length

> models::ValidatePostLength200Response validate_post_length(validate_post_length_request)
Validate post character count

Check weighted character count per platform and whether the text is within each platform's limit.  Twitter/X uses weighted counting (URLs = 23 chars via t.co, emojis = 2 chars). All other platforms use plain character length.  Returns counts and limits for all 15 supported platform variants. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_post_length_request** | [**ValidatePostLengthRequest**](ValidatePostLengthRequest.md) |  | [required] |

### Return type

[**models::ValidatePostLength200Response**](validatePostLength_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_subreddit

> models::ValidateSubreddit200Response validate_subreddit(name)
Check subreddit existence

Check if a subreddit exists and return basic info (title, subscriber count, NSFW status, post types allowed).  Uses Reddit's public JSON API (no Reddit auth needed). Returns `exists: false` for private, banned, or nonexistent subreddits. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**name** | **String** | Subreddit name (with or without \"r/\" prefix) | [required] |

### Return type

[**models::ValidateSubreddit200Response**](validateSubreddit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

