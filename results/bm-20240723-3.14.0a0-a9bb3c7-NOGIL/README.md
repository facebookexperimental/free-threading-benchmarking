# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [a9bb3c7](https://github.com/python/cpython/commit/a9bb3c7)
- commit date: 2024-07-23T09:22:04+09:00
- commit merge base: [2762c6cc5e4c1c0d630568db5fbba7a3a71a507c](https://github.com/python/cpython/commit/2762c6cc5e4c1c0d630568db5fbba7a3a71a507c)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10053621433)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7.json)

### vs. 3.12.6

- Geometric mean: 1.259x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.12.6.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.287x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.13.0rc2.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.014x faster (HPT: reliability of 99.08%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-base-mem.svg)
- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-base.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.12.0b1.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.12.5%2B.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.13.0b1.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7-vs-3.13.0rc1%2B.svg)

