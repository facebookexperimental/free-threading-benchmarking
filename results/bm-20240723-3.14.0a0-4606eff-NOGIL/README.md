# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [4606eff](https://github.com/python/cpython/commit/4606eff)
- commit date: 2024-07-23T20:45:21+03:00
- commit merge base: [a15feded71dd47202db169613effdafc468a8cf3](https://github.com/python/cpython/commit/a15feded71dd47202db169613effdafc468a8cf3)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10064564259)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff.json)

### vs. 3.12.0b1

- Geometric mean: 1.34x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 2.25x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.12.0b1.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.12.5%2B.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.13.0b1.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.40x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-3.13.0rc1%2B.svg)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 98.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-base-mem.svg)
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-base.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff-vs-base.svg)

