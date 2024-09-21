# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [e006c73](https://github.com/python/cpython/commit/e006c73)
- commit date: 2024-08-08T00:47:15+02:00
- commit merge base: [540fcc62f5da982b79504221cac01bfab8b73ba1](https://github.com/python/cpython/commit/540fcc62f5da982b79504221cac01bfab8b73ba1)
- ref: e006c7371d8e57db2625

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10306123426)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73.json)

### vs. 3.12.6

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.12.6.md)
- [📈time plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.13.0rc2.md)
- [📈time plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.45x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base-mem.svg)
- [📄table](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.md)
- [📈time plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.12.0b1.md)
- [📈time plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.12.5%2B.md)
- [📈time plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.13.0b1.md)
- [📈time plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-3.13.0rc1%2B.svg)

