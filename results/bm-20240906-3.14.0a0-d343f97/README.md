# Results

- fork: python
- version: 3.14.0a0
- config: 
- commit hash: [d343f97](https://github.com/python/cpython/commit/d343f97)
- commit date: 2024-09-06T16:08:17+02:00
- commit merge base: [ef4b69d2becf49daaea21eb04effee81328a0393](https://github.com/python/cpython/commit/ef4b69d2becf49daaea21eb04effee81328a0393)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10740950782)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97.json)

### vs. 3.12.6

- Geometric mean: 1.01x faster (HPT: reliability of 62.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.12.6.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.03x slower (HPT: reliability of 99.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.13.0rc2.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.00x faster (HPT: reliability of 79.86%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-base-mem.svg)
- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-base.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.12.0b1.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.12.5%2B.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.13.0b1.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97-vs-3.13.0rc1%2B.svg)

