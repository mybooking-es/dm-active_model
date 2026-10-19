# Changelog

## 1.4.0 - 2026-10-19

- Support ActiveModel / ActiveSupport 7.x (`activemodel >= 3.0, < 8.0`).
- `DataMapper::ActiveModel::InstanceMethods` is now an `ActiveSupport::Concern`, so
  `ActiveModel::Conversion` is included in the model class. Since ActiveModel 7.1 its
  `included` block calls `class_attribute :param_delimiter`, which raised `NoMethodError`
  when included in a plain module.
- Require `active_support` before any core extension (needed since ActiveSupport 7.1) and
  `active_support/core_ext/class/attribute` (used by `ActiveModel::Conversion`).
- Models now get the `param_delimiter=` writer from `ActiveModel::Conversion`; `to_param`
  is still the gem's own implementation.

## 1.3.0.beta - 2021-02-10

- Support ActiveModel 6.x (`activemodel >= 3.0, < 7.0`).

## Earlier versions

See [CHANGELOG](CHANGELOG) (generated from the upstream datamapper history).
