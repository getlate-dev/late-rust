# TwitterPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reply_settings** | Option<**ReplySettings**> | Controls who can reply to the tweet. \"following\" allows only people you follow, \"mentionedUsers\" allows only mentioned users, \"subscribers\" allows only subscribers. Omit for default (everyone can reply). For threads, applies to the first tweet only. (enum: following, mentionedUsers, subscribers) | [optional]
**thread_items** | Option<[**Vec<models::TwitterPlatformDataThreadItemsInner>**](TwitterPlatformDataThreadItemsInner.md)> | Sequence of tweets in a thread. First item is the root tweet. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


