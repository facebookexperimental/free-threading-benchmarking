# Results

- fork: python/c08c89addfe30a3e0e70
- version: 3.16.0a0
- config: CLANG
- commit hash: [c08c89a](https://github.com/python/cpython/commit/c08c89a)
- commit date: 2026-07-19T02:24:16+02:00
- commit merge base: [a1d580430c81c298d267ec255d544d0fa1d197c4](https://github.com/python/cpython/commit/a1d580430c81c298d267ec255d544d0fa1d197c4)
- ref: c08c89addfe30a3e0e70

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29666996773)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a-vs-3.12.6.md)
- [📈time plot](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.029x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a-vs-base-mem.svg)
- [📄table](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a-vs-base.md)
- [📈time plot](bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a-vs-base.svg)

