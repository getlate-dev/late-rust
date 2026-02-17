# \GmbFoodMenusApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_google_business_food_menus**](GmbFoodMenusApi.md#get_google_business_food_menus) | **GET** /v1/accounts/{accountId}/gmb-food-menus | Get food menus
[**update_google_business_food_menus**](GmbFoodMenusApi.md#update_google_business_food_menus) | **PUT** /v1/accounts/{accountId}/gmb-food-menus | Update food menus



## get_google_business_food_menus

> models::GetGoogleBusinessFoodMenus200Response get_google_business_food_menus(account_id)
Get food menus

Fetches food menus for a connected Google Business Profile location. Returns the full menu structure including sections, items with pricing, dietary info, allergens, and variants. Only available for locations with food menu support (restaurants, cafes, etc.). 

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

Updates the food menus for a connected Google Business Profile location.  Send the full menus array. Use updateMask for partial updates (e.g. \"menus\" to only update the menus field).  Each menu can contain sections, and each section can contain items with pricing, dietary restrictions, allergens, and more. 

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

