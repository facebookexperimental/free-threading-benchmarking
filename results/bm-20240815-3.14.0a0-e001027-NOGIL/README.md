# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [e001027](https://github.com/python/cpython/commit/e001027)
- commit date: 2024-08-15T16:09:11+00:00
- commit merge base: [1dad23edbc9db3a13268c1000c8dd428edba29f8](https://github.com/python/cpython/commit/1dad23edbc9db3a13268c1000c8dd428edba29f8)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10407802632)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027.json)

### vs. 3.12.0b1

- Geometric mean: 1.39x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 2.24x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.0b1.md)
- [📈time plot](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.41x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.5%2B.md)
- [📈time plot](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.40x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0b1.md)
- [📈time plot](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.45x slower (HPT: reliability of 100.00%, 1.33x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0rc1%2B.svg)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 82.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-base-mem.svg)
- [📄table](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-base.md)
- [📈time plot](bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-base.svg)

