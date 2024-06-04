# liblbfgs - A C library

This is a `build2` package for the [`liblbfgs`](https://github.com/chokkan/liblbfgs)
C library. It provides a C port of the implementation of Limited-memory
Broyden-Fletcher-Goldfarb-Shanno (L-BFGS) method written by Jorge Nocedal.
The original FORTRAN source code is available at:
http://www.ece.northwestern.edu/~nocedal/lbfgs.html

The L-BFGS method solves the unconstrainted minimization problem:
    minimize F(x), x = (x1, x2, ..., xN),
only if the objective function F(x) and its gradient G(x) are computable.

Refer to the libLBFGS web site for more information.
http://www.chokkan.org/software/liblbfgs/


## Usage

To start using `liblbfgs` in your project, add the following `depends`
value to your `manifest`, adjusting the version constraint as appropriate:

```
depends: liblbfgs ^1.1.0
```

Then import the library in your `buildfile`:

```
import libs = liblbfgs%lib{lbfgs}
```


## Importable targets

This package provides the following importable targets:

```
lib{lbfgs}
```

<DESCRIPTION-OF-IMPORTABLE-TARGETS>


## Configuration variables

This package provides the following configuration variables:

```
[bool] config.liblbfgs.use_double ?= true
[bool] config.liblbfgs.use_IEEE754 ?= true
[bool] config.liblbfgs.use_sse ?= true
```

- `use_double` enables double precision floating point arithmetics.
- `use_IEEE754` enables optimization routines for IEEE754 floating point values.
- `use_sse` enable SSE2 optimization routines.
