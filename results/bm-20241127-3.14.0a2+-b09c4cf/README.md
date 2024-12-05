# Results

- fork: nascheme/gh_127271_cell_get_s
- version: 3.14.0a2+
- config: 
- commit hash: [b09c4cf](https://github.com/nascheme/cpython/commit/b09c4cf)
- commit date: 2024-11-27T14:27:10-08:00
- commit merge base: [6da9d252ac39d53342455a17bfec7b1087fba697](https://github.com/python/cpython/commit/6da9d252ac39d53342455a17bfec7b1087fba697)
- ref: gh_127271_cell_get_s

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12129988631)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf.json)

### vs. 3.12.6

- Geometric mean: 1.036x faster (HPT: reliability of 99.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf-vs-3.12.6.md)
- [📈time plot](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 94.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf-vs-3.13.0rc2.md)
- [📈time plot](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 82.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf-vs-base-mem.svg)
- [📄table](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf-vs-base.md)
- [📈time plot](bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2%2B-b09c4cf-vs-base.svg)

