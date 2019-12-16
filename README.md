# Diglin Reference Data API Endpoint Bundle

Add entry point for the API of the [CustomEntityBundle](https://github.com/akeneo-labs/CustomEntityBundle) of [Akeneo Labs](https://github.com/akeneo-labs).

## Installation

You can install this bundle with composer:

`php composer.phar require diglin/custom-entity-api-endpoint-bundle:1.*`

Add **at the end** of `app/config/routing.yml`, the following content:

```yaml
diglin_api_ref_data:
    resource: "@DiglinApiRefDataBundle/Resources/config/routing.yml"
    prefix: /api
``` 

and enable the bundle in the `app/AppKernel.php` file in the `registerProjectBundles()` method:

```php
    $bundles = [
        // ...
        new \Diglin\Bundle\ApiRefDataBundle\DiglinApiRefDataBundle(),
    ]
```

## Usage

Available API endpoint:

```
api_ref_data_reference_data_list  GET  /api/rest/v1/reference-data/{referenceName}
api_ref_data_reference_data_get  GET  /api/rest/v1/reference-data/{referenceName}/{code}  
```

## License

[Do What The Fuck You Want To Public License (WTFPL)](http://www.wtfpl.net/)

## Author

* Sylvain Rayé
* http://www.diglin.com/
* [@diglin_](https://twitter.com/diglin_)
* [Follow me on github!](https://github.com/diglin)