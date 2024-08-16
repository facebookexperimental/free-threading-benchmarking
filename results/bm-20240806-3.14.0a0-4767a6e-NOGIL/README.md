# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [4767a6e](https://github.com/python/cpython/commit/4767a6e)
- commit date: 2024-08-06T23:01:44+02:00
- commit merge base: [5b8a6c5186be299d96dd483146dc6ea737ffdfe7](https://github.com/python/cpython/commit/5b8a6c5186be299d96dd483146dc6ea737ffdfe7)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10275023448)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e.json)

### vs. 3.12.0b1

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 2.23x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.12.0b1.md)
- [📈time plot](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.38x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.12.5%2B.md)
- [📈time plot](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.38x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.13.0b1.md)
- [📈time plot](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e-vs-3.13.0rc1%2B.svg)

