# Results

- fork: mpage/gh_115999_tlbc_call
- version: 3.14.0a0
- config: NOGIL
- commit hash: [819f30a](https://github.com/mpage/cpython/commit/819f30a)
- commit date: 2024-10-18T14:31:20-07:00
- commit merge base: [f1d33dbddd3496b062e1fbe024fb6d7b023a35f5](https://github.com/python/cpython/commit/f1d33dbddd3496b062e1fbe024fb6d7b023a35f5)
- ref: gh_115999_tlbc_call

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11415078774)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.36x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a-vs-3.12.6.md)
- [📈time plot](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a-vs-base-mem.svg)
- [📄table](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a-vs-base.md)
- [📈time plot](bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a-vs-base.svg)

