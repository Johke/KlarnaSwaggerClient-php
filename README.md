# SwaggerClient-php
The checkout API is used to create a checkout with Klarna and update the checkout order during the purchase.  As soon as the purchase is completed the order should be read and handled using the [`Order Management API`](/order-management/api/).

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
      "url": "http://github.com/Johke/KlarnaSwaggerClient-php.git"
    }
  ],
  "require": {
    "Johke/KlarnaSwaggerClient-php": "*@dev"
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

$apiInstance = new Swagger\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\Order(); // \Swagger\Client\Model\Order | 

try {
    $result = $apiInstance->createOrderMerchant($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->createOrderMerchant: ', $e->getMessage(), PHP_EOL;
}

$apiInstance = new Swagger\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = "order_id_example"; // string | 

try {
    $result = $apiInstance->readOrderMerchant($order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->readOrderMerchant: ', $e->getMessage(), PHP_EOL;
}

$apiInstance = new Swagger\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = "order_id_example"; // string | 
$body = new \Swagger\Client\Model\Order(); // \Swagger\Client\Model\Order | 

try {
    $result = $apiInstance->updateOrderMerchant($order_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->updateOrderMerchant: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.klarna.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OrderApi* | [**createOrderMerchant**](docs/Api/OrderApi.md#createordermerchant) | **POST** /checkout/v3/orders | Create a new order
*OrderApi* | [**readOrderMerchant**](docs/Api/OrderApi.md#readordermerchant) | **GET** /checkout/v3/orders/{order_id} | Retrieve an order
*OrderApi* | [**updateOrderMerchant**](docs/Api/OrderApi.md#updateordermerchant) | **POST** /checkout/v3/orders/{order_id} | Update an order

## Documentation For Models

 - [Address](docs/Model/Address.md)
 - [Attachment](docs/Model/Attachment.md)
 - [AttachmentDisplay](docs/Model/AttachmentDisplay.md)
 - [AttachmentDisplayBody](docs/Model/AttachmentDisplayBody.md)
 - [AttachmentDisplayBodyAccountLastModified](docs/Model/AttachmentDisplayBodyAccountLastModified.md)
 - [AttachmentDisplayBodyAddress](docs/Model/AttachmentDisplayBodyAddress.md)
 - [AttachmentDisplayBodyAirReservationDetails](docs/Model/AttachmentDisplayBodyAirReservationDetails.md)
 - [AttachmentDisplayBodyArenaLocation](docs/Model/AttachmentDisplayBodyArenaLocation.md)
 - [AttachmentDisplayBodyBusReservationDetails](docs/Model/AttachmentDisplayBodyBusReservationDetails.md)
 - [AttachmentDisplayBodyCarRentalItinerary](docs/Model/AttachmentDisplayBodyCarRentalItinerary.md)
 - [AttachmentDisplayBodyCarRentalReservationDetails](docs/Model/AttachmentDisplayBodyCarRentalReservationDetails.md)
 - [AttachmentDisplayBodyCustomerAccountInfo](docs/Model/AttachmentDisplayBodyCustomerAccountInfo.md)
 - [AttachmentDisplayBodyEvent](docs/Model/AttachmentDisplayBodyEvent.md)
 - [AttachmentDisplayBodyHotelItinerary](docs/Model/AttachmentDisplayBodyHotelItinerary.md)
 - [AttachmentDisplayBodyHotelReservationDetails](docs/Model/AttachmentDisplayBodyHotelReservationDetails.md)
 - [AttachmentDisplayBodyInsurance](docs/Model/AttachmentDisplayBodyInsurance.md)
 - [AttachmentDisplayBodyItinerary](docs/Model/AttachmentDisplayBodyItinerary.md)
 - [AttachmentDisplayBodyItinerary1](docs/Model/AttachmentDisplayBodyItinerary1.md)
 - [AttachmentDisplayBodyMarketplaceSellerInfo](docs/Model/AttachmentDisplayBodyMarketplaceSellerInfo.md)
 - [AttachmentDisplayBodyMarketplaceWinnerInfo](docs/Model/AttachmentDisplayBodyMarketplaceWinnerInfo.md)
 - [AttachmentDisplayBodyOtherDeliveryAddress](docs/Model/AttachmentDisplayBodyOtherDeliveryAddress.md)
 - [AttachmentDisplayBodyPassengers](docs/Model/AttachmentDisplayBodyPassengers.md)
 - [AttachmentDisplayBodyPaymentHistoryFull](docs/Model/AttachmentDisplayBodyPaymentHistoryFull.md)
 - [AttachmentDisplayBodyPaymentHistorySimple](docs/Model/AttachmentDisplayBodyPaymentHistorySimple.md)
 - [AttachmentDisplayBodySubscription](docs/Model/AttachmentDisplayBodySubscription.md)
 - [AttachmentDisplayBodyUniqueAccountIdentifierSeller](docs/Model/AttachmentDisplayBodyUniqueAccountIdentifierSeller.md)
 - [AttachmentDisplayBodyVoucher](docs/Model/AttachmentDisplayBodyVoucher.md)
 - [Checkbox](docs/Model/Checkbox.md)
 - [CheckboxV2](docs/Model/CheckboxV2.md)
 - [Customer](docs/Model/Customer.md)
 - [DeliveryDetailsV1](docs/Model/DeliveryDetailsV1.md)
 - [Dimensions](docs/Model/Dimensions.md)
 - [Gui](docs/Model/Gui.md)
 - [MerchantRequested](docs/Model/MerchantRequested.md)
 - [MerchantRequestedCheckbox](docs/Model/MerchantRequestedCheckbox.md)
 - [MerchantUrls](docs/Model/MerchantUrls.md)
 - [Options](docs/Model/Options.md)
 - [Order](docs/Model/Order.md)
 - [OrderLine](docs/Model/OrderLine.md)
 - [PaymentProvider](docs/Model/PaymentProvider.md)
 - [PickupLocationV1](docs/Model/PickupLocationV1.md)
 - [ProductIdentifiers](docs/Model/ProductIdentifiers.md)
 - [ProductV1](docs/Model/ProductV1.md)
 - [SelectedAddon](docs/Model/SelectedAddon.md)
 - [ShippingAttributes](docs/Model/ShippingAttributes.md)
 - [ShippingOption](docs/Model/ShippingOption.md)
 - [TimeslotV1](docs/Model/TimeslotV1.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author



# KlarnaSwaggerClient-php
