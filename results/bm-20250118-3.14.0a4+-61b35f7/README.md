# Results

- fork: python/61b35f74aa4a6ac60663
- version: 3.14.0a4+
- config: 
- commit hash: [61b35f7](https://github.com/python/cpython/commit/61b35f7)
- commit date: 2025-01-18T16:53:06-05:00
- commit merge base: [e8092e5cdcd6707ac0b16d8fb37fa080a88bcc97](https://github.com/python/cpython/commit/e8092e5cdcd6707ac0b16d8fb37fa080a88bcc97)
- ref: 61b35f74aa4a6ac60663

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12848571184)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250118-linux-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 99.99%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250118-linux-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.12.6.md)
- [📈time plot](bm-20250118-linux-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250118-linux-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250118-linux-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12847968539)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.12.6.md)
- [📈time plot](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4%2B-61b35f7-vs-3.13.0rc2.svg)

