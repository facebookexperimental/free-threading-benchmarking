# Results

- fork: python/e82c2ca2a59235bc1965
- version: 3.14.0a6+
- config: 
- commit hash: [e82c2ca](https://github.com/python/cpython/commit/e82c2ca)
- commit date: 2025-03-15T18:55:00+00:00
- commit merge base: [f104c19a94ae43f788e509019901b1f48fbd134e](https://github.com/python/cpython/commit/f104c19a94ae43f788e509019901b1f48fbd134e)
- ref: e82c2ca2a59235bc1965

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13877932822)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca.json)

### vs. 3.12.6

- Geometric mean: 1.060x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.md)
- [📈time plot](bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 76.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.md)
- [📈time plot](bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.svg)

