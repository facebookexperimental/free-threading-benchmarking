# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [c976d78](https://github.com/python/cpython/commit/c976d78)
- commit date: 2024-09-28T05:50:09-07:00
- commit merge base: [fae5058ec13aa3b4f1acc549fadfbbbc2628f1e9](https://github.com/python/cpython/commit/fae5058ec13aa3b4f1acc549fadfbbbc2628f1e9)
- ref: c976d789a98047ae7dde

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11085386981)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78.json)

### vs. 3.12.6

- Geometric mean: 1.46x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78-vs-3.12.6.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.50x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78-vs-3.13.0rc2.md)
- [📈time plot](bm-20240928-vultr-x86_64-python-c976d789a98047ae7dde-3.14.0a0-c976d78-vs-3.13.0rc2.svg)

