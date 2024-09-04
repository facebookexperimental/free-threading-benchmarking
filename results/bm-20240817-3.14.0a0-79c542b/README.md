# Results

- fork: python
- version: 3.14.0a0
- config: 
- commit hash: [79c542b](https://github.com/python/cpython/commit/79c542b)
- commit date: 2024-08-17T20:58:06+00:00
- commit merge base: [d061ffea7b408861d0a9d311e92c363da284971d](https://github.com/python/cpython/commit/d061ffea7b408861d0a9d311e92c363da284971d)
- ref: 79c542b5cc774ba758ac

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10436205116)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b.json)

### vs. 3.12.0b1

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.88x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.12.0b1.md)
- [📈time plot](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.05x faster (HPT: reliability of 99.92%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.12.5%2B.md)
- [📈time plot](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.06x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.13.0b1.md)
- [📈time plot](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.02x faster (HPT: reliability of 97.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240817-linux-x86_64-python-79c542b5cc774ba758ac-3.14.0a0-79c542b-vs-3.13.0rc1%2B.svg)

