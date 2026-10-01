# Results

- fork: python/763b6edb0ec959bdfb78
- version: 3.16.0a0
- config: NOGIL
- commit hash: [763b6ed](https://github.com/python/cpython/commit/763b6ed)
- commit date: 2026-10-01T06:48:34+08:00
- commit merge base: [e580c888746411d3b576b5c3c2ce8b34293ddaf2](https://github.com/python/cpython/commit/e580c888746411d3b576b5c3c2ce8b34293ddaf2)
- ref: 763b6edb0ec959bdfb78

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36798288173)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json)

### vs. 3.12.6

- Geometric mean: 1.045x slower (HPT: reliability of 82.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.md)
- [📈time plot](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 98.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base-mem.svg)
- [📄table](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.md)
- [📈time plot](bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36798288173)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 97.13%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.md)
- [📈time plot](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 90.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.043x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base-mem.svg)
- [📄table](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.md)
- [📈time plot](bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.svg)

