## L10a2: Time Domain Time Series Analysis

The GAMS Class L10a2, "Time domain time series analysis," includes methods for analyzing time series data in the time domain, with subclasses such as summary statistics (L10a2a), stationarity analysis (L10a2b), autoregressive models (L10a2c), ARMA/ARIMA models (L10a2d), state-space analysis (e.g., Kalman filtering, L10a2e), and analysis of locally stationary series (L10a2f). This document compiles Fortran codes identified from a broad web search, sourced from academic sites, software repositories, GitHub, and libraries. Fortran 77 codes are listed below more modern Fortran codes.

---

### Modern Fortran Codes (Fortran 90 and Later)

#### 1. fortsa (GitHub: zoziha/fortsa)
- **Description**: A univariate time series analysis and ARIMA modeling package in modern Fortran, based on the C package CTSA by Rafat Hussain. It supports ARMA, ARIMA, and discrete wavelet transforms (DWT), with bindings for the Fortran Package Manager (fpm). Developed by Zuo Zhihua.
- **Relevance**:  
  - **L10a2c (Autoregressive models)**: Includes autoregressive components within ARMA/ARIMA frameworks.  
  - **L10a2d (ARMA and ARIMA models)**: Implements ARIMA modeling, including Box-Jenkins methods.  
- **Source**: [github.com/zoziha/fortsa](https://github.com/zoziha/fortsa)  
- **Notes**: Actively maintained, uses modern Fortran features, and includes test cases. Requires Fortran-lang/fpm >= 0.6.0 and GNU/GCC >= 9.4.0 for compilation.

### Fortran 77 Codes

#### 2. TIMESLAB: A Time Series Analysis Laboratory
- **Description**: A Fortran 77 package by H. Joseph Newton, accompanying the book "Timeslab: A Time Series Analysis Laboratory" (1988). It provides a comprehensive set of routines for time series analysis, covering basic statistics, autoregressive models, and ARIMA modeling.
- **Relevance**:  
  - **L10a2a (Summary statistics)**: Includes routines for basic time series statistics.  
  - **L10a2c (Autoregressive models)**: Supports AR model estimation.  
  - **L10a2d (ARMA and ARIMA models)**: Implements ARMA/ARIMA methodologies, likely including Box-Jenkins approaches.  
- **Source**: [faculty.stat.tamu.edu/~hjn/timeslab.html](http://faculty.stat.tamu.edu/~hjn/timeslab.html) or mirrored on GitHub (e.g., [github.com/Beliavsky/Timeslab](https://github.com/Beliavsky/Timeslab)).  
- **Notes**: A classic, broad-purpose package requiring potential updates for modern compilers.

#### 3. TIMSAC: Time Series Analysis and Control
- **Description**: Developed by the Institute of Statistical Mathematics (Japan), TIMSAC is a Fortran-based package with versions like TIMSAC-74. It includes tools for ARIMA modeling, spectral analysis, and state-space methods, with Fortran source code embedded in R packages like `timsac`.
- **Relevance**:  
  - **L10a2c (Autoregressive models)**: Supports AR modeling.  
  - **L10a2d (ARMA and ARIMA models)**: Core focus on ARIMA, including parameter estimation and forecasting.  
  - **L10a2e (State-space analysis)**: Implements state-space models, potentially including Kalman filtering.  
- **Source**: Fortran code in the R package `timsac` (CRAN, [cran.r-project.org/package=timsac](https://cran.r-project.org/package=timsac)), with original documentation at ISM Japan.  
- **Notes**: Well-documented and widely used in econometrics; likely Fortran 77, callable from R.

#### 4. Netlib’s ESL Package (Kalman Filtering)
- **Description**: The `esl.tgz` package from Netlib provides Fortran routines for estimation and smoothing using Kalman filtering, based on Gerald J. Bierman’s "Factorization Methods for Discrete Sequential Estimation" (1977). It uses numerically stable methods like UDU^T factorization and square root information filters (SRIF).
- **Relevance**:  
  - **L10a2e (State-space analysis)**: Directly implements Kalman filtering for time series in state-space form.  
- **Source**: [netlib.org/esl/](http://netlib.org/esl/)  
- **Notes**: Focused on state-space methods, requiring familiarity with Fortran 77 and linear algebra.

#### 5. Kalman Smoothing Routine for Hodrick-Prescott Filter
- **Description**: A Fortran 77 routine by Edward Prescott for applying Kalman smoothing to the Hodrick-Prescott (HP) filter, used to decompose time series into trend and cyclical components.
- **Relevance**:  
  - **L10a2e (State-space analysis)**: Uses Kalman smoothing, a state-space technique, to implement the HP filter.  
  - **L10a2a (Summary statistics)**: Provides trend extraction, a form of summary statistic.  
- **Source**: Listed in DMOZ Fortran resources; available via academic archives or Netlib-like repositories (e.g., [netlib.org](http://netlib.org)).  
- **Notes**: Narrowly focused but directly applicable to time domain decomposition.

#### 6. SNP: Nonparametric Time Series Analysis
- **Description**: Fortran code by A. Ronald Gallant and George Tauchen for nonparametric time series analysis using Hermite polynomial expansions to approximate conditional densities. While primarily nonparametric, it overlaps with time domain methods.
- **Relevance**:  
  - **L10a2f (Analysis of a locally stationary series)**: Nonparametric approach suits locally stationary series.  
  - **L10a2a (Summary statistics)**: Density estimation includes statistical summarization.  
- **Source**: Available via the authors’ academic pages or econometrics archives (e.g., [econ.duke.edu/~get](https://econ.duke.edu/~get)).  
- **Notes**: Advanced and specialized; likely Fortran 77, requiring adaptation for broader use.

#### 7. Mann and Lees Multi-Taper Method (MTM)
- **Description**: Fortran 77 code for the Multi-Taper Method (MTM) by Mann and Lees, originally for spectral analysis but adaptable to time domain preprocessing and stationarity checks. Includes multivariate signal analysis extensions (MTM-SVD).
- **Relevance**:  
  - **L10a2b (Stationarity analysis)**: Can be used to assess stationarity via spectral properties.  
  - **L10a2a (Summary statistics)**: Provides time series characteristics as part of analysis.  
- **Source**: Available via academic repositories or Fortran resource lists (e.g., DMOZ, [szaghi.github.io](https://szaghi.github.io)).  
- **Notes**: Primarily spectral, but preprocessing aligns with time domain needs.

#### 8. GLIMCLIM: Generalized Linear Modelling of Daily Climate Sequences
- **Description**: Fortran 77 code for time series analysis of climate data, including random number generation and generalized linear modeling for time series.
- **Relevance**:  
  - **L10a2a (Summary statistics)**: Includes statistical modeling of time series.  
  - **L10a2f (Analysis of a locally stationary series)**: Focus on daily sequences suggests handling of local variations.  
- **Source**: Listed in DMOZ Fortran resources; available via academic climate research archives.  
- **Notes**: Application-specific but adaptable to general time domain analysis.

---

## Analysis and Coverage of Subclasses
- **L10a2a (Summary statistics)**: Covered by TIMESLAB, Kalman HP filter, SNP, GLIMCLIM, and indirectly by MTM for preprocessing statistics.  
- **L10a2b (Stationarity analysis)**: MTM provides indirect support via spectral checks; explicit stationarity tests are less common but implied in ARIMA packages like TIMESLAB, TIMSAC, and fortsa.  
- **L10a2c (Autoregressive models)**: TIMESLAB, TIMSAC, and fortsa explicitly implement AR models.  
- **L10a2d (ARMA and ARIMA models)**: TIMESLAB, TIMSAC, and fortsa offer strong ARIMA support, aligning with Box-Jenkins methods.  
- **L10a2e (State-space analysis)**: Netlib ESL and the Kalman HP filter directly implement Kalman filtering and state-space techniques; TIMSAC may also support this.  
- **L10a2f (Analysis of a locally stationary series)**: SNP’s nonparametric approach and GLIMCLIM’s daily sequence focus address this subclass, with partial support from others via preprocessing.  

The NAG library modules (e.g., G13FAF) in the GAMS list focus on GARCH models, specialized ARMA extensions. While none of these codes explicitly replicate GARCH, TIMSAC, TIMESLAB, and fortsa could be extended to such models with additional programming.

---

## Conclusion
This revised list includes fortsa (modern Fortran) for ARIMA and autoregressive modeling, alongside a robust set of Fortran 77 codes like TIMESLAB and TIMSAC for similar purposes, Netlib ESL and the Kalman HP filter for state-space techniques, and specialized tools like SNP and GLIMCLIM for nonparametric and locally stationary analysis. SSPACK was removed due to unavailability online. Gaps remain in explicit stationarity analysis (L10a2b), where MTM may need adaptation, and in GARCH-specific implementations. These codes provide robust tools for time domain time series analysis, accessible via GitHub, academic sites, Netlib, and R integrations. Fortran 77 codes may require compilation updates for modern use, while fortsa leverages contemporary Fortran features.

---
*Generated on March 02, 2025*
