# Results

- fork: python/5637f4e38a68cd015daa
- version: 3.16.0a0
- config: 
- commit hash: [5637f4e](https://github.com/python/cpython/commit/5637f4e)
- commit date: 2026-09-27T20:26:46-04:00
- commit merge base: [1c4fa4f98e64fbeda09ac0bcc9f4cba2f6d50349](https://github.com/python/cpython/commit/1c4fa4f98e64fbeda09ac0bcc9f4cba2f6d50349)
- ref: 5637f4e38a68cd015daa

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36363529387)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260927-vultr-x86_64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e.json)

### vs. 3.12.6

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260927-vultr-x86_64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.12.6.md)
- [📈time plot](bm-20260927-vultr-x86_64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 99.81%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260927-vultr-x86_64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260927-vultr-x86_64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36363529387)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e.json)

### vs. 3.12.6

- Geometric mean: 1.132x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.12.6.md)
- [📈time plot](bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 99.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e-vs-3.13.0rc2.svg)

