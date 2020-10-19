# UserJsonldUserRead

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**context** | **string** |  | [optional] 
**id** | **string** |  | [optional] 
**type** | **string** |  | [optional] 
**uuid** | **string** |  | [optional] 
**email** | **string** |  | 
**username** | **string** |  | 
**first_name** | **string** |  | [optional] 
**last_name** | **string** |  | [optional] 
**login_token** | **string** |  | [optional] 
**deleted** | **bool** |  | [optional] 
**additional_properties** | **string** | An explicit json array would make much more sense here. Unfortunately, the SDK generator does not understand this properly, so we have to encode and decode id manually. | [optional] 
**created_at** | [**\DateTime**](\DateTime.md) |  | [optional] 
**updated_at** | [**\DateTime**](\DateTime.md) |  | [optional] 
**auth_code** | **string** |  | [optional] 
**failed_login_attempts** | **int** |  | [optional] 
**failed_login_time** | [**\DateTime**](\DateTime.md) |  | [optional] 
**user_type** | **string** |  | [optional] 
**roles** | **string[]** | First time I do that ever, but it seems necessary here. | [optional] 
**active** | **bool** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

