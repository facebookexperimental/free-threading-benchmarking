# Results

- fork: python/49234c065cf2b1ea32c5
- version: 3.14.0a6+
- config: 
- commit hash: [49234c0](https://github.com/python/cpython/commit/49234c0)
- commit date: 2025-03-18T14:31:13+01:00
- commit merge base: [8cb57dc3678a8b26772d0fffce525762fee4f234](https://github.com/python/cpython/commit/8cb57dc3678a8b26772d0fffce525762fee4f234)
- ref: 49234c065cf2b1ea32c5

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13925508624)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0.json)

### vs. 3.12.6

- Geometric mean: 1.042x faster (HPT: reliability of 76.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)
- [📈time plot](bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 70.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13925508624)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0.json)

### vs. 3.12.6

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 79.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13925508624)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0.json)

### vs. 3.12.6

- Geometric mean: 1.059x faster (HPT: reliability of 98.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x slower (HPT: reliability of 95.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- missing benchmarks: chameleon, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg)

