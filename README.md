<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# negaLucas

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the nth [negaLucas number][lucas-number].

<section class="intro">

The [negaLucas numbers][lucas-number] are the integer sequence

<!-- <equation class="equation" label="eq:negalucas_sequence" align="center" raw="2, -1, 3, -4, 7, -11, 18, -29, 47, -76, 123, -199, 322, \ldots" alt="NegaLucas sequence"> -->

```math
2, -1, 3, -4, 7, -11, 18, -29, 47, -76, 123, -199, 322, \ldots
```

<!-- <div class="equation" align="center" data-raw-text="2, -1, 3, -4, 7, -11, 18, -29, 47, -76, 123, -199, 322, \ldots" data-equation="eq:negalucas_sequence">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/negalucas/docs/img/equation_negalucas_sequence.svg" alt="NegaLucas sequence">
    <br>
</div> -->

<!-- </equation> -->

The sequence is defined by the recurrence relation

<!-- <equation class="equation" label="eq:negalucas_recurrence_relation" align="center" raw="L_{n-2} = L_{n} - L_{n-1}" alt="NegaLucas sequence recurrence relation"> -->

```math
L_{n-2} = L_{n} - L_{n-1}
```

<!-- <div class="equation" align="center" data-raw-text="L_{n-2} = L_{n} - L_{n-1}" data-equation="eq:negalucas_recurrence_relation">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/negalucas/docs/img/equation_negalucas_recurrence_relation.svg" alt="NegaLucas sequence recurrence relation">
    <br>
</div> -->

<!-- </equation> -->

which yields

<!-- <equation class="equation" label="eq:negalucas_lucas" align="center" raw="L_{-n} = (-1)^{n} L_n" alt="NegaLucas relationship to Lucas numbers"> -->

```math
L_{-n} = (-1)^{n} L_n
```

<!-- <div class="equation" align="center" data-raw-text="L_{-n} = (-1)^{n} L_n" data-equation="eq:negalucas_lucas">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/negalucas/docs/img/equation_negalucas_lucas.svg" alt="NegaLucas relationship to Lucas numbers">
    <br>
</div> -->

<!-- </equation> -->

with seed values `L_0 = 2` and `L_{-1} = -1`.

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import negalucas from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-negalucas@v0.2.0-deno/mod.js';
```

#### negalucas( n )

Computes the nth [negaLucas number][lucas-number].

```javascript
var v = negalucas( 0 );
// returns 2

v = negalucas( -1 );
// returns -1

v = negalucas( -2 );
// returns 3

v = negalucas( -3 );
// returns -4

v = negalucas( -76 );
// returns 7639424778862807
```

If `n < -76`, the function returns `NaN`, as larger [negaLucas numbers][lucas-number] cannot be safely represented in [double-precision floating-point format][ieee754].

```javascript
var v = negalucas( -77 );
// returns NaN
```

If not provided a nonpositive integer value, the function returns `NaN`.

```javascript
var v = negalucas( -3.14 );
// returns NaN

v = negalucas( 1 );
// returns NaN
```

If provided `NaN`, the function returns `NaN`.

```javascript
var v = negalucas( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="notes">

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import negalucas from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-negalucas@v0.2.0-deno/mod.js';

var v;
var i;

for ( i = 0; i > -77; i-- ) {
    v = negalucas( i );
    console.log( v );
}
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math-base/special/fibonacci`][@stdlib/math/base/special/fibonacci]</span><span class="delimiter">: </span><span class="description">compute the nth Fibonacci number.</span>
-   <span class="package-name">[`@stdlib/math-base/special/lucas`][@stdlib/math/base/special/lucas]</span><span class="delimiter">: </span><span class="description">compute the nth Lucas number.</span>
-   <span class="package-name">[`@stdlib/math-base/special/negafibonacci`][@stdlib/math/base/special/negafibonacci]</span><span class="delimiter">: </span><span class="description">compute the nth negaFibonacci number.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-negalucas.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-negalucas

[test-image]: https://github.com/stdlib-js/math-base-special-negalucas/actions/workflows/test.yml/badge.svg?branch=v0.2.0
[test-url]: https://github.com/stdlib-js/math-base-special-negalucas/actions/workflows/test.yml?query=branch:v0.2.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-negalucas/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-negalucas?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-negalucas.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-negalucas/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-negalucas/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-negalucas/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-negalucas/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-negalucas/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-negalucas/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-negalucas/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-negalucas/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-negalucas/main/LICENSE

[lucas-number]: https://en.wikipedia.org/wiki/Lucas_number

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

<!-- <related-links> -->

[@stdlib/math/base/special/fibonacci]: https://github.com/stdlib-js/math-base-special-fibonacci/tree/deno

[@stdlib/math/base/special/lucas]: https://github.com/stdlib-js/math-base-special-lucas/tree/deno

[@stdlib/math/base/special/negafibonacci]: https://github.com/stdlib-js/math-base-special-negafibonacci/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
