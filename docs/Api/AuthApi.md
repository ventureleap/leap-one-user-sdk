# VentureLeap\UserService\AuthApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**postCredentialsItem**](AuthApi.md#postcredentialsitem) | **POST** /users/login | Gets Logged in User.

# **postCredentialsItem**
> \VentureLeap\UserService\Model\Auth postCredentialsItem($body)

Gets Logged in User.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AuthApi(
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
    echo 'Exception when calling AuthApi->postCredentialsItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\UserService\Model\Credentials**](../Model/Credentials.md)| Authenticates user based on credentials | [optional]

### Return type

[**\VentureLeap\UserService\Model\Auth**](../Model/Auth.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

