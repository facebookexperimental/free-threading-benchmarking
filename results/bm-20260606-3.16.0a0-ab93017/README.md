# Results

- fork: python/ab930175e7e909aaa3ec
- version: 3.16.0a0
- config: 
- commit hash: [ab93017](https://github.com/python/cpython/commit/ab93017)
- commit date: 2026-06-06T21:38:15+00:00
- commit merge base: [69851a64076cc240513b834d87d654064f7ac597](https://github.com/python/cpython/commit/69851a64076cc240513b834d87d654064f7ac597)
- ref: ab930175e7e909aaa3ec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27078289949)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20260606-vultr-x86_64-python-ab930175e7e909aaa3ec-3.16.0a0-ab93017-pystats.json)
- [pystats table](bm-20260606-vultr-x86_64-python-ab930175e7e909aaa3ec-3.16.0a0-ab93017-pystats.md)
- [raw results](bm-20260606-vultr-x86_64-python-ab930175e7e909aaa3ec-3.16.0a0-ab93017.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260606-vultr-x86_64-python-ab930175e7e909aaa3ec-3.16.0a0-ab93017-vs-3.12.6.md)
- [📈time plot](bm-20260606-vultr-x86_64-python-ab930175e7e909aaa3ec-3.16.0a0-ab93017-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 99.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260606-vultr-x86_64-python-ab930175e7e909aaa3ec-3.16.0a0-ab93017-vs-3.13.0rc2.md)
- [📈time plot](bm-20260606-vultr-x86_64-python-ab930175e7e909aaa3ec-3.16.0a0-ab93017-vs-3.13.0rc2.svg)

