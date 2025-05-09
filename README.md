# Thesis Clock

[![PHP Version Requirement](https://img.shields.io/packagist/dependency-v/thesis/clock/php)](https://packagist.org/packages/thesis/clock)
[![GitHub Release](https://img.shields.io/github/v/release/thesis-php/clock)](https://github.com/thesis-php/clock/releases)
[![Code Coverage](https://codecov.io/gh/thesis-php/clock/branch/0.1.x/graph/badge.svg)](https://codecov.io/gh/thesis-php/clock/tree/0.1.x)
[![Mutation testing badge](https://img.shields.io/endpoint?style=flat&url=https%3A%2F%2Fbadge-api.stryker-mutator.io%2Fgithub.com%2Fthesis-php%2Fclock%2F0.1.x)](https://dashboard.stryker-mutator.io/reports/github.com/thesis-php/clock/0.1.x)

## Installation

```shell
composer require thesis/clock
```

## Usage

`WallClock` is a basic implementation of the [`Psr\Clock\ClockInterface`](https://www.php-fig.org/psr/psr-20/) that returns the current wall-clock time.

```php
use Thesis\Time\WallClock;

$clock = new WallClock();

echo $clock->now()->format('c'); // Outputs current time in ISO 8601 format
```

Or with a specific timezone:

```php
$clock = new WallClock(new DateTimeZone('Europe/Moscow'));

echo $clock->now()->format('c'); // Outputs Moscow time in ISO 8601 format
```
