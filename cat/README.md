This directory contains solutions to some of the C verification benchmarks
in the paper [A benchmark for C program verification](http://www.cs.ru.nl/~freek/cbench/cbench.pdf).

For cat1, there is a choice of two solutions:
`cat1.c` and `verif_cat1.v` use the code as written, plus an axiom that there are enough resources for `putchar` to always succeed.
`cat1a.c` and `verif_cat1a.v` modify the code to check for failing `putchar`, and use no additional axioms.

## BUILD INSTRUCTIONS:

1. Install VST at some  path/to/VST

2. Choice:
  *  Install CompCert/clightgen at some   path/to/CompCert/clightgen (CompCert 3.5 or CompCert master branch)
  *  Or, don't install clightgen, just use the parsed ASTs in cat*.v

3. In this directory, create a CONFIGURE file 
    VST_LOC= path/to/VST
    COMPCERT_LOC= path/to/CompCert    (optional)

4.  "make -j"