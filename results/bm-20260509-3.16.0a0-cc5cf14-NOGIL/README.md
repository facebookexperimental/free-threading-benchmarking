# Results

- fork: python/cc5cf14ae0a3665ba9d1
- version: 3.16.0a0
- config: NOGIL
- commit hash: [cc5cf14](https://github.com/python/cpython/commit/cc5cf14)
- commit date: 2026-05-09T14:39:01-07:00
- commit merge base: [4e97ff3351f381a61b238bd8e805e4e8dd3ea5cf](https://github.com/python/cpython/commit/4e97ff3351f381a61b238bd8e805e4e8dd3ea5cf)
- ref: cc5cf14ae0a3665ba9d1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25615626552)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 91.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.12.6.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 96.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.13.0rc2.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base-mem.svg)
- [📄table](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base.svg)

