# Results

- fork: python
- version: 3.14.0a0
- config: 
- commit hash: [d7a3df9](https://github.com/python/cpython/commit/d7a3df9)
- commit date: 2024-08-15T18:42:41+00:00
- commit merge base: [b15b81ed4f58196b35e3dd13b484f4c7a73e5bb8](https://github.com/python/cpython/commit/b15b81ed4f58196b35e3dd13b484f4c7a73e5bb8)
- ref: d7a3df91505faa56c51d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10411374540)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9.json)

### vs. 3.12.0b1

- Geometric mean: 1.06x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.88x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.0b1.md)
- [📈time plot](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.05x faster (HPT: reliability of 99.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.5%2B.md)
- [📈time plot](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.05x faster (HPT: reliability of 99.91%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0b1.md)
- [📈time plot](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.01x faster (HPT: reliability of 93.30%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0rc1%2B.svg)

