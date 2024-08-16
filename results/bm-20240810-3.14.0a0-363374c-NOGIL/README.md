# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [363374c](https://github.com/python/cpython/commit/363374c)
- commit date: 2024-08-10T21:21:17+00:00
- commit merge base: [0959142e4defcf7a9fcbbb228d2e2b97a074f7ea](https://github.com/python/cpython/commit/0959142e4defcf7a9fcbbb228d2e2b97a074f7ea)
- ref: 363374cf69a7e2292fe3

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10335430249)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c.json)

### vs. 3.12.0b1

- Geometric mean: 1.31x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 2.26x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.12.0b1.md)
- [📈time plot](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.32x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.12.5%2B.md)
- [📈time plot](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.31x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.13.0b1.md)
- [📈time plot](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.36x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-3.13.0rc1%2B.svg)

### vs. base

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.15x
- [🧠memory plot](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-base-mem.svg)
- [📄table](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-base.md)
- [📈time plot](bm-20240810-linux-x86_64-python-363374cf69a7e2292fe3-3.14.0a0-363374c-vs-base.svg)

