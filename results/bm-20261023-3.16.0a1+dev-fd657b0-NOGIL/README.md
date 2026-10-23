# Results

- fork: python/fd657b067473fdf549df
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [fd657b0](https://github.com/python/cpython/commit/fd657b0)
- commit date: 2026-10-23T00:36:04Z
- commit merge base: [badd5d5ceb25aed7a402a30e265b653920e0dd40](https://github.com/python/cpython/commit/badd5d5ceb25aed7a402a30e265b653920e0dd40)
- commit date: 2026-10-23T00:36:04+00:00
- ref: fd657b067473fdf549df

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39879451555)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 71.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.12.6.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 98.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-base-mem.svg)
- [📄table](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-base.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39879451555)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 98.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.12.6.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 67.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-base-mem.svg)
- [📄table](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-base.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-base.svg)

