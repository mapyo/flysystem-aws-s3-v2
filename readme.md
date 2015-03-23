PHP 5.3 support.

# Flysystem Adapter for AWS S3 SDK v2

[![Build Status](https://travis-ci.org/mapyo/flysystem-aws-s3-v2.svg?branch=master)](https://travis-ci.org/mapyo/flysystem-aws-s3-v2)


## Installation

```bash
composer require league/flysystem-aws-s3-v2
```

## Usage

```php
use Aws\S3\S3Client;
use League\Flysystem\AwsS3v2\AwsS3Adapter;
use League\Flysystem\Filesystem;

$client = S3Client::factory(array(
    'key'    => '[your key]',
    'secret' => '[your secret]',
    'region' => '[aws-region]'
));

$adapter = new AwsS3Adapter($client, 'bucket-name', 'optional-prefix');

$filesystem = new Filesystem($adapter);
```
