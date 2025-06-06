# Results

- fork: python/732670d93b9b0c0ff8ad
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [732670d](https://github.com/python/cpython/commit/732670d)
- commit date: 2025-01-23T23:31:49+00:00
- commit merge base: [bab8918f9a647c20b64f5c165b45c0926f19ca0d](https://github.com/python/cpython/commit/bab8918f9a647c20b64f5c165b45c0926f19ca0d)
- ref: 732670d93b9b0c0ff8ad

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12940660945)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d.json)

### vs. 3.12.6

- Geometric mean: 1.064x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.146x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d-vs-base-mem.svg)
- [📄table](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d-vs-base.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-732670d93b9b0c0ff8ad-3.14.0a4%2B-732670d-vs-base.svg)

