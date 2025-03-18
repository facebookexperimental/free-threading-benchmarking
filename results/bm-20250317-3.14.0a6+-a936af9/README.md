# Results

- fork: python/a936af924efc6e2fb59e
- version: 3.14.0a6+
- config: 
- commit hash: [a936af9](https://github.com/python/cpython/commit/a936af9)
- commit date: 2025-03-17T18:34:37-04:00
- commit merge base: [f48887fb97651c02c5e412a75ed8b51a4ca11e6a](https://github.com/python/cpython/commit/f48887fb97651c02c5e412a75ed8b51a4ca11e6a)
- ref: a936af924efc6e2fb59e

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13912590604)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)
- [📈time plot](bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13912590604)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9.json)

### vs. 3.12.6

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 74.34%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13912590604)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)
- [📈time plot](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 84.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg)

