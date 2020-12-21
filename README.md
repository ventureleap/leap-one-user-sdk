# SwaggerClient-php
No description provided (generated by Swagger Codegen https://github.com/swagger-api/swagger-codegen)

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/ventureleap/leap-one-user-sdk.git"
    }
  ],
  "require": {
    "ventureleap/leap-one-user-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to */*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountApi* | [**getAccountCollection**](docs/Api/AccountApi.md#getaccountcollection) | **GET** /user/accounts | Retrieves the collection of Account resources.
*AccountApi* | [**getAccountItem**](docs/Api/AccountApi.md#getaccountitem) | **GET** /user/accounts/{id} | Retrieves a Account resource.
*AccountApi* | [**postAccountCollection**](docs/Api/AccountApi.md#postaccountcollection) | **POST** /user/accounts | Creates a Account resource.
*AccountApi* | [**putAccountItem**](docs/Api/AccountApi.md#putaccountitem) | **PUT** /user/accounts/{id} | Replaces the Account resource.
*AddressApi* | [**getAddressCollection**](docs/Api/AddressApi.md#getaddresscollection) | **GET** /user/addresses | Retrieves the collection of Address resources.
*AddressApi* | [**getAddressItem**](docs/Api/AddressApi.md#getaddressitem) | **GET** /user/addresses/{id} | Retrieves a Address resource.
*AddressApi* | [**postAddressCollection**](docs/Api/AddressApi.md#postaddresscollection) | **POST** /user/addresses | Creates a Address resource.
*AddressApi* | [**putAddressItem**](docs/Api/AddressApi.md#putaddressitem) | **PUT** /user/addresses/{id} | Replaces the Address resource.
*ConfigurationEntryApi* | [**deleteConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#deleteconfigurationentryitem) | **DELETE** /user/configuration_entries/{id} | Removes the ConfigurationEntry resource.
*ConfigurationEntryApi* | [**getConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#getconfigurationentrycollection) | **GET** /user/configuration_entries | Retrieves the collection of ConfigurationEntry resources.
*ConfigurationEntryApi* | [**getConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#getconfigurationentryitem) | **GET** /user/configuration_entries/{id} | Retrieves a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**postConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#postconfigurationentrycollection) | **POST** /user/configuration_entries | Creates a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**putConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#putconfigurationentryitem) | **PUT** /user/configuration_entries/{id} | Replaces the ConfigurationEntry resource.
*SocialAuthenticationApi* | [**socialLoginGetAuthUrl**](docs/Api/SocialAuthenticationApi.md#sociallogingetauthurl) | **GET** /user/social/{platform}/auth-url | Get Social Platform Authorization Url
*SocialAuthenticationApi* | [**socialLoginGetUser**](docs/Api/SocialAuthenticationApi.md#sociallogingetuser) | **GET** /user/social/{platform} | Perform Social Login/Registration for user
*UserApi* | [**getToken**](docs/Api/UserApi.md#gettoken) | **POST** /user/get-token | Gets JWT token for a user
*UserApi* | [**getUserCollection**](docs/Api/UserApi.md#getusercollection) | **GET** /user/users | Retrieves the collection of User resources.
*UserApi* | [**getUserItem**](docs/Api/UserApi.md#getuseritem) | **GET** /user/users/{id} | Retrieves a User resource.
*UserApi* | [**loginByTokenUserItem**](docs/Api/UserApi.md#loginbytokenuseritem) | **GET** /user/users/login-by-token/{token} | Retrieves a User resource.
*UserApi* | [**postCredentialsItem**](docs/Api/UserApi.md#postcredentialsitem) | **POST** /user/users/login | Gets Logged in User.
*UserApi* | [**postUserCollection**](docs/Api/UserApi.md#postusercollection) | **POST** /user/users | Creates a User resource.
*UserApi* | [**putUserItem**](docs/Api/UserApi.md#putuseritem) | **PUT** /user/users/{id} | Replaces the User resource.
*UserApi* | [**resetUserPasswordUserItem**](docs/Api/UserApi.md#resetuserpassworduseritem) | **PATCH** /user/users/{id}/reset-password | Updates the User resource.
*UserApi* | [**sendInvitationEmailUserItem**](docs/Api/UserApi.md#sendinvitationemailuseritem) | **GET** /user/users/{id}/invitation-email | Retrieves a User resource.

## Documentation For Models

 - [Account](docs/Model/Account.md)
 - [AccountJsonldAccountRead](docs/Model/AccountJsonldAccountRead.md)
 - [AccountJsonldAccountWrite](docs/Model/AccountJsonldAccountWrite.md)
 - [AddressJsonldAddressRead](docs/Model/AddressJsonldAddressRead.md)
 - [AddressJsonldAddressWrite](docs/Model/AddressJsonldAddressWrite.md)
 - [ConfigurationEntryJsonldConfigurationRead](docs/Model/ConfigurationEntryJsonldConfigurationRead.md)
 - [ConfigurationEntryJsonldConfigurationWrite](docs/Model/ConfigurationEntryJsonldConfigurationWrite.md)
 - [Credentials](docs/Model/Credentials.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse2002](docs/Model/InlineResponse2002.md)
 - [InlineResponse2003](docs/Model/InlineResponse2003.md)
 - [InlineResponse200Hydrasearch](docs/Model/InlineResponse200Hydrasearch.md)
 - [InlineResponse200HydrasearchHydramapping](docs/Model/InlineResponse200HydrasearchHydramapping.md)
 - [InlineResponse200Hydraview](docs/Model/InlineResponse200Hydraview.md)
 - [SocialAuthUrl](docs/Model/SocialAuthUrl.md)
 - [User](docs/Model/User.md)
 - [UserJsonldUserRead](docs/Model/UserJsonldUserRead.md)
 - [UserJsonldUserWrite](docs/Model/UserJsonldUserWrite.md)
 - [UserPasswordReset](docs/Model/UserPasswordReset.md)

## Documentation For Authorization


## apiKey

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author



