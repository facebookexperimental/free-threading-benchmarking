# Results

- fork: mpage/lfb_nolock
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [a350570](https://github.com/mpage/cpython/commit/a350570)
- commit date: 2025-03-19T17:23:23-07:00
- commit merge base: [fd545d735d5f9c048f99767c700f72853a9b7acd](https://github.com/python/cpython/commit/fd545d735d5f9c048f99767c700f72853a9b7acd)
- ref: lfb_nolock

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13959304877)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570.json)

### vs. 3.12.6

- Geometric mean: 1.005x slower (HPT: reliability of 96.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-3.12.6.md)
- [📈time plot](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x slower (HPT: reliability of 99.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-base-mem.svg)
- [📄table](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-base.md)
- [📈time plot](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.067x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- new benchmarks: html5lib, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6%2B-a350570-vs-default_base_vs_NOGIL.svg)

