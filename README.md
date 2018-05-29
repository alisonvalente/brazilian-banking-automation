[![MIT License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/gpupo/common-sdk/blob/master/LICENSE)
[![Build Status](https://secure.travis-ci.org/gpupo/brazilian-banking-automation.png?branch=master)](http://travis-ci.org/gpupo/brazilian-banking-automation)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/gpupo/brazilian-banking-automation/?branch=master)

#brazilian-banking-automation

## Install

    composer require gpupo/brazilian-banking-automation


## Usage


### Modo 1

  $header = new Header($toAttr($header));
  $trailer = new Trailer($toAttr($trailer));
  $item = new Item($toAttr($item));

  $itemCollection = new Collection();
  $itemCollection->add($item);

### Modo 2


  $cnab400 = new Factory\Cnab400();

  $returnFile = $cnab400->factoryReturnFile();

  $returnFile->getHeader()->set('foo', 'bar');
  $returnFile->getTrailer()->set('foo', 'bar');


  $returnFile->getItems()->add($cnab400->factoryReturnItem());






## Console

     ./bin/brazilian-banking-automation

## Contributors

* [@gpupo](https://github.com/gpupo)

## License

*MIT*, see LICENSE.

## Links

* [Composer Package](https://packagist.org/packages/gpupo/brazilian-banking-automation/) on packagist.org
