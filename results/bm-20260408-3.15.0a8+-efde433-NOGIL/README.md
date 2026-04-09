# Results

- fork: python/efde4333bfcdd1e24c2a
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [efde433](https://github.com/python/cpython/commit/efde433)
- commit date: 2026-04-08T23:34:46Z
- commit merge base: [09968dd2a9992a0171d5f4150e0a2e700d6651de](https://github.com/python/cpython/commit/09968dd2a9992a0171d5f4150e0a2e700d6651de)
- commit date: 2026-04-08T23:34:46+00:00
- ref: efde4333bfcdd1e24c2a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24166129438)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 63.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.md)
- [📈time plot](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 86.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.md)
- [📈time plot](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base-mem.svg)
- [📄table](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.md)
- [📈time plot](bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24166129438)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 99.90%, 1.01x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.md)
- [📈time plot](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 63.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.md)
- [📈time plot](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.052x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base-mem.svg)
- [📄table](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.md)
- [📈time plot](bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.svg)

