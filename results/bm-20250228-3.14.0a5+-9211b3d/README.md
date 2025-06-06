# Results

- fork: python/9211b3dabeacb92713ac
- version: 3.14.0a5+
- config: 
- commit hash: [9211b3d](https://github.com/python/cpython/commit/9211b3d)
- commit date: 2025-02-28T07:33:10+08:00
- commit merge base: [6140b0896e95ca96aa15472e14d0502966391485](https://github.com/python/cpython/commit/6140b0896e95ca96aa15472e14d0502966391485)
- ref: 9211b3dabeacb92713ac

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13578567493)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.svg)

