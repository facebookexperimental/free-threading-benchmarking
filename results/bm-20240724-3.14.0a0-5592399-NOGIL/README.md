# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [5592399](https://github.com/python/cpython/commit/5592399)
- commit date: 2024-07-24T10:58:28-07:00
- commit merge base: [9ac606080a0074cdf7589d9b7c9413a73e0ddf37](https://github.com/python/cpython/commit/9ac606080a0074cdf7589d9b7c9413a73e0ddf37)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10084468262)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399.json)

### vs. 3.12.6

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.12.6.md)
- [📈time plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.42x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.13.0rc2.md)
- [📈time plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.01x slower (HPT: reliability of 99.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-base-mem.svg)
- [📄table](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-base.md)
- [📈time plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.12.0b1.md)
- [📈time plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.12.5%2B.md)
- [📈time plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.13.0b1.md)
- [📈time plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399-vs-3.13.0rc1%2B.svg)

