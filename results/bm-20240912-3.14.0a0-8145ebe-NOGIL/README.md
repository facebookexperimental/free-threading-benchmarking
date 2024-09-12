# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [8145ebe](https://github.com/python/cpython/commit/8145ebe)
- commit date: 2024-09-12T19:58:32+01:00
- commit merge base: [b2afe2aae487ebf89897e22c01d9095944fd334f](https://github.com/python/cpython/commit/b2afe2aae487ebf89897e22c01d9095944fd334f)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10837026313)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe.json)

### vs. 3.12.0b1

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 2.24x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.12.0b1.md)
- [📈time plot](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.12.5%2B.md)
- [📈time plot](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.36x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.13.0b1.md)
- [📈time plot](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.41x slower (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-3.13.0rc1%2B.svg)

### vs. base

- Geometric mean: 1.01x faster (HPT: reliability of 97.21%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-base-mem.svg)
- [📄table](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-base.md)
- [📈time plot](bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe-vs-base.svg)

