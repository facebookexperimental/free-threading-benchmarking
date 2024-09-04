# Results

- fork: mpage
- version: 3.14.0a0
- config: NOGIL
- commit hash: [d8a840b](https://github.com/mpage/cpython/commit/d8a840b)
- commit date: 2024-09-03T20:49:47-07:00
- commit merge base: [7e38e6745d2f9ee235d934ab7f3c6b3085be2b70](https://github.com/mpage/cpython/commit/7e38e6745d2f9ee235d934ab7f3c6b3085be2b70)
- ref: gh_115999_thread_loc

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10694784445)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b.json)

### vs. 3.12.0b1

- Geometric mean: 1.36x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 2.29x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.0b1.md)
- [📈time plot](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.38x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.5%2B.md)
- [📈time plot](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0b1.md)
- [📈time plot](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.42x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0rc1%2B.svg)

