# Results

- fork: python/6ce088e20a13ac25320d
- version: 3.16.0a0
- config: NOGIL
- commit hash: [6ce088e](https://github.com/python/cpython/commit/6ce088e)
- commit date: 2026-06-14T00:10:56+01:00
- commit merge base: [9ad6ba0324a71ae5b51ded6e59b1ea3b653814a5](https://github.com/python/cpython/commit/9ad6ba0324a71ae5b51ded6e59b1ea3b653814a5)
- ref: 6ce088e20a13ac25320d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27483803137)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e.json)

### vs. 3.12.6

- Geometric mean: 1.032x slower (HPT: reliability of 88.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-vs-3.12.6.md)
- [📈time plot](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 97.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-vs-base-mem.svg)
- [📄table](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-vs-base.md)
- [📈time plot](bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-vs-base.svg)

