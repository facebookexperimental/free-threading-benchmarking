# Results

- fork: python/a03efb533a58fd13fb0c
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [a03efb5](https://github.com/python/cpython/commit/a03efb5)
- commit date: 2024-12-08T10:46:34-08:00
- commit merge base: [7f8ec523021427a5c1ab3ce0cdd6e4bb909f1dc5](https://github.com/python/cpython/commit/7f8ec523021427a5c1ab3ce0cdd6e4bb909f1dc5)
- ref: a03efb533a58fd13fb0c

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12226650498)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5.json)

### vs. 3.12.6

- Geometric mean: 1.156x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.12.6.md)
- [📈time plot](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.185x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.13.0rc2.md)
- [📈time plot](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.248x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-base-mem.svg)
- [📄table](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-base.md)
- [📈time plot](bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12226650498)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5.json)

### vs. 3.12.6

- Geometric mean: 1.229x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.12.6.md)
- [📈time plot](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.254x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.13.0rc2.md)
- [📈time plot](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.273x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.18x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-base-mem.svg)
- [📄table](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-base.md)
- [📈time plot](bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2%2B-a03efb5-vs-base.svg)

