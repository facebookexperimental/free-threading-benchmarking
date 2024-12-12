# Results

- fork: python/bc262de06b10a2d119c2
- version: 3.14.0a2+
- config: 
- commit hash: [bc262de](https://github.com/python/cpython/commit/bc262de)
- commit date: 2024-12-11T17:37:38+00:00
- commit merge base: [dd9da738ad1d420fabafaded3fe63912b2b17cfb](https://github.com/python/cpython/commit/dd9da738ad1d420fabafaded3fe63912b2b17cfb)
- ref: bc262de06b10a2d119c2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12283921585)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2%2B-bc262de.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2%2B-bc262de-vs-3.12.6.md)
- [📈time plot](bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2%2B-bc262de-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2%2B-bc262de-vs-3.13.0rc2.md)
- [📈time plot](bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2%2B-bc262de-vs-3.13.0rc2.svg)

