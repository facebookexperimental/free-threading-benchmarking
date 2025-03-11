# Results

- fork: python/4192ce17ba643e5b0bc9
- version: 3.14.0a5+
- config: 
- commit hash: [4192ce1](https://github.com/python/cpython/commit/4192ce1)
- commit date: 2025-03-10T23:10:53+00:00
- commit merge base: [7c98b0674daa3e4eb3e8f35afb61a0dba61d1780](https://github.com/python/cpython/commit/7c98b0674daa3e4eb3e8f35afb61a0dba61d1780)
- ref: 4192ce17ba643e5b0bc9

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13777548383)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250310-linux-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250310-linux-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.12.6.md)
- [📈time plot](bm-20250310-linux-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250310-linux-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250310-linux-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13777548383)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250310-vultr-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1.json)

### vs. 3.12.6

- Geometric mean: 1.061x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250310-vultr-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.12.6.md)
- [📈time plot](bm-20250310-vultr-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 64.01%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250310-vultr-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250310-vultr-x86_64-python-4192ce17ba643e5b0bc9-3.14.0a5%2B-4192ce1-vs-3.13.0rc2.svg)

