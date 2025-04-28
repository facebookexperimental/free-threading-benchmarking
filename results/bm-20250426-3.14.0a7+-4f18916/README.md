# Results

- fork: python/4f18916c5c28321f363e
- version: 3.14.0a7+
- config: 
- commit hash: [4f18916](https://github.com/python/cpython/commit/4f18916)
- commit date: 2025-04-26T18:43:23-04:00
- commit merge base: [ee033d455577dd7af6c5421f3365eba1c9af1087](https://github.com/python/cpython/commit/ee033d455577dd7af6c5421f3365eba1c9af1087)
- ref: 4f18916c5c28321f363e

## linux x86_64 (linux)

- [pystats raw](bm-20250426-linux-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-pystats.json)
- [pystats table](bm-20250426-linux-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-pystats.md)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14686405826)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916.json)

### vs. 3.12.6

- Geometric mean: 1.117x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.md)
- [📈time plot](bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.md)
- [📈time plot](bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.svg)

