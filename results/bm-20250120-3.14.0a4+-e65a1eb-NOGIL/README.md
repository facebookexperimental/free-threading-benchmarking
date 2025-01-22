# Results

- fork: python/e65a1eb93ae35f9fbab1
- version: 3.14.0a4+
- config: NOGIL
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

- Geometric mean: 1.077x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.md)
- [📈time plot](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.128x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-base-mem.svg)
- [📄table](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-base.md)
- [📈time plot](bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12895635620)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb.json)

### vs. 3.12.6

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-base-mem.svg)
- [📄table](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-base.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4%2B-e65a1eb-vs-base.svg)

