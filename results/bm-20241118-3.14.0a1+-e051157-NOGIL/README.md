# Results

- fork: mpage
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [e051157](https://github.com/mpage/cpython/commit/e051157)
- commit date: 2024-11-18T17:33:09-08:00
- commit merge base: [9d6366b60d01305fc5e45100e0cd13e358aa397d](https://github.com/mpage/cpython/commit/9d6366b60d01305fc5e45100e0cd13e358aa397d)
- ref: gh_115999_tlbc_call_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11976895253)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157.json)

### vs. 3.12.6

- Geometric mean: 1.324x slower (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-3.12.6.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.347x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-3.13.0rc2.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 98.27%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-base-mem.svg)
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-base.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.373x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- new benchmarks: async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1%2B-e051157-vs-default_base_vs_NOGIL.svg)

