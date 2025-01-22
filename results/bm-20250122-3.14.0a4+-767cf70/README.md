# Results

- fork: python/767cf708449fbf13826d
- version: 3.14.0a4+
- config: 
- commit hash: [767cf70](https://github.com/python/cpython/commit/767cf70)
- commit date: 2025-01-22T00:26:37+00:00
- commit merge base: [01bcf13a1c5bfca5124cf2e0679c9d1b25b04708](https://github.com/python/cpython/commit/01bcf13a1c5bfca5124cf2e0679c9d1b25b04708)
- ref: 767cf708449fbf13826d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12903005922)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70-vs-3.12.6.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70-vs-3.13.0rc2.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 99.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70-vs-base-mem.svg)
- [📄table](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70-vs-base.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4%2B-767cf70-vs-base.svg)

