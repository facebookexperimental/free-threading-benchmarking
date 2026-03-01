# Results

- fork: python/a1ec7467874207957519
- version: 3.15.0a6+
- config: JIT
- commit hash: [a1ec746](https://github.com/python/cpython/commit/a1ec746)
- commit date: 2026-02-28T22:26:47+00:00
- commit merge base: [50c2e23f69943a6f70d98c4d0bcf1ac37bcaf0d3](https://github.com/python/cpython/commit/50c2e23f69943a6f70d98c4d0bcf1ac37bcaf0d3)
- ref: a1ec7467874207957519

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22532170580)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746.json)

### vs. 3.12.6

- Geometric mean: 1.135x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)
- [📈time plot](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)
- [📈time plot](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.048x faster (HPT: reliability of 95.20%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: 🔴 genshi_text, genshi_xml
- [🧠memory plot](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base-mem.svg)
- [📄table](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.md)
- [📈time plot](bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.svg)

