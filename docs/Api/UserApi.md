# VentureLeap\UserService\UserApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getUserCollection**](UserApi.md#getusercollection) | **GET** /user/users | Retrieves the collection of User resources.
[**getUserItem**](UserApi.md#getuseritem) | **GET** /user/users/{id} | Retrieves a User resource.
[**loginByTokenUserItem**](UserApi.md#loginbytokenuseritem) | **GET** /user/users/login-by-token/{token} | Retrieves a User resource.
[**postCredentialsItem**](UserApi.md#postcredentialsitem) | **POST** /user/users/login | Gets Logged in User.
[**postUserCollection**](UserApi.md#postusercollection) | **POST** /user/users | Creates a User resource.
[**putUserItem**](UserApi.md#putuseritem) | **PUT** /user/users/{id} | Replaces the User resource.

# **getUserCollection**
> \VentureLeap\UserService\Model\InlineResponse2001 getUserCollection($username, $email, $first_name, $last_name, $additional_properties, $user_type, $active, $deleted, $page, $items_per_page, $pagination)

Retrieves the collection of User resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = "username_example"; // string | 
$email = "email_example"; // string | 
$first_name = "first_name_example"; // string | 
$last_name = "last_name_example"; // string | 
$additional_properties = "additional_properties_example"; // string | 
$user_type = "user_type_example"; // string | 
$active = true; // bool | 
$deleted = true; // bool | 
$page = 1; // int | The collection page number
$items_per_page = 10; // int | The number of items per page
$pagination = true; // bool | Enable or disable pagination

try {
    $result = $apiInstance->getUserCollection($username, $email, $first_name, $last_name, $additional_properties, $user_type, $active, $deleted, $page, $items_per_page, $pagination);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUserCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**|  | [optional]
 **email** | **string**|  | [optional]
 **first_name** | **string**|  | [optional]
 **last_name** | **string**|  | [optional]
 **additional_properties** | **string**|  | [optional]
 **user_type** | **string**|  | [optional]
 **active** | **bool**|  | [optional]
 **deleted** | **bool**|  | [optional]
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

# **getUserItem**
> \VentureLeap\UserService\Model\UserJsonldUserRead getUserItem($id)

Retrieves a User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getUserItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUserItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **loginByTokenUserItem**
> \VentureLeap\UserService\Model\UserJsonldUserRead loginByTokenUserItem($token)

Retrieves a User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$token = "token_example"; // string | 

try {
    $result = $apiInstance->loginByTokenUserItem($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->loginByTokenUserItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postCredentialsItem**
> \VentureLeap\UserService\Model\User postCredentialsItem($body)

Gets Logged in User.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\UserService\Model\Credentials(); // \VentureLeap\UserService\Model\Credentials | Authenticates user based on credentials

try {
    $result = $apiInstance->postCredentialsItem($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->postCredentialsItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\UserService\Model\Credentials**](../Model/Credentials.md)| Authenticates user based on credentials | [optional]

### Return type

[**\VentureLeap\UserService\Model\User**](../Model/User.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUserCollection**
> \VentureLeap\UserService\Model\UserJsonldUserRead postUserCollection($body)

Creates a User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\UserService\Model\UserJsonldUserWrite(); // \VentureLeap\UserService\Model\UserJsonldUserWrite | The new User resource

try {
    $result = $apiInstance->postUserCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->postUserCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\UserService\Model\UserJsonldUserWrite**](../Model/UserJsonldUserWrite.md)| The new User resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putUserItem**
> \VentureLeap\UserService\Model\UserJsonldUserRead putUserItem($id, $body)

Replaces the User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\UserService\Model\UserJsonldUserWrite(); // \VentureLeap\UserService\Model\UserJsonldUserWrite | The updated User resource

try {
    $result = $apiInstance->putUserItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->putUserItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\UserService\Model\UserJsonldUserWrite**](../Model/UserJsonldUserWrite.md)| The updated User resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

