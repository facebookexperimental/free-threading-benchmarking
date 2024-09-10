# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [11fa119](https://github.com/python/cpython/commit/11fa119)
- commit date: 2024-09-07T21:46:56+03:00
- commit merge base: [93050e46144c5864fbf2b39eac798387d5758a2d](https://github.com/python/cpython/commit/93050e46144c5864fbf2b39eac798387d5758a2d)
- ref: 11fa11987990eb7ed75b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10755442682)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119.json)

### vs. 3.12.0b1

- Geometric mean: 1.28x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 2.24x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.12.0b1.md)
- [📈time plot](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.30x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.12.5%2B.md)
- [📈time plot](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.29x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.13.0b1.md)
- [📈time plot](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.34x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-3.13.0rc1%2B.svg)

### vs. base

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-base-mem.svg)
- [📄table](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-base.md)
- [📈time plot](bm-20240907-linux-x86_64-python-11fa11987990eb7ed75b-3.14.0a0-11fa119-vs-base.svg)

