<!--

@license Apache-2.0

Copyright (c) 2020 The Stdlib Authors.

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

# Square Root

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the principal [square root][square-root] of a single-precision floating-point number.

<section class="intro">

The principal [square root][square-root] is defined as

<!-- <equation class="equation" label="eq:principal_square_root" align="center" raw="\sqrt{x^2} = \begin{matrix} x, & \textrm{if}\ x \geq 0\end{matrix}" alt="Principal square root"> -->

<div class="equation" align="center" data-raw-text="\sqrt{x^2} = \begin{matrix} x, &amp; \textrm{if}\ x \geq 0\end{matrix}" data-equation="eq:principal_square_root">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@fd65465ee942bbb6e3856d58268e1ee90d570989/lib/node_modules/@stdlib/math/base/special/sqrtf/docs/img/equation_principal_square_root.svg" alt="Principal square root">
    <br>
</div>

<!-- </equation> -->

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-sqrtf
```

</section>

<section class="usage">

## Usage

```javascript
var sqrtf = require( '@stdlib/math-base-special-sqrtf' );
```

#### sqrtf( x )

Computes the principal [square root][square-root] of a single-precision floating-point number.

```javascript
var v = sqrtf( 4.0 );
// returns 2.0

v = sqrtf( 9.0 );
// returns 3.0

v = sqrtf( 0.0 );
// returns 0.0

v = sqrtf( NaN );
// returns NaN
```

For negative numbers, the principal [square root][square-root] is **not** defined.

```javascript
var v = sqrtf( -4.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var sqrtf = require( '@stdlib/math-base-special-sqrtf' );

var x;
var i;

for ( i = 0; i < 100; i++ ) {
    x = round( randu() * 100.0 );
    console.log( 'sqrt(%d) = %d', x, sqrtf( x ) );
}
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-sqrtf
```

</section>

<section class="usage">

### Usage

```c
#include "stdlib/math/base/special/sqrtf.h"
```

#### stdlib_base_sqrtf( x )

Computes the principal [square root][square-root] of a single-precision floating-point number.

```c
float y = stdlib_base_sqrtf( 9.0f );
// returns 3.0f
```

The function accepts the following arguments:

-   **x**: `[in] float` input value.

```c
float stdlib_base_sqrtf( const float x );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/math/base/special/sqrtf.h"
#include <stdio.h>

int main() {
    float x[] = { 3.14f, 9.0f, 0.0f, 0.0f/0.0f };

    float y;
    int i;
    for ( i = 0; i < 4; i++ ) {
        y = stdlib_base_sqrtf( x[ i ] );
        printf( "sqrt(%f) = %f\n", x[ i ], y );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math/base/special/cbrtf`][@stdlib/math/base/special/cbrtf]</span><span class="delimiter">: </span><span class="description">compute the cube root of a single-precision floating-point number.</span>
-   <span class="package-name">[`@stdlib/math/base/special/rsqrtf`][@stdlib/math/base/special/rsqrtf]</span><span class="delimiter">: </span><span class="description">compute the reciprocal square root of a single-precision floating-point number.</span>
-   <span class="package-name">[`@stdlib/math/base/special/sqrt`][@stdlib/math/base/special/sqrt]</span><span class="delimiter">: </span><span class="description">compute the principal square root of a double-precision floating-point number.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-sqrtf.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-sqrtf

[test-image]: https://github.com/stdlib-js/math-base-special-sqrtf/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/math-base-special-sqrtf/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-sqrtf/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-sqrtf?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-sqrtf.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-sqrtf/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-sqrtf/main/LICENSE

[square-root]: https://en.wikipedia.org/wiki/Square_root

<!-- <related-links> -->

[@stdlib/math/base/special/cbrtf]: https://github.com/stdlib-js/math-base-special-cbrtf

[@stdlib/math/base/special/rsqrtf]: https://github.com/stdlib-js/math-base-special-rsqrtf

[@stdlib/math/base/special/sqrt]: https://github.com/stdlib-js/math-base-special-sqrt

<!-- </related-links> -->

</section>

<!-- /.links -->
