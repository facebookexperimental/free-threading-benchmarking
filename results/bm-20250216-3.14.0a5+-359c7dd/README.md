# Results

- fork: python/359c7dde3bb074e02968
- version: 3.14.0a5+
- config: 
- commit hash: [359c7dd](https://github.com/python/cpython/commit/359c7dd)
- commit date: 2025-02-16T03:01:24+08:00
- commit merge base: [c26bed1160978fe8b1844878b8123778e47870c6](https://github.com/python/cpython/commit/c26bed1160978fe8b1844878b8123778e47870c6)
- ref: 359c7dde3bb074e02968

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13349846653)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.md)
- [📈time plot](bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.svg)

