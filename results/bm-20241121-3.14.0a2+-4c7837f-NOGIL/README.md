# Results

- fork: mpage
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [4c7837f](https://github.com/mpage/cpython/commit/4c7837f)
- commit date: 2024-11-21T16:51:33-08:00
- commit merge base: [32428cf9ea03bce6d64c7acd28e0b7d92774eb53](https://github.com/mpage/cpython/commit/32428cf9ea03bce6d64c7acd28e0b7d92774eb53)
- ref: gh_115999_tlbc_call

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11978595387)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f.json)

### vs. 3.12.6

- Geometric mean: 1.49x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.12.6.md)
- [📈time plot](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.03x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-base-mem.svg)
- [📄table](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-base.md)
- [📈time plot](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.56x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- new benchmarks: async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-default_base_vs_NOGIL.svg)

