# Results

- fork: python
- version: 3.14.0a0
- config: 
- commit hash: [16cd6cc](https://github.com/python/cpython/commit/16cd6cc)
- commit date: 2024-10-05T09:56:44+02:00
- commit merge base: [a5fc50994a3fae46d0c3d496c4e1d5e00548a1b8](https://github.com/python/cpython/commit/a5fc50994a3fae46d0c3d496c4e1d5e00548a1b8)
- ref: 16cd6cc86b3ba20074ae

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11197338023)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241005-vultr-x86_64-python-16cd6cc86b3ba20074ae-3.14.0a0-16cd6cc.json)

### vs. 3.12.6

- Geometric mean: 1.06x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241005-vultr-x86_64-python-16cd6cc86b3ba20074ae-3.14.0a0-16cd6cc-vs-3.12.6.md)
- [📈time plot](bm-20241005-vultr-x86_64-python-16cd6cc86b3ba20074ae-3.14.0a0-16cd6cc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.03x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241005-vultr-x86_64-python-16cd6cc86b3ba20074ae-3.14.0a0-16cd6cc-vs-3.13.0rc2.md)
- [📈time plot](bm-20241005-vultr-x86_64-python-16cd6cc86b3ba20074ae-3.14.0a0-16cd6cc-vs-3.13.0rc2.svg)

