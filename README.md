# Cairo stubs

[Cairo](https://github.com/cairophp/cairo)'s PHP API as stubs, for IDEs and
static analysers: signatures and docblocks of every `Cairo\` class and
function, no bodies. Cairo itself is the `cairo` binary, which has the real
classes built in.

```sh
composer require --dev cairophp/stubs
```

PhpStorm and Intelephense index `cairo.php` from `vendor/`. For PHPStan,
include `vendor/cairophp/stubs/phpstan.neon` (phpstan/extension-installer does
that for you). For Psalm, list `vendor/cairophp/stubs/cairo.php` under
`<stubs>`. The package has no autoload entry on purpose: never `require` the
stubs, since Cairo already declares these classes.

This repository is a read-only mirror. It is generated from `stubs/` in
[cairophp/cairo](https://github.com/cairophp/cairo) with every release and
carries the same tags; open issues and pull requests there.
