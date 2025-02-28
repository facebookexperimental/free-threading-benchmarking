# Results

- fork: mpage/all_blocks
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [9ad230b](https://github.com/mpage/cpython/commit/9ad230b)
- commit date: 2025-02-27T16:54:13-08:00
- commit merge base: [9211b3dabeacb92713ac3f5f0fa43bc7cf69afd8](https://github.com/python/cpython/commit/9211b3dabeacb92713ac3f5f0fa43bc7cf69afd8)
- ref: all_blocks

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13578969654)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 99.93%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.12.6.md)
- [📈time plot](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.028x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-base-mem.svg)
- [📄table](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-base.md)
- [📈time plot](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.126x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-default_base_vs_NOGIL.svg)

