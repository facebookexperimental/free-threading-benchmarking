# Results

- fork: python/fad06746051f6bd95a25
- version: 3.16.0a0
- config: 
- commit hash: [fad0674](https://github.com/python/cpython/commit/fad0674)
- commit date: 2026-05-23T08:31:26-04:00
- commit merge base: [b0a149a8c6c4118fa0afecfe8c37d7c3b8651865](https://github.com/python/cpython/commit/b0a149a8c6c4118fa0afecfe8c37d7c3b8651865)
- ref: fad06746051f6bd95a25

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26347623596)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-pystats.json)
- [pystats table](bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-pystats.md)
- [raw results](bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674.json)

### vs. 3.12.6

- Geometric mean: 1.057x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-vs-3.12.6.md)
- [📈time plot](bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 98.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-vs-3.13.0rc2.md)
- [📈time plot](bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-vs-3.13.0rc2.svg)

