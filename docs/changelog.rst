Changelog
=========

2017-05-12
----------

- removed entrypoint magic
- 0.10.0


2017-03-25 0.9.0
----------------

- added `And` trafaret and `&` shortcut operation.
- change `>>` behaviour. From now on Trafaret does not use self.converters and use `And` trafaret instead
- added `RegxpRaw` and `Regexp` trafarets. `RegexpRaw` returns re.Match object and `Regexp` returns match string.
- deprecate `String` `regex` argument in favor to `Regexp` and `RegexpRaw` usage
- `Dict` now takes `allow_extra`, `allow_extra_trafaret` and `ignore_extra` keyword arguments as preferred alternative to methods


0.8.1
-----

- added trafaret.constructor. Now you can use `construct` and `C` from this package.


2016-09-25
----------

Added `trafaret` argument to `DataError` constructor and made `_failure`
a method (rather than static method)


2016-08-03
----------

Added `Subclass` trafaret.


2016-03-31
----------

Fixed loading contrib modules, so now original contrib module loading exception will be raised on contrib Trafaret access.
Added `value` option to internal _failure interface, and option `value` to `DataError.as_dict` method.


2016-03-18
----------

Fixed Key default behaviour for Dict with allowed extra when names are the
same in Key and in data source


2014-09-17
----------

Fixed Email validator


2012-05-30
----------

Renamed methods to `check_value` and `check_and_return`.
Added `Tuple` trafaret.


2012-05-28
----------

Fixed `Dict(...).make_optional(...)` method for a chaining support


2012-05-21
----------

Updated `KeysSubSet` errors propagation - now you can return error either
`{'a': DataError('message')}`, or `DataError({'a': 'message'})`


2012-05-16
----------

Added `__call__` alias to `check`.


2012-05-11
----------

Added `visitor` module.


2012-05-10
----------

Fixed `Dict.allow_extra` behaviour.


2012-04-12
----------

`Int` will not convert not-rounded floats like 2.2

`Dict` have `.ignore_extra` method, similar to `.allow_extra`, but given keys
will not included to result dict. If you will provide `*`, any extra will be ignored.
