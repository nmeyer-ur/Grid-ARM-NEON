ARMv8a 128-bit neon intrinsics port for Grid
supports double, single and half precision


file changes

    configure.ac
    Grid_vector_types.h
    Grid_generic_types.h
    Grid_neon.h


developed and tested with

    Grid git commit 4a8c4ccfba1d05159348d21a9698028ea847e77b
    Author: Guido Cossu <guido.cossu@ed.ac.uk>
    Date:   Fri Jun 2 17:02:29 2017 +0100

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


testing

    double precision

    arm.neon.clang_4.0.dp.bench.openmp.txt
    arm.neon.clang_4.0.dp.tests.openmp.txt

    single precision

    arm.neon.clang_4.0.sp.bench.openmp.txt
    arm.neon.clang_4.0.sp.tests.openmp.txt

