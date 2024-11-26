# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
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

- Geometric mean: 1.263x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.md)
- [📈time plot](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.291x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.md)
- [📈time plot](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.307x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.15x
- [🧠memory plot](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-base-mem.svg)
- [📄table](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-base.md)
- [📈time plot](bm-20240928-linux-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11088043721)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d.json)

### vs. 3.12.6

- Geometric mean: 1.303x slower (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.327x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.357x slower (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.16x
- [🧠memory plot](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-base-mem.svg)
- [📄table](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-base.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-04c837d9d8a474777ef9-3.14.0a0-04c837d-vs-base.svg)

