# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [1d607fe](https://github.com/python/cpython/commit/1d607fe)
- commit date: 2024-07-25T14:27:26-06:00
- commit merge base: [5f6001130f8ada871193377954cfcfee01ef93b6](https://github.com/python/cpython/commit/5f6001130f8ada871193377954cfcfee01ef93b6)
- ref: 1d607fe759ef22177b50

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10102071203)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe.json)

### vs. 3.12.0b1

- Geometric mean: 1.34x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 2.25x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.12.0b1.md)
- [📈time plot](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.12.5%2B.md)
- [📈time plot](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.13.0b1.md)
- [📈time plot](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.40x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe-vs-3.13.0rc1%2B.svg)

