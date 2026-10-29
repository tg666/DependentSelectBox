# Dependent Select Box

Dependent Select Box for [Nette Framework](https://nette.org).

A maintained fork of [NasExt/DependentSelectBox](https://github.com/NasExt/DependentSelectBox) (`nasext/dependent-select-box`). The namespace `NasExt\Forms` and the API are the same, only the package name differs.

[![Tests](https://github.com/tg666/DependentSelectBox/actions/workflows/tests.yml/badge.svg)](https://github.com/tg666/DependentSelectBox/actions/workflows/tests.yml)

## Installation

The best way to install the package is using [Composer](https://getcomposer.org/):

```sh
$ composer require tg666/dependent-select-box
```

Requirements: PHP `^8.3`, `nette/application` `^3.1.15`, `nette/forms` `^3.2` and `nette/component-model` `^3.0.3`.

## Upgrade

### From `nasext/dependent-select-box` 5.x

Replace the package in `composer.json`, the code doesn't change. Version 2.0 contains all changes of `nasext/dependent-select-box` 5.2.0.

### From 1.x to 2.0

- The minimal PHP version is 8.3, the minimal versions are `nette/application` 3.1.15, `nette/forms` 3.2 and `nette/component-model` 3.0.3.
- The deprecated classes `NasExt\Forms\Controls\DependentSelectBoxData` and `NasExt\Forms\DI\DependentSelectBoxExtension` are removed. Use `NasExt\Forms\DependentData` and `NasExt\Forms\DependentExtension`.
- `DependentMultiSelectBox::setDisabled()` has the signature of `nette/forms` 3.2: `setDisabled(array|bool $state = true): static`.

## Documentation

Learn more in the [documentation](doc/index.md).
