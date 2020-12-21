# VentureLeap\UserService\AddressApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAddressCollection**](AddressApi.md#getaddresscollection) | **GET** /user/addresses | Retrieves the collection of Address resources.
[**getAddressItem**](AddressApi.md#getaddressitem) | **GET** /user/addresses/{id} | Retrieves a Address resource.
[**postAddressCollection**](AddressApi.md#postaddresscollection) | **POST** /user/addresses | Creates a Address resource.
[**putAddressItem**](AddressApi.md#putaddressitem) | **PUT** /user/addresses/{id} | Replaces the Address resource.

# **getAddressCollection**
> \VentureLeap\UserService\Model\InlineResponse2001 getAddressCollection($page, $items_per_page, $pagination)

Retrieves the collection of Address resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number
$items_per_page = 10; // int | The number of items per page
$pagination = true; // bool | Enable or disable pagination

try {
    $result = $apiInstance->getAddressCollection($page, $items_per_page, $pagination);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->getAddressCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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

# **getAddressItem**
> \VentureLeap\UserService\Model\AddressJsonldAddressRead getAddressItem($id)

Retrieves a Address resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getAddressItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->getAddressItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\AddressJsonldAddressRead**](../Model/AddressJsonldAddressRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postAddressCollection**
> \VentureLeap\UserService\Model\AddressJsonldAddressRead postAddressCollection($body)

Creates a Address resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\UserService\Model\AddressJsonldAddressWrite(); // \VentureLeap\UserService\Model\AddressJsonldAddressWrite | The new Address resource

try {
    $result = $apiInstance->postAddressCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->postAddressCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\UserService\Model\AddressJsonldAddressWrite**](../Model/AddressJsonldAddressWrite.md)| The new Address resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\AddressJsonldAddressRead**](../Model/AddressJsonldAddressRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putAddressItem**
> \VentureLeap\UserService\Model\AddressJsonldAddressRead putAddressItem($id, $body)

Replaces the Address resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\UserService\Api\AddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\UserService\Model\AddressJsonldAddressWrite(); // \VentureLeap\UserService\Model\AddressJsonldAddressWrite | The updated Address resource

try {
    $result = $apiInstance->putAddressItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->putAddressItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\UserService\Model\AddressJsonldAddressWrite**](../Model/AddressJsonldAddressWrite.md)| The updated Address resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\AddressJsonldAddressRead**](../Model/AddressJsonldAddressRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

