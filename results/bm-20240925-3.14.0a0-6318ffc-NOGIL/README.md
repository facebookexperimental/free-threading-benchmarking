# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [6318ffc](https://github.com/python/cpython/commit/6318ffc)
- commit date: 2024-09-25T20:06:54+01:00
- commit merge base: [198756b0f653e9f487076df2c6f943e374def6cb](https://github.com/python/cpython/commit/198756b0f653e9f487076df2c6f943e374def6cb)
- ref: 6318ffcba21f8fc155f5

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11042226213)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240925-linux-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240925-linux-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.12.6.md)
- [📈time plot](bm-20240925-linux-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240925-linux-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.13.0rc2.md)
- [📈time plot](bm-20240925-linux-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11042224705)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240925-vultr-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240925-vultr-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.12.6.md)
- [📈time plot](bm-20240925-vultr-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.33x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240925-vultr-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.13.0rc2.md)
- [📈time plot](bm-20240925-vultr-x86_64-python-6318ffcba21f8fc155f5-3.14.0a0-6318ffc-vs-3.13.0rc2.svg)

