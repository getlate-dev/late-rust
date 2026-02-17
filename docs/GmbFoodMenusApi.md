# \GmbFoodMenusApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_google_business_food_menus**](GmbFoodMenusApi.md#get_google_business_food_menus) | **GET** /v1/accounts/{accountId}/gmb-food-menus | Get food menus
[**update_google_business_food_menus**](GmbFoodMenusApi.md#update_google_business_food_menus) | **PUT** /v1/accounts/{accountId}/gmb-food-menus | Update food menus



## get_google_business_food_menus

> models::GetGoogleBusinessFoodMenus200Response get_google_business_food_menus(account_id)
Get food menus

Returns food menus for a GBP location including sections, items, pricing, and dietary info. Only for locations with food menu support.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Late account ID (from /v1/accounts) | [required] |

### Return type

[**models::GetGoogleBusinessFoodMenus200Response**](getGoogleBusinessFoodMenus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_google_business_food_menus

> models::UpdateGoogleBusinessFoodMenus200Response update_google_business_food_menus(account_id, update_google_business_food_menus_request)
Update food menus

Updates food menus for a GBP location. Send the full menus array. Use updateMask for partial updates.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Late account ID (from /v1/accounts) | [required] |
**update_google_business_food_menus_request** | [**UpdateGoogleBusinessFoodMenusRequest**](UpdateGoogleBusinessFoodMenusRequest.md) |  | [required] |

### Return type

[**models::UpdateGoogleBusinessFoodMenus200Response**](updateGoogleBusinessFoodMenus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

