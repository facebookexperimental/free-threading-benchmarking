# Results

- fork: python/a385add4015c431534e2
- version: 3.14.0a5+
- config: 
- commit hash: [a385add](https://github.com/python/cpython/commit/a385add)
- commit date: 2025-03-06T23:41:03+00:00
- commit merge base: [a025f27d94afe732be2e9e6f05b9007d04f983a8](https://github.com/python/cpython/commit/a025f27d94afe732be2e9e6f05b9007d04f983a8)
- ref: a385add4015c431534e2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13710957475)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250306-linux-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250306-linux-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.12.6.md)
- [📈time plot](bm-20250306-linux-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250306-linux-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.13.0rc2.md)
- [📈time plot](bm-20250306-linux-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13710957475)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250306-vultr-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250306-vultr-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.12.6.md)
- [📈time plot](bm-20250306-vultr-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250306-vultr-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.13.0rc2.md)
- [📈time plot](bm-20250306-vultr-x86_64-python-a385add4015c431534e2-3.14.0a5%2B-a385add-vs-3.13.0rc2.svg)

