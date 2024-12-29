# Results

- fork: python/f9a5a3a3ef34e63dc197
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [f9a5a3a](https://github.com/python/cpython/commit/f9a5a3a)
- commit date: 2024-12-28T21:05:34+00:00
- commit merge base: [492b224b991cd9027f1bc6d9988d01e94f764992](https://github.com/python/cpython/commit/492b224b991cd9027f1bc6d9988d01e94f764992)
- ref: f9a5a3a3ef34e63dc197

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12530819968)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a.json)

### vs. 3.12.6

- Geometric mean: 1.105x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.md)
- [📈time plot](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.136x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.208x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base-mem.svg)
- [📄table](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.md)
- [📈time plot](bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12530819968)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a.json)

### vs. 3.12.6

- Geometric mean: 1.174x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.md)
- [📈time plot](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.201x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.239x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base-mem.svg)
- [📄table](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.md)
- [📈time plot](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.svg)

