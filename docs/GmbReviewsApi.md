# \GmbReviewsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_google_business_reviews**](GmbReviewsApi.md#get_google_business_reviews) | **GET** /v1/accounts/{accountId}/gmb-reviews | Get reviews



## get_google_business_reviews

> models::GetGoogleBusinessReviews200Response get_google_business_reviews(account_id, page_size, page_token)
Get reviews

Returns reviews for a GBP account including ratings, comments, and owner replies. Use nextPageToken for pagination.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Late account ID (from /v1/accounts) | [required] |
**page_size** | Option<**i32**> | Number of reviews to fetch per page (max 50) |  |[default to 50]
**page_token** | Option<**String**> | Pagination token from previous response |  |

### Return type

[**models::GetGoogleBusinessReviews200Response**](getGoogleBusinessReviews_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

