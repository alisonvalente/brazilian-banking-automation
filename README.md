[![MIT License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/gpupo/common-sdk/blob/master/LICENSE)
[![Build Status](https://secure.travis-ci.org/gpupo/brazilian-banking-automation.png?branch=master)](http://travis-ci.org/gpupo/brazilian-banking-automation)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/?branch=master)

#brazilian-banking-automation

## Install

    composer require gpupo/brazilian-banking-automation


## Usage

$headerAttributes = [
    'tipo_de_registro' => '0',
    'codigo_de_retorno' => '2',
    //...all required fields
];

$trailerAttributes = [
    'tipo_de_registro' => '9',
    'codigo_de_retorno' => '2',
    //...all required fields
];

$itemAttributes = [
    'tipo_de_registro' => '001',
    'codigo_de_inscricao' => '1',
    //...all required fields
];


### Modo 1 - instantiating objects

  $headerObject = new Header($headerAttributes);
  $trailerObject = new Trailer($trailerAttributes);
  $itemObject = new Item($itemAttributes);

  $file = new File($headerObject, $trailerObject);
  $file->addItem($itemObject);

  $file->getContent();

### Modo 2 - using factory

  $factory = new Cnab400\Factory();

  $item = $factory->factoryReturnItem($itemAttributes);
  $file = $factory->factoryfile($headerAttributes, $trailerAttributes);
  $file->addItem(item);

  $file->getContent();










## Console

     ./bin/brazilian-banking-automation

## Contributors

* [@gpupo](https://github.com/gpupo)

## License

*MIT*, see LICENSE.

## Links

* [Composer Package](https://packagist.org/packages/gpupo/brazilian-banking-automation/) on packagist.org
