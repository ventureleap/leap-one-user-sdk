# VentureLeap\UserService\SocialAuthenticationApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**socialLoginGetAuthUrl**](SocialAuthenticationApi.md#sociallogingetauthurl) | **GET** /user/social/{platform}/auth-url | Get Social Platform Authorization Url
[**socialLoginGetUser**](SocialAuthenticationApi.md#sociallogingetuser) | **GET** /user/social/{platform} | Perform Social Login/Registration for user

# **socialLoginGetAuthUrl**
> \VentureLeap\UserService\Model\SocialAuthUrl socialLoginGetAuthUrl($platform)

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
    $result = $apiInstance->socialLoginGetAuthUrl($platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SocialAuthenticationApi->socialLoginGetAuthUrl: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\SocialAuthUrl**](../Model/SocialAuthUrl.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **socialLoginGetUser**
> \VentureLeap\UserService\Model\UserJsonldUserRead socialLoginGetUser($platform, $state, $code)

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
$state = "state_example"; // string | 
$code = "code_example"; // string | 

try {
    $result = $apiInstance->socialLoginGetUser($platform, $state, $code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SocialAuthenticationApi->socialLoginGetUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **string**|  |
 **state** | **string**|  |
 **code** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

