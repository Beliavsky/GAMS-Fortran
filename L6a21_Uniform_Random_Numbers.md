## GAMS Class L6a21: Uniform (Continuous and Discrete) Random Numbers, Random Uniform Order Statistics

The GAMS Class L6a21, "Uniform (continuous and discrete) random numbers, random uniform order statistics," focuses on generating pseudorandom numbers from uniform distributions (continuous over intervals like [0,1] or (0,1), discrete over integer ranges) and uniform order statistics. 


### Modern Fortran Codes (Fortran 90 and Later)

#### 1. GitHub: jannisteunissen/rng_fortran
- **Description**: A modern Fortran RNG using the xoroshiro128+ algorithm, supporting uniform random numbers and OpenMP parallelism.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers over [0,1), like `G05SAF`.  
- **Source**: [github.com/jannisteunissen/rng_fortran](https://github.com/jannisteunissen/rng_fortran)  
- **Notes**: High-performance, listed in [github.com/Beliavsky/Fortran-code-on-GitHub](https://github.com/Beliavsky/Fortran-code-on-GitHub).

#### 2. GitHub: leonfoks/coretran (Prng_Class)
- **Description**: A Fortran library with a `Prng_Class` module using xorshift128+ or xorshift1024* algorithms, supporting uniform distributions and thread safety with OpenMP/MPI.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers over [0,1), akin to `RNUNF`.  
  - **Uniform (discrete)**: Supports uniform integer generation, like `G05TLF`.  
- **Source**: [github.com/leonfoks/coretran](https://github.com/leonfoks/coretran)  
- **Notes**: Versatile, listed in [github.com/Beliavsky/Fortran-code-on-GitHub](https://github.com/Beliavsky/Fortran-code-on-GitHub).

#### 3. SPRNG (Scalable Parallel Random Number Generator)
- **Description**: A Fortran 90 library for scalable parallel RNGs, supporting Monte Carlo applications with uniform random number generation and MPI interfacing.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers over [0,1), like `G05LGF`.  
- **Source**: [netlib.org/random/sprng.tar.gz](http://netlib.org/random/sprng.tar.gz) or TOMS 806 ([netlib.org/toms/806-FORTRAN](http://netlib.org/toms/806-FORTRAN))  
- **Notes**: Ideal for parallel computing; robust for large-scale use.

#### 4. GitHub: fortran-lang/stdlib (Proposed RNG Module)
- **Description**: A developing Fortran Standard Library module proposing a uniform RNG over [0,1) with thread-safe options.
- **Relevance**:  
  - **Uniform (continuous)**: Aims to provide a standard uniform RNG, similar to `RNUNF`.  
- **Source**: [github.com/fortran-lang/stdlib](https://github.com/fortran-lang/stdlib)  
- **Notes**: In progress; reflects modern Fortran RNG goals.

#### 5. Alan Miller: luxury.f90
- **Description**: A Fortran 90 uniform RNG providing “luxury” random numbers with enhanced statistical properties, translated from earlier work.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers over [0,1), akin to `RNUN` or `G05KAF`.  
- **Source**: [jblevins.org/mirror/amiller/luxury.f90](https://jblevins.org/mirror/amiller/luxury.f90)  
- **Notes**: Public domain; includes a test program `luxtst.f90`.

#### 6. Alan Miller: taus88.f90 and lfsr113.f90
- **Description**: Fortran 90 implementations of L’Ecuyer’s Tausworthe RNGs: `taus88` (cycle 2^88) and `lfsr113` (cycle 2^113), generating uniform random numbers.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers over [0,1), similar to `UNI` or `DUNI`.  
- **Source**: [jblevins.org/mirror/amiller/taus88.f90](https://jblevins.org/mirror/amiller/taus88.f90), [jblevins.org/mirror/amiller/lfsr113.f90](https://jblevins.org/mirror/amiller/lfsr113.f90)  
- **Notes**: High-quality RNGs; assumes 32-bit integers.

#### 7. Alan Miller: ziggurat.f90
- **Description**: Fortran 90 implementation of Marsaglia’s Ziggurat method for uniform, normal, and exponential distributions.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers as a base, like `G05SAF`.  
- **Source**: [jblevins.org/mirror/amiller/ziggurat.f90](https://jblevins.org/mirror/amiller/ziggurat.f90)  
- **Notes**: Efficient; public domain.

#### 8. John Burkardt: uniform
- **Description**: A Fortran 90 library returning a sequence of uniformly distributed pseudorandom numbers using a simple linear congruential generator (LCG) from the IBM System 360.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers over [0,1), akin to `RAND` or `RUNIF`.  
- **Source**: [people.sc.fsu.edu/~jburkardt/f_src/uniform/uniform.f90](https://people.sc.fsu.edu/~jburkardt/f_src/uniform/uniform.f90)  
- **Notes**: Basic method; portable but not state-of-the-art.

#### 9. John Burkardt: ranlib
- **Description**: A Fortran 90 library by Barry Brown and James Lovato, adapted by Burkardt, generating random samples from multiple PDFs, including uniform continuous and discrete.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers on [0,1], like `RNUN`.  
  - **Uniform (discrete)**: Supports uniform integer generation, akin to `RNUND`.  
- **Source**: [people.sc.fsu.edu/~jburkardt/f_src/ranlib/ranlib.f90](https://people.sc.fsu.edu/~jburkardt/f_src/ranlib/ranlib.f90)  
- **Notes**: Requires RNGLIB; robust with multiple streams.

#### 10. John Burkardt: ziggurat
- **Description**: A Fortran 90 library implementing Marsaglia’s Ziggurat method for uniform, normal, and exponential distributions.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers as a base, similar to `G05KAC`.  
- **Source**: [people.sc.fsu.edu/~jburkardt/f_src/ziggurat/ziggurat.f90](https://people.sc.fsu.edu/~jburkardt/f_src/ziggurat/ziggurat.f90)  
- **Notes**: Efficient; includes OpenMP example.

### Fortran 77 Codes

#### 11. Netlib’s ZUFALL (Uniform Random Number Generator)
- **Description**: A Fortran 77 package by W.P. Petersen providing subroutines for generating vectors of uniform, normal, and Poisson random numbers using a lagged (-273, -607) Fibonacci series algorithm.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers over [0,1], akin to `RAND` or `G05KAF`.  
- **Source**: [netlib.org/zufall/zufall.f](http://netlib.org/zufall/zufall.f)  
- **Notes**: Portable and fast; optimized for specific processors.

#### 12. TIMESLAB (Random Number Generation Component)
- **Description**: A Fortran 77 package by H. Joseph Newton for time series analysis, including a uniform random number generator for simulations.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers on [0,1], similar to `UNIRAN` or `RNUN`.  
- **Source**: [faculty.stat.tamu.edu/~hjn/timeslab.html](http://faculty.stat.tamu.edu/~hjn/timeslab.html) or [github.com/Beliavsky/Timeslab](https://github.com/Beliavsky/Timeslab)  
- **Notes**: Basic RNG within a broader package.

#### 13. Netlib’s RANLIB
- **Description**: A Fortran 77 library by Barry W. Brown and James Lovato for random number generation from multiple distributions, including uniform, using L’Ecuyer and Cote’s algorithm.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers on [0,1], similar to `RAND`.  
  - **Uniform (discrete)**: Supports uniform integer generation, akin to `RNUND`.  
- **Source**: [netlib.org/random/ranlib.f.tar.gz](http://netlib.org/random/ranlib.f.tar.gz)  
- **Notes**: Robust; requires RNGLIB for multiple streams.

#### 14. TOMS Algorithm 599 (SUNIF)
- **Description**: A Fortran 77 function `SUNIF` by Ahrens et al. (ACM TOMS, 1983) for sampling from the uniform (0,1) distribution.
- **Relevance**:  
  - **Uniform (continuous)**: Implements a uniform RNG on (0,1), matching `G05CAC`.  
- **Source**: [netlib.org/toms/599](http://netlib.org/toms/599)  
- **Notes**: High statistical quality; older code.

#### 15. Richard Chandler’s Random Number Generator
- **Description**: Fortran 77 code by Richard Chandler (UCL) for generating random numbers from multiple distributions, including uniform continuous and discrete.
- **Relevance**:  
  - **Uniform (continuous)**: Generates uniform random numbers on [0,1], like `G05KAC`.  
  - **Uniform (discrete)**: Supports uniform integer generation, akin to `G05DYC`.  
- **Source**: [ucl.ac.uk/~ucakarc/work/software/randgen.f](https://www.ucl.ac.uk/~ucakarc/work/software/randgen.f)  
- **Notes**: Updated in 2003; portable with good properties.

---

## Analysis and Coverage
- **Uniform (continuous)**: Extensively covered by modern codes (`rng_fortran`, `coretran`, `SPRNG`, `stdlib`, Miller’s `luxury.f90`, `taus88.f90`, `lfsr113.f90`, `ziggurat.f90`, Burkardt’s `uniform`, `ranlib`, `ziggurat`) and Fortran 77 codes (`ZUFALL`, `TIMESLAB`, `RANLIB`, `SUNIF`, Chandler’s RNG), aligning with `RAND`, `G05SAF`, `RNUN`.  
- **Uniform (discrete)**: Supported by `coretran`, Burkardt’s `ranlib`, Chandler’s RNG, and `RANLIB`, matching `RNUND`, `G05TLF`.  
- **Uniform order statistics**: Not explicitly implemented. Order statistics (e.g., `RNUNO`) require sorting uniform samples (feasible with `RANLIB`, `coretran`, or Miller’s RNGs plus a sorting routine), indicating a gap.

The GAMS list includes `NAG G05KAF` (continuous), `IMSL RNUND` (discrete), and `RNUNO` (order statistics). Continuous uniform RNGs are abundant, discrete uniform is less common, and order statistics need adaptation.

---

## Conclusion
This list provides a robust set of Fortran codes for Class L6a21, with modern Fortran codes (e.g., `rng_fortran`, `coretran`, Miller’s and Burkardt’s contributions) offering advanced features like parallelism and long periods, and Fortran 77 codes (e.g., `ZUFALL`, `RANLIB`) providing portable, proven solutions. Miller’s `luxury.f90`, `taus88.f90`, `lfsr113.f90`, and `ziggurat.f90` enhance statistical quality, while Burkardt’s `uniform`, `ranlib`, and `ziggurat` add accessibility. Continuous uniform RNGs are well-represented, discrete uniform is supported, and order statistics require additional steps. Modern codes suit current applications, while Fortran 77 codes remain viable with updates.

---
*Generated on March 02, 2025*
