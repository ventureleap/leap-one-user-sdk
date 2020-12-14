# VentureLeap\UserService\SocialAuthenticationApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**socialLogin**](SocialAuthenticationApi.md#sociallogin) | **GET** /user/social/{platform}/auth-url | Get Social Platform Authorization Url
[**socialLogin_0**](SocialAuthenticationApi.md#sociallogin_0) | **GET** /user/social/{platform} | Perform Social Login/Registration for user

# **socialLogin**
> \VentureLeap\UserService\Model\InlineResponse2003 socialLogin($platform)

Get Social Platform Authorization Url

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\SocialAuthenticationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$platform = "platform_example"; // string | 

try {
    $result = $apiInstance->socialLogin($platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SocialAuthenticationApi->socialLogin: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\InlineResponse2003**](../Model/InlineResponse2003.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **socialLogin_0**
> \VentureLeap\UserService\Model\User socialLogin_0($platform)

Perform Social Login/Registration for user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\SocialAuthenticationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$platform = "platform_example"; // string | 

try {
    $result = $apiInstance->socialLogin_0($platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SocialAuthenticationApi->socialLogin_0: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\User**](../Model/User.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

