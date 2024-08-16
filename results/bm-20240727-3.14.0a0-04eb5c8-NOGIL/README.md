# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [04eb5c8](https://github.com/python/cpython/commit/04eb5c8)
- commit date: 2024-07-27T21:33:38+03:00
- commit merge base: [ae192262ad1cffb6ece9d16e67804386c382be0c](https://github.com/python/cpython/commit/ae192262ad1cffb6ece9d16e67804386c382be0c)
- ref: 04eb5c8db1e24cabd0cb

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10127363223)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json)

### vs. 3.12.0b1

- Geometric mean: 1.33x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 2.28x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.12.0b1.md)
- [📈time plot](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.34x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.12.5%2B.md)
- [📈time plot](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.34x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.13.0b1.md)
- [📈time plot](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.39x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-3.13.0rc1%2B.svg)

### vs. base

- Geometric mean: 1.44x slower (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-base-mem.svg)
- [📄table](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-base.md)
- [📈time plot](bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8-vs-base.svg)

