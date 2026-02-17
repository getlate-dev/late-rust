# \AccountsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_account**](AccountsApi.md#delete_account) | **DELETE** /v1/accounts/{accountId} | Disconnect account
[**get_account_health**](AccountsApi.md#get_account_health) | **GET** /v1/accounts/{accountId}/health | Check account health
[**get_all_accounts_health**](AccountsApi.md#get_all_accounts_health) | **GET** /v1/accounts/health | Check accounts health
[**get_follower_stats**](AccountsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats
[**list_accounts**](AccountsApi.md#list_accounts) | **GET** /v1/accounts | List accounts
[**update_account**](AccountsApi.md#update_account) | **PUT** /v1/accounts/{accountId} | Update account



## delete_account

> models::DeleteAccountGroup200Response delete_account(account_id)
Disconnect account

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_account_health

> models::GetAccountHealth200Response get_account_health(account_id)
Check account health

Returns detailed health information for a specific social account, including token status, granted permissions, missing permissions, and actionable recommendations. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The account ID to check | [required] |

### Return type

[**models::GetAccountHealth200Response**](getAccountHealth_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_all_accounts_health

> models::GetAllAccountsHealth200Response get_all_accounts_health(profile_id, platform, status)
Check accounts health

Returns the health status of all connected social accounts, including token validity, permissions status, and any issues that need attention. Useful for monitoring account connections and identifying accounts that need reconnection. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform |  |
**status** | Option<**String**> | Filter by health status |  |

### Return type

[**models::GetAllAccountsHealth200Response**](getAllAccountsHealth_200_response.md)

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


## list_accounts

> models::ListAccounts200Response list_accounts(profile_id, include_over_limit)
List accounts

Returns list of connected social accounts. By default, only returns accounts from profiles within the user's plan limit. Follower count data (followersCount, followersLastUpdated) is only included if user has analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter accounts by profile ID |  |
**include_over_limit** | Option<**bool**> | When true, includes accounts from profiles that exceed the user's plan limit. Useful for disconnecting accounts from over-limit profiles so they can be deleted.  |  |[default to false]

### Return type

[**models::ListAccounts200Response**](listAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_account

> models::UpdateAccount200Response update_account(account_id, update_account_request)
Update account

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_account_request** | [**UpdateAccountRequest**](UpdateAccountRequest.md) |  | [required] |

### Return type

[**models::UpdateAccount200Response**](updateAccount_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

