# Results

- fork: python/30efede33ca1fe32debb
- version: 3.14.0a3+
- config: 
- commit hash: [30efede](https://github.com/python/cpython/commit/30efede)
- commit date: 2024-12-24T05:17:47+08:00
- commit merge base: [d61542b5ff1fe64705e5ce1bcc53048f14098dba](https://github.com/python/cpython/commit/d61542b5ff1fe64705e5ce1bcc53048f14098dba)
- ref: 30efede33ca1fe32debb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12474785779)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.svg)

