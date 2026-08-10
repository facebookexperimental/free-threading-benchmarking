# Results

- fork: python/998b89020456db591be4
- version: 3.16.0a0
- config: NOGIL
- commit hash: [998b890](https://github.com/python/cpython/commit/998b890)
- commit date: 2026-08-08T18:11:23+03:00
- commit merge base: [8ed1479619a3487af72a7c44bf61c9711370d4da](https://github.com/python/cpython/commit/8ed1479619a3487af72a7c44bf61c9711370d4da)
- ref: 998b89020456db591be4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31285717329)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 82.35%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890-vs-3.12.6.md)
- [📈time plot](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 96.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890-vs-3.13.0rc2.md)
- [📈time plot](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890-vs-base-mem.svg)
- [📄table](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890-vs-base.md)
- [📈time plot](bm-20260808-vultr-x86_64-python-998b89020456db591be4-3.16.0a0-998b890-vs-base.svg)

