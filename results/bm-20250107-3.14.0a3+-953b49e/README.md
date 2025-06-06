# Results

- fork: python/953b49e5468d02afadda
- version: 3.14.0a3+
- config: 
- commit hash: [953b49e](https://github.com/python/cpython/commit/953b49e)
- commit date: 2025-01-07T00:38:45+01:00
- commit merge base: [7363476b6405e3d288a61282aa7bc6aca9c2114d](https://github.com/python/cpython/commit/7363476b6405e3d288a61282aa7bc6aca9c2114d)
- ref: 953b49e5468d02afadda

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12642710446)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.md)
- [📈time plot](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.svg)

