# Results

- fork: python/cebae977a63f32c3c03d
- version: 3.15.0a0
- config: NOGIL
- commit hash: [cebae97](https://github.com/python/cpython/commit/cebae97)
- commit date: 2025-06-01T00:33:02+03:00
- commit merge base: [3704171415c1ea6ebbeb2f992758b6565f42e378](https://github.com/python/cpython/commit/3704171415c1ea6ebbeb2f992758b6565f42e378)
- ref: cebae977a63f32c3c03d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15368876192)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json)

### vs. 3.12.6

- Geometric mean: 1.013x faster (HPT: reliability of 84.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.12.6.md)
- [📈time plot](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x slower (HPT: reliability of 94.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.13.0rc2.md)
- [📈time plot](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-base-mem.svg)
- [📄table](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-base.md)
- [📈time plot](bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15368876192)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 94.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.12.6.md)
- [📈time plot](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x faster (HPT: reliability of 84.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.13.0rc2.md)
- [📈time plot](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.013x slower (HPT: reliability of 98.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-base-mem.svg)
- [📄table](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-base.md)
- [📈time plot](bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97-vs-base.svg)

