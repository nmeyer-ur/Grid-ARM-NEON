ARMv8a 128-bit neon port of Grid intrinsics layer

supports double, single and half precision


file changes

  configure.ac
  Grid_vector_types.h
  Grid_generic_types.h
  Grid_neon.h


tested with

  git commit

  clang 3.8 (no OpenMP support on our system)
  clang 4.0.0 (has OpenMP)
  gcc 6.3.0 (has OpenMP)

  with and without openmp


configure Grid using

  configure CXX=... CXXFLAGS="-std=c++11 -O3 -D NEONv8" --enable-simd=NEONv8


notes

  Vset is defined but not used by Grid, currently untested
  prefetches missing, intrinsics-level commands unknown
  streaming missing, intrinsics-level commands unknown

  gcc 6.3.0 compile time is high
