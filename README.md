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

# until

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Invoke a function until a test condition is true.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import until from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-until@v0.2.0-deno/mod.js';
```

#### until( predicate, fcn\[, thisArg ] )

Invokes a `function` until a `predicate` function returns `true`.

```javascript
function predicate( i ) {
    return ( i >= 5 );
}

function beep( i ) {
    console.log( 'boop: %d', i );
}

until( predicate, beep );
/* =>
    boop: 0
    boop: 1
    boop: 2
    boop: 3
    boop: 4
*/
```

Both the `predicate` function and the `function` to invoke are provided a single argument:

-   `i`: iteration number (starting from zero)

To set the function execution context for the invoked function, provide a `thisArg`.

```javascript
function predicate( i ) {
    return ( i >= 5 );
}

function count() {
    this.count += 1;
}

var context = {
    'count': 0
};

until( predicate, count, context );

console.log( context.count );
// => 5
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@deno/mod.js';
import until from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-until@v0.2.0-deno/mod.js';

function predicate() {
    return ( randu() <= 0.05 );
}

function log( i ) {
    console.log( i );
}

until( predicate, log );
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/utils-do-until`][@stdlib/utils/do-until]</span><span class="delimiter">: </span><span class="description">invoke a function until a test condition is true.</span>
-   <span class="package-name">[`@stdlib/utils-do-while`][@stdlib/utils/do-while]</span><span class="delimiter">: </span><span class="description">invoke a function while a test condition is true.</span>
-   <span class="package-name">[`@stdlib/utils-async/until`][@stdlib/utils/async/until]</span><span class="delimiter">: </span><span class="description">invoke a function until a test condition is true.</span>
-   <span class="package-name">[`@stdlib/utils-until-each`][@stdlib/utils/until-each]</span><span class="delimiter">: </span><span class="description">until a test condition is true, invoke a function for each element in a collection.</span>
-   <span class="package-name">[`@stdlib/utils-while`][@stdlib/utils/while]</span><span class="delimiter">: </span><span class="description">invoke a function while a test condition is true.</span>

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/utils-until.svg
[npm-url]: https://npmjs.org/package/@stdlib/utils-until

[test-image]: https://github.com/stdlib-js/utils-until/actions/workflows/test.yml/badge.svg?branch=v0.2.0
[test-url]: https://github.com/stdlib-js/utils-until/actions/workflows/test.yml?query=branch:v0.2.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/utils-until/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/utils-until?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/utils-until.svg
[dependencies-url]: https://david-dm.org/stdlib-js/utils-until/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/utils-until/tree/deno
[deno-readme]: https://github.com/stdlib-js/utils-until/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/utils-until/tree/umd
[umd-readme]: https://github.com/stdlib-js/utils-until/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/utils-until/tree/esm
[esm-readme]: https://github.com/stdlib-js/utils-until/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/utils-until/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-until/main/LICENSE

<!-- <related-links> -->

[@stdlib/utils/do-until]: https://github.com/stdlib-js/utils-do-until/tree/deno

[@stdlib/utils/do-while]: https://github.com/stdlib-js/utils-do-while/tree/deno

[@stdlib/utils/async/until]: https://github.com/stdlib-js/utils-async-until/tree/deno

[@stdlib/utils/until-each]: https://github.com/stdlib-js/utils-until-each/tree/deno

[@stdlib/utils/while]: https://github.com/stdlib-js/utils-while/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
