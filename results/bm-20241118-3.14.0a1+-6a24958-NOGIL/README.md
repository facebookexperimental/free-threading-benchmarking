# Results

- fork: mpage/gh_115999_tlbc_call
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [6a24958](https://github.com/mpage/cpython/commit/6a24958)
- commit date: 2024-11-18T22:09:20-08:00
- commit merge base: [9d6366b60d01305fc5e45100e0cd13e358aa397d](https://github.com/python/cpython/commit/9d6366b60d01305fc5e45100e0cd13e358aa397d)
- ref: gh_115999_tlbc_call

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11907366581)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-3.12.6.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.37x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-3.13.0rc2.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-base-mem.svg)
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-base.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.36x slower at 99th %ile)
- Memory usage: 1.21x
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1%2B-6a24958-vs-default_base_vs_NOGIL.svg)

