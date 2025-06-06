# Results

- fork: mpage/gh_115999_tlbc_load_
- version: 3.14.0a0
- config: NOGIL
- commit hash: [2613a14](https://github.com/mpage/cpython/commit/2613a14)
- commit date: 2024-09-25T11:33:28-07:00
- commit merge base: [a15a584bf3f94ea11ab9363548c8872251364000](https://github.com/python/cpython/commit/a15a584bf3f94ea11ab9363548c8872251364000)
- ref: gh_115999_tlbc_load_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11042230894)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14-vs-3.12.6.md)
- [📈time plot](bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14-vs-3.13.0rc2.md)
- [📈time plot](bm-20240925-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-2613a14-vs-3.13.0rc2.svg)

