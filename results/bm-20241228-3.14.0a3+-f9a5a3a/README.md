# Results

- fork: python/f9a5a3a3ef34e63dc197
- version: 3.14.0a3+
- config: 
- commit hash: [f9a5a3a](https://github.com/python/cpython/commit/f9a5a3a)
- commit date: 2024-12-28T21:05:34+00:00
- commit merge base: [492b224b991cd9027f1bc6d9988d01e94f764992](https://github.com/python/cpython/commit/492b224b991cd9027f1bc6d9988d01e94f764992)
- ref: f9a5a3a3ef34e63dc197

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12530819968)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.md)
- [📈time plot](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.svg)

