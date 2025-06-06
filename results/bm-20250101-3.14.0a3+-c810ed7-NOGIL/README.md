# Results

- fork: python/c810ed7c8e0a7464d197
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [c810ed7](https://github.com/python/cpython/commit/c810ed7)
- commit date: 2025-01-01T22:11:29+00:00
- commit merge base: [a327810169982e3782bdefc2247789a71aa79b43](https://github.com/python/cpython/commit/a327810169982e3782bdefc2247789a71aa79b43)
- ref: c810ed7c8e0a7464d197

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12575740700)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7.json)

### vs. 3.12.6

- Geometric mean: 1.166x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.md)
- [📈time plot](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.193x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.237x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base-mem.svg)
- [📄table](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base.md)
- [📈time plot](bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base.svg)

