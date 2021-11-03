# VentureLeap\UserService\AccountApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiAccountsUsersGetSubresource**](AccountApi.md#apiaccountsusersgetsubresource) | **GET** /user/accounts/{id}/users | Retrieves the collection of User resources.
[**getAccountCollection**](AccountApi.md#getaccountcollection) | **GET** /user/accounts | Retrieves the collection of Account resources.
[**getAccountItem**](AccountApi.md#getaccountitem) | **GET** /user/accounts/{id} | Retrieves a Account resource.
[**postAccountCollection**](AccountApi.md#postaccountcollection) | **POST** /user/accounts | Creates a Account resource.
[**putAccountItem**](AccountApi.md#putaccountitem) | **PUT** /user/accounts/{id} | Replaces the Account resource.

# **apiAccountsUsersGetSubresource**
> \VentureLeap\UserService\Model\InlineResponse2001 apiAccountsUsersGetSubresource($id, $username, $email, $first_name, $last_name, $custom_data, $user_type, $active, $deleted, $username, $page, $items_per_page, $pagination)

Retrieves the collection of User resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$username = "username_example"; // string | 
$email = "email_example"; // string | 
$first_name = "first_name_example"; // string | 
$last_name = "last_name_example"; // string | 
$custom_data = "custom_data_example"; // string | 
$user_type = "user_type_example"; // string | 
$active = true; // bool | 
$deleted = true; // bool | 
$username = "username_example"; // string | 
$page = 1; // int | The collection page number
$items_per_page = 10; // int | The number of items per page
$pagination = true; // bool | Enable or disable pagination

try {
    $result = $apiInstance->apiAccountsUsersGetSubresource($id, $username, $email, $first_name, $last_name, $custom_data, $user_type, $active, $deleted, $username, $page, $items_per_page, $pagination);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->apiAccountsUsersGetSubresource: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **username** | **string**|  | [optional]
 **email** | **string**|  | [optional]
 **first_name** | **string**|  | [optional]
 **last_name** | **string**|  | [optional]
 **custom_data** | **string**|  | [optional]
 **user_type** | **string**|  | [optional]
 **active** | **bool**|  | [optional]
 **deleted** | **bool**|  | [optional]
 **username** | **string**|  | [optional]
 **page** | **int**| The collection page number | [optional] [default to 1]
 **items_per_page** | **int**| The number of items per page | [optional] [default to 10]
 **pagination** | **bool**| Enable or disable pagination | [optional]

### Return type

[**\VentureLeap\UserService\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAccountCollection**
> \VentureLeap\UserService\Model\InlineResponse200 getAccountCollection($account_number, $active, $deleted, $page, $items_per_page, $pagination)

Retrieves the collection of Account resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_number = "account_number_example"; // string | 
$active = true; // bool | 
$deleted = true; // bool | 
$page = 1; // int | The collection page number
$items_per_page = 10; // int | The number of items per page
$pagination = true; // bool | Enable or disable pagination

try {
    $result = $apiInstance->getAccountCollection($account_number, $active, $deleted, $page, $items_per_page, $pagination);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->getAccountCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_number** | **string**|  | [optional]
 **active** | **bool**|  | [optional]
 **deleted** | **bool**|  | [optional]
 **page** | **int**| The collection page number | [optional] [default to 1]
 **items_per_page** | **int**| The number of items per page | [optional] [default to 10]
 **pagination** | **bool**| Enable or disable pagination | [optional]

### Return type

[**\VentureLeap\UserService\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAccountItem**
> \VentureLeap\UserService\Model\AccountJsonldAccountRead getAccountItem($id)

Retrieves a Account resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getAccountItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->getAccountItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\AccountJsonldAccountRead**](../Model/AccountJsonldAccountRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postAccountCollection**
> \VentureLeap\UserService\Model\AccountJsonldAccountRead postAccountCollection($body)

Creates a Account resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\UserService\Model\AccountJsonldAccountWrite(); // \VentureLeap\UserService\Model\AccountJsonldAccountWrite | The new Account resource

try {
    $result = $apiInstance->postAccountCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->postAccountCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\UserService\Model\AccountJsonldAccountWrite**](../Model/AccountJsonldAccountWrite.md)| The new Account resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\AccountJsonldAccountRead**](../Model/AccountJsonldAccountRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putAccountItem**
> \VentureLeap\UserService\Model\AccountJsonldAccountRead putAccountItem($id, $body)

Replaces the Account resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\UserService\Model\AccountJsonldAccountWrite(); // \VentureLeap\UserService\Model\AccountJsonldAccountWrite | The updated Account resource

try {
    $result = $apiInstance->putAccountItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->putAccountItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\UserService\Model\AccountJsonldAccountWrite**](../Model/AccountJsonldAccountWrite.md)| The updated Account resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\AccountJsonldAccountRead**](../Model/AccountJsonldAccountRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

