# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [5f68511](https://github.com/python/cpython/commit/5f68511)
- commit date: 2024-08-13T17:09:21+00:00
- commit merge base: [901d94992eddd84ded2edc55235cbf22503c4de4](https://github.com/python/cpython/commit/901d94992eddd84ded2edc55235cbf22503c4de4)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10376477734)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511.json)

### vs. 3.12.6

- Geometric mean: 1.40x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.6.md)
- [📈time plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.46x slower (HPT: reliability of 100.00%, 1.33x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0rc2.md)
- [📈time plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.02x slower (HPT: reliability of 99.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-base-mem.svg)
- [📄table](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-base.md)
- [📈time plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.0b1.md)
- [📈time plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.5%2B.md)
- [📈time plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0b1.md)
- [📈time plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0rc1%2B.svg)

