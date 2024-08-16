# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [901d949](https://github.com/python/cpython/commit/901d949)
- commit date: 2024-08-13T19:39:12+03:00
- commit merge base: [906b796af8388174cf493e23f29720eaed9fdf03](https://github.com/python/cpython/commit/906b796af8388174cf493e23f29720eaed9fdf03)
- ref: 901d94992eddd84ded2e

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10376477734)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949.json)

### vs. 3.12.0b1

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 2.25x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.0b1.md)
- [📈time plot](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.5%2B.md)
- [📈time plot](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.36x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0b1.md)
- [📈time plot](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.41x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0rc1%2B.svg)

