# VentureLeap\UserService\UserApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getUserCollection**](UserApi.md#getusercollection) | **GET** /users | Retrieves the collection of User resources.
[**getUserItem**](UserApi.md#getuseritem) | **GET** /users/{id} | Retrieves a User resource.
[**loginByTokenUserItem**](UserApi.md#loginbytokenuseritem) | **GET** /users/login-by-token/{token} | Retrieves a User resource.
[**postUserCollection**](UserApi.md#postusercollection) | **POST** /users | Creates a User resource.
[**putUserItem**](UserApi.md#putuseritem) | **PUT** /users/{id} | Replaces the User resource.

# **getUserCollection**
> \VentureLeap\UserService\Model\InlineResponse2001 getUserCollection($username, $email, $first_name, $last_name, $additional_properties, $user_type, $active, $deleted, $page)

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

try {
    $result = $apiInstance->getUserCollection($username, $email, $first_name, $last_name, $additional_properties, $user_type, $active, $deleted, $page);
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
> \VentureLeap\UserService\Model\UserJsonldUserRead loginByTokenUserItem($id)

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
    $result = $apiInstance->loginByTokenUserItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->loginByTokenUserItem: ', $e->getMessage(), PHP_EOL;
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

