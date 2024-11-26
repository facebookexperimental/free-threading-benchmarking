# Results

- fork: python
- version: 3.14.0a0
- config: 
- commit hash: [04c837d](https://github.com/python/cpython/commit/04c837d)
- commit date: 2024-09-28T15:15:43-07:00
- commit merge base: [69a4063ca516360b5eb96f5432ad9f9dfc32a72e](https://github.com/python/cpython/commit/69a4063ca516360b5eb96f5432ad9f9dfc32a72e)
- ref: 04c837d9d8a474777ef9

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11088043721)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.md)
- [📈time plot](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 99.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.md)
- [📈time plot](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11088043721)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.svg)

