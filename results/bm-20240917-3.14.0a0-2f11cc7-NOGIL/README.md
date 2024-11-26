# Results

- fork: mpage
- version: 3.14.0a0
- config: NOGIL
- commit hash: [2f11cc7](https://github.com/mpage/cpython/commit/2f11cc7)
- commit date: 2024-09-17T21:38:12-07:00
- commit merge base: [a15a584bf3f94ea11ab9363548c8872251364000](https://github.com/mpage/cpython/commit/a15a584bf3f94ea11ab9363548c8872251364000)
- ref: gh_115999_thread_loc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11039247561)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7-vs-3.12.6.md)
- [📈time plot](bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7-vs-3.13.0rc2.md)
- [📈time plot](bm-20240917-vultr-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-2f11cc7-vs-3.13.0rc2.svg)

