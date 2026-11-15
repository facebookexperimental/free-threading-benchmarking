# Results

- fork: python/edd6f7692ad1bb30ba48
- version: 3.16.0a2+dev
- config: JIT
- commit hash: [edd6f76](https://github.com/python/cpython/commit/edd6f76)
- commit date: 2026-11-14T23:53:42Z
- commit merge base: [cc987451e8e902ddc0db77485faa34973b4e3ca8](https://github.com/python/cpython/commit/cc987451e8e902ddc0db77485faa34973b4e3ca8)
- commit date: 2026-11-14T23:53:42+00:00
- ref: edd6f7692ad1bb30ba48

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43657100611)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76.json)

### vs. 3.12.6

- Geometric mean: 1.209x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.12.6.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.168x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.13.0rc2.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-base-mem.svg)
- [📄table](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-base.md)
- [📈time plot](bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43657100611)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76.json)

### vs. 3.12.6

- Geometric mean: 1.338x faster (HPT: reliability of 100.00%, 1.20x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.12.6.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.236x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.13.0rc2.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.112x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-base-mem.svg)
- [📄table](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-base.md)
- [📈time plot](bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-vs-base.svg)

