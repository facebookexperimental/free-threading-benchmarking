# Results

- fork: mpage/gh_115999_tlbc_call
- version: 3.14.0a2+
- config: 
- commit hash: [8ebd73d](https://github.com/mpage/cpython/commit/8ebd73d)
- commit date: 2024-11-20T22:27:45-08:00
- commit merge base: [32428cf9ea03bce6d64c7acd28e0b7d92774eb53](https://github.com/python/cpython/commit/32428cf9ea03bce6d64c7acd28e0b7d92774eb53)
- ref: gh_115999_tlbc_call

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11959013491)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 90.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d-vs-3.12.6.md)
- [📈time plot](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 90.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d-vs-3.13.0rc2.md)
- [📈time plot](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 59.05%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d-vs-base-mem.svg)
- [📄table](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d-vs-base.md)
- [📈time plot](bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-8ebd73d-vs-base.svg)

