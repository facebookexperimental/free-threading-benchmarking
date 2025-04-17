# Results

- fork: python/39ee468e092eed659bfc
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [39ee468](https://github.com/python/cpython/commit/39ee468)
- commit date: 2025-04-17T03:46:36+00:00
- commit merge base: [b530e174a3f870f0795200fee197a46e8bbfd0e8](https://github.com/python/cpython/commit/b530e174a3f870f0795200fee197a46e8bbfd0e8)
- ref: 39ee468e092eed659bfc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14509698475)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468.json)

### vs. 3.12.6

- Geometric mean: 1.027x faster (HPT: reliability of 70.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-3.12.6.md)
- [📈time plot](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x slower (HPT: reliability of 92.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-3.13.0rc2.md)
- [📈time plot](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 69.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-base-mem.svg)
- [📄table](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-base.md)
- [📈time plot](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.079x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7%2B-39ee468-vs-default_base_vs_NOGIL.svg)

