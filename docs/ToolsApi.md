# \ToolsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_instagram_hashtags**](ToolsApi.md#check_instagram_hashtags) | **POST** /v1/tools/instagram/hashtag-checker | Check Instagram hashtag bans
[**download_bluesky_media**](ToolsApi.md#download_bluesky_media) | **GET** /v1/tools/bluesky/download | Download Bluesky media
[**download_facebook_video**](ToolsApi.md#download_facebook_video) | **GET** /v1/tools/facebook/download | Download Facebook video
[**download_instagram_media**](ToolsApi.md#download_instagram_media) | **GET** /v1/tools/instagram/download | Download Instagram media
[**download_linked_in_video**](ToolsApi.md#download_linked_in_video) | **GET** /v1/tools/linkedin/download | Download LinkedIn video
[**download_tik_tok_video**](ToolsApi.md#download_tik_tok_video) | **GET** /v1/tools/tiktok/download | Download TikTok video
[**download_twitter_media**](ToolsApi.md#download_twitter_media) | **GET** /v1/tools/twitter/download | Download Twitter/X media
[**download_you_tube_video**](ToolsApi.md#download_you_tube_video) | **GET** /v1/tools/youtube/download | Download YouTube video
[**get_you_tube_transcript**](ToolsApi.md#get_you_tube_transcript) | **GET** /v1/tools/youtube/transcript | Get YouTube transcript



## check_instagram_hashtags

> models::CheckInstagramHashtags200Response check_instagram_hashtags(check_instagram_hashtags_request)
Check Instagram hashtag bans

Check if Instagram hashtags are banned, restricted, or safe to use.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**check_instagram_hashtags_request** | [**CheckInstagramHashtagsRequest**](CheckInstagramHashtagsRequest.md) |  | [required] |

### Return type

[**models::CheckInstagramHashtags200Response**](checkInstagramHashtags_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_bluesky_media

> models::DownloadBlueskyMedia200Response download_bluesky_media(url)
Download Bluesky media

Download videos from Bluesky posts.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Bluesky post URL | [required] |

### Return type

[**models::DownloadBlueskyMedia200Response**](downloadBlueskyMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_facebook_video

> models::DownloadFacebookVideo200Response download_facebook_video(url)
Download Facebook video

Download videos and reels from Facebook.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Facebook video or reel URL | [required] |

### Return type

[**models::DownloadFacebookVideo200Response**](downloadFacebookVideo_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_instagram_media

> models::DownloadInstagramMedia200Response download_instagram_media(url)
Download Instagram media

Download Instagram reels, posts, or photos.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Instagram reel or post URL | [required] |

### Return type

[**models::DownloadInstagramMedia200Response**](downloadInstagramMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_linked_in_video

> models::DownloadInstagramMedia200Response download_linked_in_video(url)
Download LinkedIn video

Download videos from LinkedIn posts.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | LinkedIn post URL | [required] |

### Return type

[**models::DownloadInstagramMedia200Response**](downloadInstagramMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_tik_tok_video

> models::DownloadTikTokVideo200Response download_tik_tok_video(url, action, format_id)
Download TikTok video

Download TikTok videos with or without watermark.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | TikTok video URL or ID | [required] |
**action** | Option<**String**> | 'formats' to list available formats |  |[default to download]
**format_id** | Option<**String**> | Specific format ID (0 = no watermark, etc.) |  |

### Return type

[**models::DownloadTikTokVideo200Response**](downloadTikTokVideo_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_twitter_media

> models::DownloadInstagramMedia200Response download_twitter_media(url, action, format_id)
Download Twitter/X media

Download videos from Twitter/X posts.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Twitter/X post URL | [required] |
**action** | Option<**String**> |  |  |[default to download]
**format_id** | Option<**String**> |  |  |

### Return type

[**models::DownloadInstagramMedia200Response**](downloadInstagramMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_you_tube_video

> models::DownloadYouTubeVideo200Response download_you_tube_video(url, action, format, quality, format_id)
Download YouTube video

Download YouTube videos or audio. Returns available formats or direct download URL.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | YouTube video URL or video ID | [required] |
**action** | Option<**String**> | Action to perform: 'download' returns download URL, 'formats' lists available formats |  |[default to download]
**format** | Option<**String**> | Desired format (when action=download) |  |[default to video]
**quality** | Option<**String**> | Desired quality (when action=download) |  |[default to hd]
**format_id** | Option<**String**> | Specific format ID from formats list |  |

### Return type

[**models::DownloadYouTubeVideo200Response**](downloadYouTubeVideo_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_transcript

> models::GetYouTubeTranscript200Response get_you_tube_transcript(url, lang)
Get YouTube transcript

Extract transcript/captions from a YouTube video.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | YouTube video URL or video ID | [required] |
**lang** | Option<**String**> | Language code for transcript |  |[default to en]

### Return type

[**models::GetYouTubeTranscript200Response**](getYouTubeTranscript_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

