# Vectorized Riemann solver.

## Functions profile.

<img src="exe_prof.png" width="30%">

## Vectorization effectiveness.

![effectiveness](effectiveness.png "Vectorization effectiveness")

## Build and run.

`./comp_icc.sh` - build with icc compiler

flags:
- `-DOPENMP_CHUNKS` - strategy for OpenMP
- `-DTEST_MODE=1` - big test mode
- `-DREPEATS_ORIG=1` - repeats number for scalar version of code
- `-DREPEATS_OPT=10` - repeats number for vector version of code
- `-DINNER_REPEATS=100` - repeats number for processing arrays

run test:

`./riemann.out <lo_threads> <hi_threads>`

Solver will run for threads number from <lo_thread> to <hi_threads>.

Run results are printed into stdout.
