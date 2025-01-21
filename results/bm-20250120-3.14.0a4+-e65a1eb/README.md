# Results

- fork: python/e65a1eb93ae35f9fbab1
- version: 3.14.0a4+
- config: 
- commit hash: [e65a1eb](https://github.com/python/cpython/commit/e65a1eb)
- commit date: 2025-01-20T23:53:33+00:00
- commit merge base: [e54ac3b69edacf4149988150591226df1397d127](https://github.com/python/cpython/commit/e54ac3b69edacf4149988150591226df1397d127)
- ref: e65a1eb93ae35f9fbab1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12877706717)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 98.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.md)
- [📈time plot](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 94.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12877706717)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.svg)

