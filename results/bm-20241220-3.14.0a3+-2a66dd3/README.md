# Results

- fork: python/2a66dd33dfc0b845042d
- version: 3.14.0a3+
- config: 
- commit hash: [2a66dd3](https://github.com/python/cpython/commit/2a66dd3)
- commit date: 2024-12-20T11:40:58-08:00
- commit merge base: [3879ca0100942ae15a09ac22889cbe3e46d424eb](https://github.com/python/cpython/commit/3879ca0100942ae15a09ac22889cbe3e46d424eb)
- ref: 2a66dd33dfc0b845042d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12447977829)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3-pystats.json)
- [pystats table](bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3-pystats.md)
- [raw results](bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3-vs-3.12.6.md)
- [📈time plot](bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3-vs-3.13.0rc2.md)
- [📈time plot](bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3-vs-3.13.0rc2.svg)

