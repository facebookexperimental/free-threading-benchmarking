# Results

- fork: python/29f8a67ae00081a36fdc
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [29f8a67](https://github.com/python/cpython/commit/29f8a67)
- commit date: 2025-02-08T23:35:28+00:00
- commit merge base: [c1f352bf0813803bb795b796c16040a5cd4115f2](https://github.com/python/cpython/commit/c1f352bf0813803bb795b796c16040a5cd4115f2)
- ref: 29f8a67ae00081a36fdc

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13220486562)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67.json)

### vs. 3.12.6

- Geometric mean: 1.003x faster (HPT: reliability of 98.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)
- [📈time plot](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x slower (HPT: reliability of 99.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)
- [📈time plot](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.123x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base-mem.svg)
- [📄table](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.md)
- [📈time plot](bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13220486562)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67.json)

### vs. 3.12.6

- Geometric mean: 1.048x slower (HPT: reliability of 99.96%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)
- [📈time plot](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)
- [📈time plot](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.132x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base-mem.svg)
- [📄table](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.md)
- [📈time plot](bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.svg)

