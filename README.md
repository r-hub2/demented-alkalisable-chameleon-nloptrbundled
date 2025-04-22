
<!-- README.md is generated from README.Rmd. Please edit that file -->

# nloptrbundled

<!-- badges: start -->

[![R-CMD-check](https://github.com/astamm/nloptrbundled/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/astamm/nloptrbundled/actions/workflows/R-CMD-check.yaml)
[![Codecov test
coverage](https://codecov.io/gh/astamm/nloptrbundled/graph/badge.svg)](https://app.codecov.io/gh/astamm/nloptrbundled)
<!-- badges: end -->

**nloptrbundled** is an R interface to
[NLopt](https://nlopt.readthedocs.io/en/latest/), a free/open-source
library for nonlinear optimization started by Steven G. Johnson,
providing a common interface for a number of different free optimization
routines available online as well as original implementations of various
other algorithms. It can be used to solve general nonlinear programming
problems with nonlinear constraints and lower and upper bounds for the
controls, such as:

$$ \min_{x \in \mathbb{R}^n} \quad f(x), $$

s.t. $g(x) \le 0$, $h(x) = 0$ and $\ell \le x \le u$.

The [NLopt](https://nlopt.readthedocs.io/en/latest/) library is
available under the GNU Lesser General Public License (LGPL), and the
copyrights are owned by a variety of authors. See the
[website](https://nlopt.readthedocs.io/en/latest/Citing_NLopt/) for
information on how to cite NLopt and the algorithms you use.

## Installation

[NLopt](https://nlopt.readthedocs.io/en/latest/) 2.10.0 is built from
included sources using [CMake](https://cmake.org). Specifically, a
binary of [CMake](https://cmake.org) stored in environment variable
`CMAKE_BIN` is searched on the `PATH` and, alternatively, on a
macOS-specific location. If that variable cannot be set, install will
abort suggesting ways of installing [CMake](https://cmake.org). The
minimal version requirement on `cmake` is `>= 3.15.0`.

### Installing [CMake](https://cmake.org)

You can install [CMake](https://cmake.org) by following [CMake
installation instructions](https://cmake.org/resources/). The important
thing is that you add the [CMake](https://cmake.org) binary to your
`PATH`:

- On macOS, you can install [CMake](https://cmake.org) and then run it.
  In the menu bar, there is an item *How to Install For Command Line
  Use* which you can click on to have proper instructions on how to
  update your `PATH`. Note that the location of the
  [CMake](https://cmake.org) binary is always
  `/Applications/CMake.app/Contents/bin/cmake`. Hence, **nloptrbundled**
  knows where to find it even if you do not update your `PATH`.
- On Linux, it will be automatically added unless you specifically
  change the default installation directory before building
  [CMake](https://cmake.org).

Alternatively, you can set an environment variable `CMAKE_BIN` pointing
to a [CMake](https://cmake.org) binary of your liking on your computer
for **nloptrbundled** to use.

### Installing **nloptrbundled**

You can install the development version from GitHub:

``` r
# install.packages("pak")
pak::pak("astamm/nloptrbundled")
```

## Acknowledgments

I would like to express my sincere gratitude to [Avraham
Adler](https://github.com/aadler), [Tomas
Kalibera](https://github.com/kalibera), [Jeroen
Ooms](https://github.com/jeroen) and [Jelmer
Ypma](https://github.com/jyypma) for their contributions and the very
instructive discussions about the pros and cons of various build
strategies in R packages.

## Reference

Steven G. Johnson, The NLopt nonlinear-optimization package,
<https://nlopt.readthedocs.io/en/latest/>
