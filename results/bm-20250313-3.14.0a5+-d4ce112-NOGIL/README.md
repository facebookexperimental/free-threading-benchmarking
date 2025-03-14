# Results

- fork: nascheme/gh_127266_type_slots
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [d4ce112](https://github.com/nascheme/cpython/commit/d4ce112)
- commit date: 2025-03-13T16:27:12-07:00
- commit merge base: [db1e5827c45ad737bf83f358a2851e943626d29b](https://github.com/python/cpython/commit/db1e5827c45ad737bf83f358a2851e943626d29b)
- ref: gh_127266_type_slots

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13847246221)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.12.6.md)
- [📈time plot](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.13.0rc2.md)
- [📈time plot](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-base-mem.svg)
- [📄table](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-base.md)
- [📈time plot](bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-base.svg)

