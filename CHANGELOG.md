# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.0.0] - 2026-10-29

### Added

- Support for PHP 8.4 and 8.5 and for `nette/forms` 3.2 and 3.3 (from `nasext/dependent-select-box` 5.2.0: `setValue()` accepts a `BackedEnum`).
- GitHub Actions run the tests on PHP 8.3, 8.4 and 8.5 with the highest dependencies and on PHP 8.3 with the lowest dependencies, the tests report deprecations.

### Changed

- Minimal PHP version is 8.3, minimal versions are `nette/application` 3.1.15, `nette/forms` 3.2 and `nette/component-model` 3.0.3 (BC break).
- The link of the signal uses `IComponent::NameSeparator` instead of the deprecated `IComponent::NAME_SEPARATOR`.
- `DependentMultiSelectBox::setDisabled()` has the signature `setDisabled(array|bool $state = true): static` (BC break for subclasses).

### Removed

- The deprecated classes `NasExt\Forms\Controls\DependentSelectBoxData` and `NasExt\Forms\DI\DependentSelectBoxExtension` (BC break).
- Travis CI configuration.

### Fixed

- `DependentMultiSelectBox` caused a fatal error with `nette/forms` 3.2+, its `setDisabled()` was not compatible with `MultiChoiceControl::setDisabled()`.
- `DependentSelectBox::getValue()` returned a disabled item when the value was set before the items were loaded (e.g. a submitted form).
- The tests run with current versions of Nette (string POST data, forms allow cross-origin requests, the boolean attribute `multiple`, the items of the AJAX payload are a list).

## [1.0.0] - 2024-08-06

### Changed

- The package is renamed to `tg666/dependent-select-box`, a fork of `nasext/dependent-select-box` at commit `b2cc8e4` (2023-03-08).

### Fixed

- The return type of `DependentTrait::getValue()` is `mixed`.

[Unreleased]: https://github.com/tg666/DependentSelectBox/compare/2.0.0...HEAD
[2.0.0]: https://github.com/tg666/DependentSelectBox/compare/1.0.0...2.0.0
[1.0.0]: https://github.com/tg666/DependentSelectBox/releases/tag/1.0.0
