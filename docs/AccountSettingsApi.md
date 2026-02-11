# \AccountSettingsApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_instagram_ice_breakers**](AccountSettingsApi.md#delete_instagram_ice_breakers) | **DELETE** /v1/accounts/{accountId}/instagram-ice-breakers | Delete Instagram ice breakers
[**delete_messenger_menu**](AccountSettingsApi.md#delete_messenger_menu) | **DELETE** /v1/accounts/{accountId}/messenger-menu | Delete Facebook persistent menu
[**delete_telegram_commands**](AccountSettingsApi.md#delete_telegram_commands) | **DELETE** /v1/accounts/{accountId}/telegram-commands | Delete Telegram bot commands
[**get_instagram_ice_breakers**](AccountSettingsApi.md#get_instagram_ice_breakers) | **GET** /v1/accounts/{accountId}/instagram-ice-breakers | Get Instagram ice breakers
[**get_messenger_menu**](AccountSettingsApi.md#get_messenger_menu) | **GET** /v1/accounts/{accountId}/messenger-menu | Get Facebook persistent menu
[**get_telegram_commands**](AccountSettingsApi.md#get_telegram_commands) | **GET** /v1/accounts/{accountId}/telegram-commands | Get Telegram bot commands
[**set_instagram_ice_breakers**](AccountSettingsApi.md#set_instagram_ice_breakers) | **PUT** /v1/accounts/{accountId}/instagram-ice-breakers | Set Instagram ice breakers
[**set_messenger_menu**](AccountSettingsApi.md#set_messenger_menu) | **PUT** /v1/accounts/{accountId}/messenger-menu | Set Facebook persistent menu
[**set_telegram_commands**](AccountSettingsApi.md#set_telegram_commands) | **PUT** /v1/accounts/{accountId}/telegram-commands | Set Telegram bot commands



## delete_instagram_ice_breakers

> delete_instagram_ice_breakers(account_id)
Delete Instagram ice breakers

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_messenger_menu

> delete_messenger_menu(account_id)
Delete Facebook persistent menu

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_telegram_commands

> delete_telegram_commands(account_id)
Delete Telegram bot commands

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_ice_breakers

> models::GetMessengerMenu200Response get_instagram_ice_breakers(account_id)
Get Instagram ice breakers

Get the ice breaker configuration for an Instagram account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetMessengerMenu200Response**](getMessengerMenu_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_messenger_menu

> models::GetMessengerMenu200Response get_messenger_menu(account_id)
Get Facebook persistent menu

Get the persistent menu configuration for a Facebook Messenger account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetMessengerMenu200Response**](getMessengerMenu_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_telegram_commands

> models::GetTelegramCommands200Response get_telegram_commands(account_id)
Get Telegram bot commands

Get the bot commands configuration for a Telegram account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetTelegramCommands200Response**](getTelegramCommands_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_instagram_ice_breakers

> set_instagram_ice_breakers(account_id, set_instagram_ice_breakers_request)
Set Instagram ice breakers

Set ice breakers for an Instagram account. Max 4 ice breakers, question max 80 chars.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_instagram_ice_breakers_request** | [**SetInstagramIceBreakersRequest**](SetInstagramIceBreakersRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_messenger_menu

> set_messenger_menu(account_id, set_messenger_menu_request)
Set Facebook persistent menu

Set the persistent menu for a Facebook Messenger account. Max 3 top-level items, max 5 nested items.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_messenger_menu_request** | [**SetMessengerMenuRequest**](SetMessengerMenuRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_telegram_commands

> set_telegram_commands(account_id, set_telegram_commands_request)
Set Telegram bot commands

Set bot commands for a Telegram account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_telegram_commands_request** | [**SetTelegramCommandsRequest**](SetTelegramCommandsRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

