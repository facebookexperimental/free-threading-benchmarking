# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [1dad23e](https://github.com/python/cpython/commit/1dad23e)
- commit date: 2024-08-15T09:01:01-04:00
- commit merge base: [3203a7412977b8da3aba2770308136a37f48c927](https://github.com/python/cpython/commit/3203a7412977b8da3aba2770308136a37f48c927)
- ref: 1dad23edbc9db3a13268

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10407802632)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e.json)

### vs. 3.12.0b1

- Geometric mean: 1.38x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 2.23x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.0b1.md)
- [📈time plot](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.40x slower (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.5%2B.md)
- [📈time plot](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.39x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0b1.md)
- [📈time plot](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.44x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0rc1%2B.svg)

