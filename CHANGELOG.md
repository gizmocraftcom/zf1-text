# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-text`, published as `gizmocraft/zendframework1-text`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-text` to `gizmocraft/zendframework1-text`. It now requires `gizmocraft/zendframework1-exception` `^2.0.0`, `gizmocraft/zendframework1-config` `^3.0.0` and `gizmocraft/zendframework1-loader` `^2.0.0`.

### Other changes

- No public signature changes.
- `Zend_Text_Figlet`: cast the font header smush value to `int` before the bit mask (PHPStan finding, same behaviour). `Zend_Text_Table_Decorator_Unicode::_uniChar()` masks the single-byte code point with `0xFF` before `chr()`; same result as before.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes. Two obsolete PHPStan ignores removed.
- CI runs PHP 8.5 and 8.6.
