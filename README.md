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

// Configure API key authorization: applicationId
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKey('ApplicationId', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\UserService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApplicationId', 'Bearer');// Configure HTTP basic authorization: basicAuth
$config = VentureLeap\UserService\Configuration::getDefaultConfiguration()
    ->setUsername('YOUR_USERNAME')
    ->setPassword('YOUR_PASSWORD');

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

## Documentation for API Endpoints

All URIs are relative to */*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthApi* | [**postCredentialsItem**](docs/Api/AuthApi.md#postcredentialsitem) | **POST** /login | Gets Logged in User.
*ConfigurationEntryApi* | [**deleteConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#deleteconfigurationentryitem) | **DELETE** /configuration_entries/{id} | Removes the ConfigurationEntry resource.
*ConfigurationEntryApi* | [**getConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#getconfigurationentrycollection) | **GET** /configuration_entries | Retrieves the collection of ConfigurationEntry resources.
*ConfigurationEntryApi* | [**getConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#getconfigurationentryitem) | **GET** /configuration_entries/{id} | Retrieves a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**postConfigurationEntryCollection**](docs/Api/ConfigurationEntryApi.md#postconfigurationentrycollection) | **POST** /configuration_entries | Creates a ConfigurationEntry resource.
*ConfigurationEntryApi* | [**putConfigurationEntryItem**](docs/Api/ConfigurationEntryApi.md#putconfigurationentryitem) | **PUT** /configuration_entries/{id} | Replaces the ConfigurationEntry resource.
*UserApi* | [**getUserCollection**](docs/Api/UserApi.md#getusercollection) | **GET** /users | Retrieves the collection of User resources.
*UserApi* | [**getUserItem**](docs/Api/UserApi.md#getuseritem) | **GET** /users/{id} | Retrieves a User resource.
*UserApi* | [**loginByTokenUserItem**](docs/Api/UserApi.md#loginbytokenuseritem) | **GET** /users/login-by-token/{token} | Retrieves a User resource.
*UserApi* | [**postUserCollection**](docs/Api/UserApi.md#postusercollection) | **POST** /users | Creates a User resource.
*UserApi* | [**putUserItem**](docs/Api/UserApi.md#putuseritem) | **PUT** /users/{id} | Replaces the User resource.

## Documentation For Models

 - [Auth](docs/Model/Auth.md)
 - [ConfigurationEntryJsonldConfigurationRead](docs/Model/ConfigurationEntryJsonldConfigurationRead.md)
 - [ConfigurationEntryJsonldConfigurationWrite](docs/Model/ConfigurationEntryJsonldConfigurationWrite.md)
 - [Credentials](docs/Model/Credentials.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse200Hydrasearch](docs/Model/InlineResponse200Hydrasearch.md)
 - [InlineResponse200HydrasearchHydramapping](docs/Model/InlineResponse200HydrasearchHydramapping.md)
 - [InlineResponse200Hydraview](docs/Model/InlineResponse200Hydraview.md)
 - [UserJsonldUserRead](docs/Model/UserJsonldUserRead.md)
 - [UserJsonldUserWrite](docs/Model/UserJsonldUserWrite.md)

## Documentation For Authorization


## applicationId

- **Type**: API key
- **API key parameter name**: ApplicationId
- **Location**: HTTP header

## basicAuth

- **Type**: HTTP basic authentication


## Author



