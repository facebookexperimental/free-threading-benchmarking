# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [3bd942f](https://github.com/python/cpython/commit/3bd942f)
- commit date: 2024-09-11T21:25:23+03:00
- commit merge base: [eb169f40276a8611827770f02c4b82827c98e00f](https://github.com/python/cpython/commit/eb169f40276a8611827770f02c4b82827c98e00f)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10819936093)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.12.6.md)
- [📈time plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.13.0rc2.md)
- [📈time plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 85.70%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-base-mem.svg)
- [📄table](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-base.md)
- [📈time plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.12.0b1.md)
- [📈time plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.12.5%2B.md)
- [📈time plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.13.0b1.md)
- [📈time plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f-vs-3.13.0rc1%2B.svg)

