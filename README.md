# TYPO3 Opcache Control ![CI](https://github.com/pagemachine/typo3-opcache-control/workflows/CI/badge.svg)

PHP Opcache management for TYPO3

## Installation

Via [Composer](https://packagist.org/packages/pagemachine/typo3-opcache-control):

    composer require pagemachine/typo3-opcache-control

## Purpose

This package provides CLI commands for PHP Opcache management within TYPO3. This is essential to e.g. reset the Opcache on deployments.

Since the web Opcache is managed, resetting the Opcache is essentially the same as the related action in the TYPO3 backend.

## Usage

Use the TYPO3 CLI or TYPO3 Console to execute Opcache control commands.

The Opcache status can be checked using the `opcache:status` command:

```
$ typo3cms opcache:status
+---------------------------+------------------+
| opcache_enabled           | true             |
# ...
```

The Opcache can be reset using the `opcache:reset` command:

```
$ typo3cms opcache:reset
Success: opcache reset
```

The commands are executed with real HTTP requests, thus at least one valid site must be set up.
