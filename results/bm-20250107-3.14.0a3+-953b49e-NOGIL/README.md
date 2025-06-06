# Results

- fork: python/953b49e5468d02afadda
- version: 3.14.0a3+
- config: NOGIL
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

- Geometric mean: 1.168x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.md)
- [📈time plot](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.195x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.240x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base-mem.svg)
- [📄table](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base.md)
- [📈time plot](bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base.svg)

