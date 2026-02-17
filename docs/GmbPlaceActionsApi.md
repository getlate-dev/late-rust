# \GmbPlaceActionsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_google_business_place_action**](GmbPlaceActionsApi.md#create_google_business_place_action) | **POST** /v1/accounts/{accountId}/gmb-place-actions | Create action link
[**delete_google_business_place_action**](GmbPlaceActionsApi.md#delete_google_business_place_action) | **DELETE** /v1/accounts/{accountId}/gmb-place-actions | Delete action link
[**list_google_business_place_actions**](GmbPlaceActionsApi.md#list_google_business_place_actions) | **GET** /v1/accounts/{accountId}/gmb-place-actions | List action links



## create_google_business_place_action

> models::CreateGoogleBusinessPlaceAction200Response create_google_business_place_action(account_id, create_google_business_place_action_request)
Create action link

Creates a place action link for a location.  Available action types: - `APPOINTMENT` - Booking an appointment - `ONLINE_APPOINTMENT` - Booking an online appointment - `DINING_RESERVATION` - Making a dining reservation (OpenTable, Resy, etc.) - `FOOD_ORDERING` - Ordering food for delivery and/or takeout (DoorDash, Uber Eats, etc.) - `FOOD_DELIVERY` - Ordering food for delivery only - `FOOD_TAKEOUT` - Ordering food for takeout only - `SHOP_ONLINE` - Shopping with delivery and/or pickup 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**create_google_business_place_action_request** | [**CreateGoogleBusinessPlaceActionRequest**](CreateGoogleBusinessPlaceActionRequest.md) |  | [required] |

### Return type

[**models::CreateGoogleBusinessPlaceAction200Response**](createGoogleBusinessPlaceAction_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_google_business_place_action

> models::DeleteGoogleBusinessPlaceAction200Response delete_google_business_place_action(account_id, name)
Delete action link

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**name** | **String** | The resource name of the place action link (e.g. locations/123/placeActionLinks/456) | [required] |

### Return type

[**models::DeleteGoogleBusinessPlaceAction200Response**](deleteGoogleBusinessPlaceAction_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_google_business_place_actions

> models::ListGoogleBusinessPlaceActions200Response list_google_business_place_actions(account_id, page_size, page_token)
List action links

Lists place action links for a Google Business Profile location.  Place actions are the booking, ordering, and reservation buttons that appear on your listing. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**page_size** | Option<**i32**> |  |  |[default to 100]
**page_token** | Option<**String**> |  |  |

### Return type

[**models::ListGoogleBusinessPlaceActions200Response**](listGoogleBusinessPlaceActions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

