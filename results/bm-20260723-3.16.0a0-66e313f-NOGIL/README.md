# Results

- fork: python/66e313f471516bfa04c5
- version: 3.16.0a0
- config: NOGIL
- commit hash: [66e313f](https://github.com/python/cpython/commit/66e313f)
- commit date: 2026-07-23T17:28:39+00:00
- commit merge base: [2b4e062a277f888c0139ac7196c2b6dcaed795dc](https://github.com/python/cpython/commit/2b4e062a277f888c0139ac7196c2b6dcaed795dc)
- ref: 66e313f471516bfa04c5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30056847903)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f.json)

### vs. 3.12.6

- Geometric mean: 1.034x slower (HPT: reliability of 79.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f-vs-3.12.6.md)
- [📈time plot](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 96.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f-vs-base-mem.svg)
- [📄table](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f-vs-base.md)
- [📈time plot](bm-20260723-vultr-x86_64-python-66e313f471516bfa04c5-3.16.0a0-66e313f-vs-base.svg)

