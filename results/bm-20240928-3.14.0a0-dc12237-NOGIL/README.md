# Results

- fork: python/main
- version: 3.14.0a0
- config: NOGIL
- commit hash: [dc12237](https://github.com/python/cpython/commit/dc12237)
- commit date: 2024-09-28T16:12:53+00:00
- commit merge base: [c976d789a98047ae7ddec6d13c9ea7086d9fa3f9](https://github.com/python/cpython/commit/c976d789a98047ae7ddec6d13c9ea7086d9fa3f9)
- ref: main

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11085386981)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237-vs-3.12.6.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237-vs-3.13.0rc2.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 84.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237-vs-base-mem.svg)
- [📄table](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237-vs-base.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-main-3.14.0a0-dc12237-vs-base.svg)

