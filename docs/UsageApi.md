# \UsageApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_usage_stats**](UsageApi.md#get_usage_stats) | **GET** /v1/usage-stats | Get plan and usage stats



## get_usage_stats

> models::UsageStats get_usage_stats()
Get plan and usage stats

Returns the current plan name, billing period, plan limits, and usage counts.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::UsageStats**](UsageStats.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

