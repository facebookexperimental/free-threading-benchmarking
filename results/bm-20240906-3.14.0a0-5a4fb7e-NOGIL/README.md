# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [5a4fb7e](https://github.com/python/cpython/commit/5a4fb7e)
- commit date: 2024-09-06T20:12:12+03:00
- commit merge base: [56e4a417ce170e5c538ce9aafccf3333e7bf7492](https://github.com/python/cpython/commit/56e4a417ce170e5c538ce9aafccf3333e7bf7492)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10740958612)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e.json)

### vs. 3.12.0b1

- Geometric mean: 1.40x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 2.26x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.12.0b1.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.41x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.12.5%2B.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.41x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.13.0b1.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.46x slower (HPT: reliability of 100.00%, 1.33x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e-vs-3.13.0rc1%2B.svg)

