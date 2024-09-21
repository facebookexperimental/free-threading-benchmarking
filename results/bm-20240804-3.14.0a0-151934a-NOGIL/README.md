# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [151934a](https://github.com/python/cpython/commit/151934a)
- commit date: 2024-08-04T00:55:47+03:00
- commit merge base: [95f5c89b545beaafad73f05a695742da3e90bc41](https://github.com/python/cpython/commit/95f5c89b545beaafad73f05a695742da3e90bc41)
- ref: 151934a324789c58cca9

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10231897633)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a.json)

### vs. 3.12.6

- Geometric mean: 1.31x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.12.6.md)
- [📈time plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.36x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.13.0rc2.md)
- [📈time plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.42x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-base-mem.svg)
- [📄table](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-base.md)
- [📈time plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.12.0b1.md)
- [📈time plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.12.5%2B.md)
- [📈time plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.13.0b1.md)
- [📈time plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240804-linux-x86_64-python-151934a324789c58cca9-3.14.0a0-151934a-vs-3.13.0rc1%2B.svg)

