# Results

- fork: mpage/gh_115999_tlbc_integ
- version: 3.14.0a0
- config: NOGIL
- commit hash: [0a68813](https://github.com/mpage/cpython/commit/0a68813)
- commit date: 2024-10-31T10:15:40-07:00
- commit merge base: [f1d33dbddd3496b062e1fbe024fb6d7b023a35f5](https://github.com/python/cpython/commit/f1d33dbddd3496b062e1fbe024fb6d7b023a35f5)
- ref: gh_115999_tlbc_integ

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11708555186)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.12.6.md)
- [📈time plot](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.13.0rc2.md)
- [📈time plot](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base-mem.svg)
- [📄table](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base.md)
- [📈time plot](bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11616736837)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.12.6.md)
- [📈time plot](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.13.0rc2.md)
- [📈time plot](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base-mem.svg)
- [📄table](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base.md)
- [📈time plot](bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base.svg)

