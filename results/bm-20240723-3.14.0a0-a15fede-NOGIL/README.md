# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [a15fede](https://github.com/python/cpython/commit/a15fede)
- commit date: 2024-07-23T17:06:03+00:00
- commit merge base: [e6b25e9a09dbe09839b36f97b9174a30b1db2dbf](https://github.com/python/cpython/commit/e6b25e9a09dbe09839b36f97b9174a30b1db2dbf)
- ref: a15feded71dd47202db1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10064564259)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede.json)

### vs. 3.12.0b1

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 2.27x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.12.0b1.md)
- [📈time plot](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.12.5%2B.md)
- [📈time plot](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.36x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.13.0b1.md)
- [📈time plot](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.41x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede-vs-3.13.0rc1%2B.svg)

