# Results

- fork: python/7a918411a300ddeef06d
- version: 3.16.0a0
- config: JIT
- commit hash: [7a91841](https://github.com/python/cpython/commit/7a91841)
- commit date: 2026-09-05T17:00:22Z
- commit merge base: [e208bf0dda73b8e5a32af154f448e68ad11b26b7](https://github.com/python/cpython/commit/e208bf0dda73b8e5a32af154f448e68ad11b26b7)
- commit date: 2026-09-05T17:00:22+00:00
- ref: 7a918411a300ddeef06d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34001092175)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json)

### vs. 3.12.6

- Geometric mean: 1.165x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.12.6.md)
- [📈time plot](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.126x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.13.0rc2.md)
- [📈time plot](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-base-mem.svg)
- [📄table](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-base.md)
- [📈time plot](bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34001092175)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json)

### vs. 3.12.6

- Geometric mean: 1.260x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.12.6.md)
- [📈time plot](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.164x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.13.0rc2.md)
- [📈time plot](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-base-mem.svg)
- [📄table](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-base.md)
- [📈time plot](bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-vs-base.svg)

