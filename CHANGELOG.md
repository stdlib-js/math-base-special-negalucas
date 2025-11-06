# CHANGELOG

> Package changelog.

<section class="release" id="unreleased">

## Unreleased (2025-11-06)

<section class="reverts">

### Reverts

-   [`d8a4cfb`](https://github.com/stdlib-js/stdlib/commit/d8a4cfb578a949ed07c7a18749e48096f4f9b488) - chore: update to modern benchmark Makefile

</section>

<!-- /.reverts -->

<section class="breaking-changes">

### BREAKING CHANGES

-   [`801494f`](https://github.com/stdlib-js/stdlib/commit/801494fbca7a4db22753f7417267502d98ba1b31): update signature to accept doubles

    -   User code should behave similarly in the primary case of providing integer-valued input values. However, no longer will real-values truncate. Now, real-valued inputs will result in `NaN`, which is, arguably, better behavior, as real-to-integer truncation can be a source of silent bugs.

</section>

<!-- /.breaking-changes -->

<section class="commits">

### Commits

<details>

-   [`147344e`](https://github.com/stdlib-js/stdlib/commit/147344eb928314b046645fac287a6d96516c400d) - **chore:** add structured package data for `math/base/special/negalucas` [(#8401)](https://github.com/stdlib-js/stdlib/pull/8401) _(by Manvith M)_
-   [`81f904d`](https://github.com/stdlib-js/stdlib/commit/81f904da25808197e2ae83ebf9c8b26860855e7c) - **bench:** fix failing C benchmarks by using `round` and `roundf` [(#7980)](https://github.com/stdlib-js/stdlib/pull/7980) _(by Gunj Joshi)_
-   [`801494f`](https://github.com/stdlib-js/stdlib/commit/801494fbca7a4db22753f7417267502d98ba1b31) - **refactor:** modify C implementation to accept `double` value instead of `int32` in `math/base/special/negalucas` [(#7955)](https://github.com/stdlib-js/stdlib/pull/7955) _(by Gunj Joshi)_
-   [`3425c5a`](https://github.com/stdlib-js/stdlib/commit/3425c5a231e90c72af55fc462e8aa18401a9ebdf) - **bench:** add missing `native.js` and fix variable range [(#6467)](https://github.com/stdlib-js/stdlib/pull/6467) _(by Karan Anand, stdlib-bot)_
-   [`e9f9513`](https://github.com/stdlib-js/stdlib/commit/e9f951387dd4387dc0a7b4acfadc59c5b2541736) - **bench:** update random value generation [(#6430)](https://github.com/stdlib-js/stdlib/pull/6430) _(by Harsh Yadav)_
-   [`c13062e`](https://github.com/stdlib-js/stdlib/commit/c13062e5b90cbe28ec62f0b690211bd14b626cf3) - **style:** update to use tabs for indentation _(by Philipp Burckhardt)_
-   [`6a0d6b8`](https://github.com/stdlib-js/stdlib/commit/6a0d6b861f8e2079a501ca4e46a9175440eedb46) - **style:** update to use tabs for indentation _(by Philipp Burckhardt)_
-   [`6bbf2d6`](https://github.com/stdlib-js/stdlib/commit/6bbf2d67034e056190594bf2bceca4eb40a66b6f) - **style:** fix indentation _(by Philipp Burckhardt)_
-   [`b0e68c5`](https://github.com/stdlib-js/stdlib/commit/b0e68c5bc8ee985794eb2ea1791c9337cd15fbd0) - **chore:** update to modern benchmark Makefile _(by Philipp Burckhardt)_
-   [`d8a4cfb`](https://github.com/stdlib-js/stdlib/commit/d8a4cfb578a949ed07c7a18749e48096f4f9b488) - **revert:** chore: update to modern benchmark Makefile _(by Philipp Burckhardt)_
-   [`97a27cf`](https://github.com/stdlib-js/stdlib/commit/97a27cf2746042026c3e68416b7c5f9da2bb24d9) - **chore:** update to modern benchmark Makefile _(by Philipp Burckhardt)_

</details>

</section>

<!-- /.commits -->

<section class="contributors">

### Contributors

A total of 5 people contributed to this release. Thank you to the following contributors:

-   Gunj Joshi
-   Harsh Yadav
-   Karan Anand
-   Manvith M
-   Philipp Burckhardt

</section>

<!-- /.contributors -->

</section>

<!-- /.release -->

<section class="release" id="v0.2.2">

## 0.2.2 (2024-07-28)

<section class="commits">

### Commits

<details>

-   [`2777e4b`](https://github.com/stdlib-js/stdlib/commit/2777e4be161869d09406e3b17947d24c64b47af2) - **bench:** resolve lint errors in benchmarks _(by Athan Reines)_

</details>

</section>

<!-- /.commits -->

<section class="contributors">

### Contributors

A total of 1 person contributed to this release. Thank you to this contributor:

-   Athan Reines

</section>

<!-- /.contributors -->

</section>

<!-- /.release -->

<section class="release" id="v0.2.1">

## 0.2.1 (2024-02-24)

No changes reported for this release.

</section>

<!-- /.release -->

<section class="release" id="v0.2.0">

## 0.2.0 (2024-02-14)

<section class="commits">

### Commits

<details>

-   [`215dfe6`](https://github.com/stdlib-js/stdlib/commit/215dfe690670731f044d09c92832081bc99372cc) - **docs:** update links _(by Athan Reines)_

</details>

</section>

<!-- /.commits -->

<section class="contributors">

### Contributors

A total of 1 person contributed to this release. Thank you to this contributor:

-   Athan Reines

</section>

<!-- /.contributors -->

</section>

<!-- /.release -->

<section class="release" id="v0.1.0">

## 0.1.0 (2023-09-24)

<section class="features">

### Features

-   [`58832ee`](https://github.com/stdlib-js/stdlib/commit/58832eef6d93e6519622148242600eae93dca4d9) - update minimum TypeScript version
-   [`60429f5`](https://github.com/stdlib-js/stdlib/commit/60429f55de228f0d415751a1f3292b2cac123600) - add C API to `@stdlib/math-base/special/negalucas` [(#913)](https://github.com/stdlib-js/stdlib/pull/913)

</section>

<!-- /.features -->

<section class="breaking-changes">

### BREAKING CHANGES

-   [`58832ee`](https://github.com/stdlib-js/stdlib/commit/58832eef6d93e6519622148242600eae93dca4d9): update minimum TypeScript version to 4.1

    -   To migrate, users should upgrade their TypeScript version to at least version 4.1.

</section>

<!-- /.breaking-changes -->

<section class="issues">

### Closed Issues

This release closes the following issue:

[#893](https://github.com/stdlib-js/stdlib/issues/893)

</section>

<!-- /.issues -->

<section class="commits">

### Commits

<details>

-   [`58832ee`](https://github.com/stdlib-js/stdlib/commit/58832eef6d93e6519622148242600eae93dca4d9) - **feat:** update minimum TypeScript version _(by Philipp Burckhardt)_
-   [`28e1c84`](https://github.com/stdlib-js/stdlib/commit/28e1c84390d88044883c9ef940a12f38d66ea3ef) - **docs:** resolve C lint errors _(by Athan Reines)_
-   [`c5da1f9`](https://github.com/stdlib-js/stdlib/commit/c5da1f9a22b1033d40115798acf13a09acf9410d) - **docs:** render equations via math code blocks _(by Philipp Burckhardt)_
-   [`01a8ecb`](https://github.com/stdlib-js/stdlib/commit/01a8ecbc37710514cf17d17f12d29cef3affd9c2) - **chore:** update package meta data [(#967)](https://github.com/stdlib-js/stdlib/pull/967) _(by stdlib-bot, Athan Reines)_
-   [`60429f5`](https://github.com/stdlib-js/stdlib/commit/60429f55de228f0d415751a1f3292b2cac123600) - **feat:** add C API to `@stdlib/math-base/special/negalucas` [(#913)](https://github.com/stdlib-js/stdlib/pull/913) _(by Jordan Gallivan, Pranav, Athan Reines)_

</details>

</section>

<!-- /.commits -->

<section class="contributors">

### Contributors

A total of 4 people contributed to this release. Thank you to the following contributors:

-   Athan Reines
-   Jordan Gallivan
-   Philipp Burckhardt
-   Pranav Goswami

</section>

<!-- /.contributors -->

</section>

<!-- /.release -->

<section class="release" id="v0.0.6">

## 0.0.6 (2022-02-16)

No changes reported for this release.

</section>

<!-- /.release -->

<section class="release" id="v0.0.5">

## 0.0.5 (2021-08-23)

No changes reported for this release.

</section>

<!-- /.release -->

<section class="release" id="v0.0.4">

## 0.0.4 (2021-07-07)

No changes reported for this release.

</section>

<!-- /.release -->

<section class="release" id="v0.0.3">

## 0.0.3 (2021-06-27)

No changes reported for this release.

</section>

<!-- /.release -->

<section class="release" id="v0.0.2">

## 0.0.2 (2021-06-16)

No changes reported for this release.

</section>

<!-- /.release -->

<section class="release" id="v0.0.1">

## 0.0.1 (2021-06-15)

No changes reported for this release.

</section>

<!-- /.release -->

