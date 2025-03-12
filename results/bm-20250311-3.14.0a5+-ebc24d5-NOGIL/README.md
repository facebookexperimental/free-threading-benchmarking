# Results

- fork: python/ebc24d54bcf554403e9b
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [ebc24d5](https://github.com/python/cpython/commit/ebc24d5)
- commit date: 2025-03-11T23:17:58+00:00
- commit merge base: [c00ac578241b3213ceb79c1f32bc83ea471f02da](https://github.com/python/cpython/commit/c00ac578241b3213ceb79c1f32bc83ea471f02da)
- ref: ebc24d54bcf554403e9b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13800893559)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 99.94%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.md)
- [📈time plot](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base-mem.svg)
- [📄table](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.md)
- [📈time plot](bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13800893559)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.md)
- [📈time plot](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base-mem.svg)
- [📄table](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.md)
- [📈time plot](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.svg)

