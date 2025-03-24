# Results

- fork: mpage/measure_latest_lfb
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [80fc5aa](https://github.com/mpage/cpython/commit/80fc5aa)
- commit date: 2025-03-23T14:38:35-07:00
- commit merge base: [ef06508f8ef1d2943b2fb1e310ab115b65e489a8](https://github.com/python/cpython/commit/ef06508f8ef1d2943b2fb1e310ab115b65e489a8)
- ref: measure_latest_lfb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14046064353)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 93.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa-vs-3.12.6.md)
- [📈time plot](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 60.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa-vs-3.13.0rc2.md)
- [📈time plot](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.026x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa-vs-base-mem.svg)
- [📄table](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa-vs-base.md)
- [📈time plot](bm-20250323-vultr-x86_64-mpage-measure_latest_lfb-3.14.0a6%2B-80fc5aa-vs-base.svg)

