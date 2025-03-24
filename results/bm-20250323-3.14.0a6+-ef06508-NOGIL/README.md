# Results

- fork: python/ef06508f8ef1d2943b2f
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [ef06508](https://github.com/python/cpython/commit/ef06508)
- commit date: 2025-03-23T19:56:03+05:30
- commit merge base: [5fc889ffbfd271c651f563ab0afe2d345bacbca5](https://github.com/python/cpython/commit/5fc889ffbfd271c651f563ab0afe2d345bacbca5)
- ref: ef06508f8ef1d2943b2f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14023363904)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.12.6.md)
- [📈time plot](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.13.0rc2.md)
- [📈time plot](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-base-mem.svg)
- [📄table](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-base.md)
- [📈time plot](bm-20250323-vultr-x86_64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14024567867)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 99.87%, 1.01x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.12.6.md)
- [📈time plot](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.13.0rc2.md)
- [📈time plot](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-base-mem.svg)
- [📄table](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-base.md)
- [📈time plot](bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6%2B-ef06508-vs-base.svg)

