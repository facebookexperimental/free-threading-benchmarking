# Results

- fork: python/0e353134844fd50628f3
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [0e35313](https://github.com/python/cpython/commit/0e35313)
- commit date: 2026-10-26T15:09:33-07:00
- commit merge base: [3acc941f2b7288b212a4163ab21aa79faff9cd13](https://github.com/python/cpython/commit/3acc941f2b7288b212a4163ab21aa79faff9cd13)
- ref: 0e353134844fd50628f3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40427761408)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 70.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.md)
- [📈time plot](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 93.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.md)
- [📈time plot](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base-mem.svg)
- [📄table](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.md)
- [📈time plot](bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40427761408)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 97.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.md)
- [📈time plot](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 72.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.md)
- [📈time plot](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base-mem.svg)
- [📄table](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.md)
- [📈time plot](bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.svg)

