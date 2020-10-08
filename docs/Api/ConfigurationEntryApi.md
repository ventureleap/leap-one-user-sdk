# VentureLeap\UserService\ConfigurationEntryApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteConfigurationEntryItem**](ConfigurationEntryApi.md#deleteconfigurationentryitem) | **DELETE** /user/configuration_entries/{id} | Removes the ConfigurationEntry resource.
[**getConfigurationEntryCollection**](ConfigurationEntryApi.md#getconfigurationentrycollection) | **GET** /user/configuration_entries | Retrieves the collection of ConfigurationEntry resources.
[**getConfigurationEntryItem**](ConfigurationEntryApi.md#getconfigurationentryitem) | **GET** /user/configuration_entries/{id} | Retrieves a ConfigurationEntry resource.
[**postConfigurationEntryCollection**](ConfigurationEntryApi.md#postconfigurationentrycollection) | **POST** /user/configuration_entries | Creates a ConfigurationEntry resource.
[**putConfigurationEntryItem**](ConfigurationEntryApi.md#putconfigurationentryitem) | **PUT** /user/configuration_entries/{id} | Replaces the ConfigurationEntry resource.

# **deleteConfigurationEntryItem**
> deleteConfigurationEntryItem($id)

Removes the ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\UserService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteConfigurationEntryItem($id);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->deleteConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConfigurationEntryCollection**
> \VentureLeap\UserService\Model\InlineResponse200 getConfigurationEntryCollection($key, $value, $application_id, $page)

Retrieves the collection of ConfigurationEntry resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\UserService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = "key_example"; // string | 
$value = "value_example"; // string | 
$application_id = "application_id_example"; // string | 
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->getConfigurationEntryCollection($key, $value, $application_id, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**|  | [optional]
 **value** | **string**|  | [optional]
 **application_id** | **string**|  | [optional]
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**\VentureLeap\UserService\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConfigurationEntryItem**
> \VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationRead getConfigurationEntryItem($id)

Retrieves a ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\UserService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getConfigurationEntryItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postConfigurationEntryCollection**
> \VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationRead postConfigurationEntryCollection($body)

Creates a ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\UserService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationWrite | The new ConfigurationEntry resource

try {
    $result = $apiInstance->postConfigurationEntryCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->postConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The new ConfigurationEntry resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putConfigurationEntryItem**
> \VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationRead putConfigurationEntryItem($id, $body)

Replaces the ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: applicationId
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new VentureLeap\UserService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationWrite | The updated ConfigurationEntry resource

try {
    $result = $apiInstance->putConfigurationEntryItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->putConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The updated ConfigurationEntry resource | [optional]

### Return type

[**\VentureLeap\UserService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

[applicationId](../../README.md#applicationId), [basicAuth](../../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

