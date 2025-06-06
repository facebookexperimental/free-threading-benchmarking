# Results

- fork: mpage/gh_115999_tlbc_load_
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [0e50451](https://github.com/mpage/cpython/commit/0e50451)
- commit date: 2024-11-08T12:48:46-08:00
- commit merge base: [54c63a32d06cb5f07a66245c375eac7d7efb964a](https://github.com/python/cpython/commit/54c63a32d06cb5f07a66245c375eac7d7efb964a)
- ref: gh_115999_tlbc_load_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11749360862)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-3.12.6.md)
- [📈time plot](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.37x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-3.13.0rc2.md)
- [📈time plot](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-base-mem.svg)
- [📄table](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-base.md)
- [📈time plot](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.21x
- [📄table](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1%2B-0e50451-vs-default_base_vs_NOGIL.svg)

