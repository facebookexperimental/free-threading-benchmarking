# Results

- fork: python/5ec4bf86b7f4455432ae
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [5ec4bf8](https://github.com/python/cpython/commit/5ec4bf8)
- commit date: 2025-02-22T17:54:43+00:00
- commit merge base: [3cc9e867eba1ed139cf28c74b4a788bcc4801394](https://github.com/python/cpython/commit/3cc9e867eba1ed139cf28c74b4a788bcc4801394)
- ref: 5ec4bf86b7f4455432ae

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13477790620)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.md)
- [📈time plot](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.124x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base-mem.svg)
- [📄table](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base.md)
- [📈time plot](bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base.svg)

