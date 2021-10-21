# Modules Development

Modules are all written to work with the [`develop`](https://github.com/moja-global/FLINT/tree/develop) branch of the **FLINT** and any actively maintained branches will work with the most recent version (and are broken with old enough builds of the FLINT). The FLINT Application Programming Interface (API) has evolved over time, so some modules might be out of date. None of these modules require a custom fork of FLINT.

## Background

It is useful to think about what a module manifest might look like. **Manifests** are meta-data used by the package managers to describe the compatibility (FLINT versions that are used), dependencies (necessary inputs) and the configuration requirements (for example whether the module uses daily, monthly or annual time steps).

This project describes the core contribution of each module.

## Index

1.  [Prerequisites](Prerequisites.md)
2.  [Empirical forest growth module](empirical-forest-growth-module.md)
3.  [Hybrid forest growth module](hybrid-forest-growth-module.md)
4.  [WOFOST crop growth module](wofost-crop-growth-module.md)
5.  [Turnover module](turnover-module.md)
6.  [Decomposition module](decomposition-module.md)
7.  [RothC soil carbon module](rothc-soil-carbon-module.md)
8.  [Chapman Richards module](chapman-richards-module.md)
9.  [GCBM module](gcbm-module.md)
10. [Commonly asked questions / FAQ](FAQ.md)

