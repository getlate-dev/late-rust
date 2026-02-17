# \ConnectApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**complete_telegram_connect**](ConnectApi.md#complete_telegram_connect) | **PATCH** /v1/connect/telegram | Check Telegram status
[**connect_bluesky_credentials**](ConnectApi.md#connect_bluesky_credentials) | **POST** /v1/connect/bluesky/credentials | Connect Bluesky account
[**get_connect_url**](ConnectApi.md#get_connect_url) | **GET** /v1/connect/{platform} | Get OAuth connect URL
[**get_facebook_pages**](ConnectApi.md#get_facebook_pages) | **GET** /v1/accounts/{accountId}/facebook-page | List Facebook pages
[**get_gmb_locations**](ConnectApi.md#get_gmb_locations) | **GET** /v1/accounts/{accountId}/gmb-locations | List GBP locations
[**get_linked_in_organizations**](ConnectApi.md#get_linked_in_organizations) | **GET** /v1/accounts/{accountId}/linkedin-organizations | List LinkedIn orgs
[**get_pending_o_auth_data**](ConnectApi.md#get_pending_o_auth_data) | **GET** /v1/connect/pending-data | Get pending OAuth data
[**get_pinterest_boards**](ConnectApi.md#get_pinterest_boards) | **GET** /v1/accounts/{accountId}/pinterest-boards | List Pinterest boards
[**get_reddit_flairs**](ConnectApi.md#get_reddit_flairs) | **GET** /v1/accounts/{accountId}/reddit-flairs | List subreddit flairs
[**get_reddit_subreddits**](ConnectApi.md#get_reddit_subreddits) | **GET** /v1/accounts/{accountId}/reddit-subreddits | List Reddit subreddits
[**get_telegram_connect_status**](ConnectApi.md#get_telegram_connect_status) | **GET** /v1/connect/telegram | Generate Telegram code
[**handle_o_auth_callback**](ConnectApi.md#handle_o_auth_callback) | **POST** /v1/connect/{platform} | Complete OAuth callback
[**initiate_telegram_connect**](ConnectApi.md#initiate_telegram_connect) | **POST** /v1/connect/telegram | Connect Telegram directly
[**list_facebook_pages**](ConnectApi.md#list_facebook_pages) | **GET** /v1/connect/facebook/select-page | List Facebook pages
[**list_google_business_locations**](ConnectApi.md#list_google_business_locations) | **GET** /v1/connect/googlebusiness/locations | List GBP locations
[**list_linked_in_organizations**](ConnectApi.md#list_linked_in_organizations) | **GET** /v1/connect/linkedin/organizations | List LinkedIn orgs
[**list_pinterest_boards_for_selection**](ConnectApi.md#list_pinterest_boards_for_selection) | **GET** /v1/connect/pinterest/select-board | List Pinterest boards
[**list_snapchat_profiles**](ConnectApi.md#list_snapchat_profiles) | **GET** /v1/connect/snapchat/select-profile | List Snapchat profiles
[**select_facebook_page**](ConnectApi.md#select_facebook_page) | **POST** /v1/connect/facebook/select-page | Select Facebook page
[**select_google_business_location**](ConnectApi.md#select_google_business_location) | **POST** /v1/connect/googlebusiness/select-location | Select GBP location
[**select_linked_in_organization**](ConnectApi.md#select_linked_in_organization) | **POST** /v1/connect/linkedin/select-organization | Select LinkedIn org
[**select_pinterest_board**](ConnectApi.md#select_pinterest_board) | **POST** /v1/connect/pinterest/select-board | Select Pinterest board
[**select_snapchat_profile**](ConnectApi.md#select_snapchat_profile) | **POST** /v1/connect/snapchat/select-profile | Select Snapchat profile
[**update_facebook_page**](ConnectApi.md#update_facebook_page) | **PUT** /v1/accounts/{accountId}/facebook-page | Update Facebook page
[**update_gmb_location**](ConnectApi.md#update_gmb_location) | **PUT** /v1/accounts/{accountId}/gmb-locations | Update GBP location
[**update_linked_in_organization**](ConnectApi.md#update_linked_in_organization) | **PUT** /v1/accounts/{accountId}/linkedin-organization | Switch LinkedIn account type
[**update_pinterest_boards**](ConnectApi.md#update_pinterest_boards) | **PUT** /v1/accounts/{accountId}/pinterest-boards | Set default Pinterest board
[**update_reddit_subreddits**](ConnectApi.md#update_reddit_subreddits) | **PUT** /v1/accounts/{accountId}/reddit-subreddits | Set default subreddit



## complete_telegram_connect

> models::CompleteTelegramConnect200Response complete_telegram_connect(code)
Check Telegram status

Poll this endpoint to check if a Telegram access code has been used to connect a channel/group. Recommended polling interval: 3 seconds. Status values: pending (waiting for user), connected (channel/group linked), expired (generate a new code). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**code** | **String** | The access code to check status for | [required] |

### Return type

[**models::CompleteTelegramConnect200Response**](completeTelegramConnect_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## connect_bluesky_credentials

> models::ConnectBlueskyCredentials200Response connect_bluesky_credentials(connect_bluesky_credentials_request)
Connect Bluesky account

Connect a Bluesky account using identifier (handle or email) and an app password. To get your userId for the state parameter, call GET /v1/users which includes a currentUserId field. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**connect_bluesky_credentials_request** | [**ConnectBlueskyCredentialsRequest**](ConnectBlueskyCredentialsRequest.md) |  | [required] |

### Return type

[**models::ConnectBlueskyCredentials200Response**](connectBlueskyCredentials_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_connect_url

> models::GetConnectUrl200Response get_connect_url(platform, profile_id, redirect_url)
Get OAuth connect URL

Initiate an OAuth connection flow. Returns an authUrl to redirect the user to. Standard flow: Late hosts the selection UI, then redirects to your redirect_url. Headless mode (headless=true): user is redirected to your redirect_url with OAuth data for custom UI. Use the platform-specific selection endpoints to complete. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | **String** | Social media platform to connect | [required] |
**profile_id** | **String** | Your Late profile ID (get from /v1/profiles) | [required] |
**redirect_url** | Option<**String**> | Your custom redirect URL after connection completes. Standard mode appends ?connected={platform}&profileId=X&username=Y. Headless mode appends OAuth data params. |  |

### Return type

[**models::GetConnectUrl200Response**](getConnectUrl_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_facebook_pages

> models::GetFacebookPages200Response get_facebook_pages(account_id)
List Facebook pages

Returns all Facebook pages the connected account has access to, including the currently selected page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetFacebookPages200Response**](getFacebookPages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_gmb_locations

> models::GetGmbLocations200Response get_gmb_locations(account_id)
List GBP locations

Returns all Google Business Profile locations the connected account has access to, including the currently selected location.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetGmbLocations200Response**](getGmbLocations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_organizations

> models::GetLinkedInOrganizations200Response get_linked_in_organizations(account_id)
List LinkedIn orgs

Returns LinkedIn organizations (company pages) the connected account has admin access to.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetLinkedInOrganizations200Response**](getLinkedInOrganizations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_pending_o_auth_data

> models::GetPendingOAuthData200Response get_pending_o_auth_data(token)
Get pending OAuth data

Fetch pending OAuth data for headless mode using the pendingDataToken from the redirect URL. One-time use, expires after 10 minutes. No authentication required.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | The pending data token from the OAuth redirect URL (pendingDataToken parameter) | [required] |

### Return type

[**models::GetPendingOAuthData200Response**](getPendingOAuthData_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_pinterest_boards

> models::GetPinterestBoards200Response get_pinterest_boards(account_id)
List Pinterest boards

Returns the boards available for a connected Pinterest account. Use this to get a board ID when creating a Pinterest post.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetPinterestBoards200Response**](getPinterestBoards_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_reddit_flairs

> models::GetRedditFlairs200Response get_reddit_flairs(account_id, subreddit)
List subreddit flairs

Returns available post flairs for a subreddit. Some subreddits require a flair when posting.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**subreddit** | **String** | Subreddit name (without \"r/\" prefix) to fetch flairs for | [required] |

### Return type

[**models::GetRedditFlairs200Response**](getRedditFlairs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_reddit_subreddits

> models::GetRedditSubreddits200Response get_reddit_subreddits(account_id)
List Reddit subreddits

Returns the subreddits the connected Reddit account can post to. Use this to get a subreddit name when creating a Reddit post.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetRedditSubreddits200Response**](getRedditSubreddits_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_telegram_connect_status

> models::GetTelegramConnectStatus200Response get_telegram_connect_status(profile_id)
Generate Telegram code

Generate an access code (valid 15 minutes) for connecting a Telegram channel or group. Add the bot as admin, then send the code + @yourchannel to the bot. Poll PATCH /v1/connect/telegram to check status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | The profile ID to connect the Telegram account to | [required] |

### Return type

[**models::GetTelegramConnectStatus200Response**](getTelegramConnectStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## handle_o_auth_callback

> handle_o_auth_callback(platform, handle_o_auth_callback_request)
Complete OAuth callback

Exchange the OAuth authorization code for tokens and connect the account to the specified profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | **String** |  | [required] |
**handle_o_auth_callback_request** | [**HandleOAuthCallbackRequest**](HandleOAuthCallbackRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## initiate_telegram_connect

> models::InitiateTelegramConnect200Response initiate_telegram_connect(initiate_telegram_connect_request)
Connect Telegram directly

Connect a Telegram channel/group directly using the chat ID. Alternative to the access code flow. The bot must already be an admin in the channel/group.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**initiate_telegram_connect_request** | [**InitiateTelegramConnectRequest**](InitiateTelegramConnectRequest.md) |  | [required] |

### Return type

[**models::InitiateTelegramConnect200Response**](initiateTelegramConnect_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_facebook_pages

> models::ListFacebookPages200Response list_facebook_pages(profile_id, temp_token)
List Facebook pages

Returns the list of Facebook Pages the user can manage after OAuth. Extract tempToken and userProfile from the OAuth redirect params and pass them here. Use the X-Connect-Token header if connecting via API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID from your connection flow | [required] |
**temp_token** | **String** | Temporary Facebook access token from the OAuth callback redirect | [required] |

### Return type

[**models::ListFacebookPages200Response**](listFacebookPages_200_response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_google_business_locations

> models::ListGoogleBusinessLocations200Response list_google_business_locations(profile_id, temp_token)
List GBP locations

For headless flows. Returns the list of GBP locations the user can manage. Use X-Connect-Token if connecting via API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID from your connection flow | [required] |
**temp_token** | **String** | Temporary Google access token from the OAuth callback redirect | [required] |

### Return type

[**models::ListGoogleBusinessLocations200Response**](listGoogleBusinessLocations_200_response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_linked_in_organizations

> models::ListLinkedInOrganizations200Response list_linked_in_organizations(temp_token, org_ids)
List LinkedIn orgs

Fetch full LinkedIn organization details (logos, vanity names, websites) for custom UI. No authentication required, just the tempToken from OAuth.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**temp_token** | **String** | The temporary LinkedIn access token from the OAuth redirect | [required] |
**org_ids** | **String** | Comma-separated list of organization IDs to fetch details for (max 100) | [required] |

### Return type

[**models::ListLinkedInOrganizations200Response**](listLinkedInOrganizations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_pinterest_boards_for_selection

> models::ListPinterestBoardsForSelection200Response list_pinterest_boards_for_selection(x_connect_token, profile_id, temp_token)
List Pinterest boards

For headless flows. Returns Pinterest boards the user can post to. Use X-Connect-Token from the redirect URL.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**x_connect_token** | **String** | Short-lived connect token from the OAuth redirect | [required] |
**profile_id** | **String** | Your Late profile ID | [required] |
**temp_token** | **String** | Temporary Pinterest access token from the OAuth callback redirect | [required] |

### Return type

[**models::ListPinterestBoardsForSelection200Response**](listPinterestBoardsForSelection_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_snapchat_profiles

> models::ListSnapchatProfiles200Response list_snapchat_profiles(x_connect_token, profile_id, temp_token)
List Snapchat profiles

For headless flows. Returns Snapchat Public Profiles the user can post to. Use X-Connect-Token from the redirect URL.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**x_connect_token** | **String** | Short-lived connect token from the OAuth redirect | [required] |
**profile_id** | **String** | Your Late profile ID | [required] |
**temp_token** | **String** | Temporary Snapchat access token from the OAuth callback redirect | [required] |

### Return type

[**models::ListSnapchatProfiles200Response**](listSnapchatProfiles_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## select_facebook_page

> models::SelectFacebookPage200Response select_facebook_page(select_facebook_page_request)
Select Facebook page

Complete the headless flow by saving the user's selected Facebook page. Pass the userProfile from the OAuth redirect and use X-Connect-Token if connecting via API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**select_facebook_page_request** | [**SelectFacebookPageRequest**](SelectFacebookPageRequest.md) |  | [required] |

### Return type

[**models::SelectFacebookPage200Response**](selectFacebookPage_200_response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## select_google_business_location

> models::SelectGoogleBusinessLocation200Response select_google_business_location(select_google_business_location_request)
Select GBP location

Complete the headless flow by saving the user's selected GBP location. Include userProfile from the OAuth redirect (contains refresh token). Use X-Connect-Token if connecting via API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**select_google_business_location_request** | [**SelectGoogleBusinessLocationRequest**](SelectGoogleBusinessLocationRequest.md) |  | [required] |

### Return type

[**models::SelectGoogleBusinessLocation200Response**](selectGoogleBusinessLocation_200_response.md)

### Authorization

[connectToken](../README.md#connectToken), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## select_linked_in_organization

> models::SelectLinkedInOrganization200Response select_linked_in_organization(select_linked_in_organization_request)
Select LinkedIn org

Complete the LinkedIn connection flow. Set accountType to \"personal\" or \"organization\" to connect as a company page. Use X-Connect-Token if connecting via API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**select_linked_in_organization_request** | [**SelectLinkedInOrganizationRequest**](SelectLinkedInOrganizationRequest.md) |  | [required] |

### Return type

[**models::SelectLinkedInOrganization200Response**](selectLinkedInOrganization_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## select_pinterest_board

> models::SelectPinterestBoard200Response select_pinterest_board(select_pinterest_board_request)
Select Pinterest board

Complete the Pinterest connection flow. After OAuth, use this endpoint to save the selected board and complete the account connection. Use the X-Connect-Token header if you initiated the connection via API key. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**select_pinterest_board_request** | [**SelectPinterestBoardRequest**](SelectPinterestBoardRequest.md) |  | [required] |

### Return type

[**models::SelectPinterestBoard200Response**](selectPinterestBoard_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## select_snapchat_profile

> models::SelectSnapchatProfile200Response select_snapchat_profile(select_snapchat_profile_request, x_connect_token)
Select Snapchat profile

Complete the Snapchat connection flow by saving the selected Public Profile. Snapchat requires a Public Profile to publish content. Use X-Connect-Token if connecting via API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**select_snapchat_profile_request** | [**SelectSnapchatProfileRequest**](SelectSnapchatProfileRequest.md) |  | [required] |
**x_connect_token** | Option<**String**> | Short-lived connect token from the OAuth redirect (for API users) |  |

### Return type

[**models::SelectSnapchatProfile200Response**](selectSnapchatProfile_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_facebook_page

> models::UpdateFacebookPage200Response update_facebook_page(account_id, update_facebook_page_request)
Update Facebook page

Switch which Facebook Page is active for a connected account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_facebook_page_request** | [**UpdateFacebookPageRequest**](UpdateFacebookPageRequest.md) |  | [required] |

### Return type

[**models::UpdateFacebookPage200Response**](updateFacebookPage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_gmb_location

> models::UpdateGmbLocation200Response update_gmb_location(account_id, update_gmb_location_request)
Update GBP location

Switch which GBP location is active for a connected account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_gmb_location_request** | [**UpdateGmbLocationRequest**](UpdateGmbLocationRequest.md) |  | [required] |

### Return type

[**models::UpdateGmbLocation200Response**](updateGmbLocation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_linked_in_organization

> models::ConnectBlueskyCredentials200Response update_linked_in_organization(account_id, update_linked_in_organization_request)
Switch LinkedIn account type

Switch a LinkedIn account between personal profile and organization (company page) posting.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_linked_in_organization_request** | [**UpdateLinkedInOrganizationRequest**](UpdateLinkedInOrganizationRequest.md) |  | [required] |

### Return type

[**models::ConnectBlueskyCredentials200Response**](connectBlueskyCredentials_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_pinterest_boards

> models::ConnectBlueskyCredentials200Response update_pinterest_boards(account_id, update_pinterest_boards_request)
Set default Pinterest board

Sets the default board used when publishing pins for this account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_pinterest_boards_request** | [**UpdatePinterestBoardsRequest**](UpdatePinterestBoardsRequest.md) |  | [required] |

### Return type

[**models::ConnectBlueskyCredentials200Response**](connectBlueskyCredentials_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_reddit_subreddits

> models::UpdateRedditSubreddits200Response update_reddit_subreddits(account_id, update_reddit_subreddits_request)
Set default subreddit

Sets the default subreddit used when publishing posts for this Reddit account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_reddit_subreddits_request** | [**UpdateRedditSubredditsRequest**](UpdateRedditSubredditsRequest.md) |  | [required] |

### Return type

[**models::UpdateRedditSubreddits200Response**](updateRedditSubreddits_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

