# Results

- fork: colesbury
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [5583ac0](https://github.com/colesbury/cpython/commit/5583ac0)
- commit date: 2024-11-19T16:47:54+00:00
- commit merge base: [29cbcbd73bbfd8c953c0b213fb33682c289934ff](https://github.com/colesbury/cpython/commit/29cbcbd73bbfd8c953c0b213fb33682c289934ff)
- ref: gh_127022_cheaper_st

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11917792707)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.37x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0-vs-3.12.6.md)
- [📈time plot](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0-vs-3.13.0rc2.md)
- [📈time plot](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0-vs-base-mem.svg)
- [📄table](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0-vs-base.md)
- [📈time plot](bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-5583ac0-vs-base.svg)

