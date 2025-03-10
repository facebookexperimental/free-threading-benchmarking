# Results

- fork: python/98fa4a49fecbac3c990a
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [98fa4a4](https://github.com/python/cpython/commit/98fa4a4)
- commit date: 2025-03-09T16:09:23-04:00
- commit merge base: [475f933ed8b1c9546f1b5497a2241140c7065b5f](https://github.com/python/cpython/commit/475f933ed8b1c9546f1b5497a2241140c7065b5f)
- ref: 98fa4a49fecbac3c990a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13754065132)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 99.94%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.12.6.md)
- [📈time plot](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 99.94%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-base-mem.svg)
- [📄table](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-base.md)
- [📈time plot](bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13754065132)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.12.6.md)
- [📈time plot](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.144x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-base-mem.svg)
- [📄table](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-base.md)
- [📈time plot](bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5%2B-98fa4a4-vs-base.svg)

