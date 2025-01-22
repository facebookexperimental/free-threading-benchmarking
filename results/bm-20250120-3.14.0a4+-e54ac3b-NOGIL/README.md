# Results

- fork: python/e54ac3b69edacf414998
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [e54ac3b](https://github.com/python/cpython/commit/e54ac3b)
- commit date: 2025-01-20T23:53:08+00:00
- commit merge base: [f3980af38b7cc4a4dfb5476324b841a519d56c9a](https://github.com/python/cpython/commit/f3980af38b7cc4a4dfb5476324b841a519d56c9a)
- ref: e54ac3b69edacf414998

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12895635620)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4%2B-e54ac3b.json)

### vs. 3.12.6

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4%2B-e54ac3b-vs-3.12.6.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4%2B-e54ac3b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.113x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4%2B-e54ac3b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-e54ac3b69edacf414998-3.14.0a4%2B-e54ac3b-vs-3.13.0rc2.svg)

