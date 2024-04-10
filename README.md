# liblbfgs - <SUMMARY>

[`liblbfgs`](https://github.com/chokkan/liblbfgs)
C library. It provides a C port of the implementation of Limited-memory
Broyden-Fletcher-Goldfarb-Shanno (L-BFGS) method written by Jorge Nocedal.
The original FORTRAN source code is available at:
http://www.ece.northwestern.edu/~nocedal/lbfgs.html

The L-BFGS method solves the unconstrainted minimization problem:
    minimize F(x), x = (x1, x2, ..., xN),
only if the objective function F(x) and its gradient G(x) are computable.

Refer to the libLBFGS web site for more information.
http://www.chokkan.org/software/liblbfgs/

This file contains setup instructions and other details that are more
appropriate for development rather than consumption. If you want to use
`liblbfgs` in your `build2`-based project, then instead see the accompanying
[`PACKAGE-README.md`](<PACKAGE>/PACKAGE-README.md) file.

The development setup for `liblbfgs` uses the standard `bdep`-based workflow.
For example:

```
git clone .../liblbfgs.git
cd liblbfgs

bdep init -C @gcc cc config.cxx=g++
bdep update
bdep test
```
