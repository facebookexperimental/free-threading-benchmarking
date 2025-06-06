# Results

- fork: python/22a442181d5f1ac496da
- version: 3.14.0a3+
- config: 
- commit hash: [22a4421](https://github.com/python/cpython/commit/22a4421)
- commit date: 2025-01-11T19:27:47+00:00
- commit merge base: [0946ed25b53dddfa4eb040513720353b7214d71b](https://github.com/python/cpython/commit/0946ed25b53dddfa4eb040513720353b7214d71b)
- ref: 22a442181d5f1ac496da

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12728736793)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-pystats.json)
- [pystats table](bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-pystats.md)
- [raw results](bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.svg)

