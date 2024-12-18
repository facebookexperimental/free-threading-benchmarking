# Results

- fork: python/329165639f9ac00ba64f
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [3291656](https://github.com/python/cpython/commit/3291656)
- commit date: 2024-12-17T22:14:16-08:00
- commit merge base: [5892853fb71acd6530e1e241a9a4bcf71a61fb21](https://github.com/python/cpython/commit/5892853fb71acd6530e1e241a9a4bcf71a61fb21)
- ref: 329165639f9ac00ba64f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12387565069)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3%2B-3291656.json)

### vs. 3.12.6

- Geometric mean: 1.211x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3%2B-3291656-vs-3.12.6.md)
- [📈time plot](bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3%2B-3291656-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.236x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3%2B-3291656-vs-3.13.0rc2.md)
- [📈time plot](bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3%2B-3291656-vs-3.13.0rc2.svg)

