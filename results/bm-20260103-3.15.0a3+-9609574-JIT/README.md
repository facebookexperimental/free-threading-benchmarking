# Results

- fork: python/9609574e7fd36edfaa8b
- version: 3.15.0a3+
- config: JIT
- commit hash: [9609574](https://github.com/python/cpython/commit/9609574)
- commit date: 2026-01-03T23:05:57+01:00
- commit merge base: [6c53af18f61c074d514e677b469b6201573a59da](https://github.com/python/cpython/commit/6c53af18f61c074d514e677b469b6201573a59da)
- ref: 9609574e7fd36edfaa8b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20684923315)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574.json)

### vs. 3.12.6

- Geometric mean: 1.124x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574-vs-3.12.6.md)
- [📈time plot](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574-vs-3.13.0rc2.md)
- [📈time plot](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.040x faster (HPT: reliability of 97.14%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574-vs-base-mem.svg)
- [📄table](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574-vs-base.md)
- [📈time plot](bm-20260103-vultr-x86_64-python-9609574e7fd36edfaa8b-3.15.0a3%2B-9609574-vs-base.svg)

