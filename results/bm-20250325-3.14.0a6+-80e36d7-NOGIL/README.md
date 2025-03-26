# Results

- fork: colesbury/gh_128421_fix_perf_r
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [80e36d7](https://github.com/colesbury/cpython/commit/80e36d7)
- commit date: 2025-03-25T20:27:08+00:00
- commit merge base: [8ada7a9e1435302ec2cb73375122072d0e1cdd6f](https://github.com/python/cpython/commit/8ada7a9e1435302ec2cb73375122072d0e1cdd6f)
- ref: gh_128421_fix_perf_r

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14069463091)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.98%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 97.75%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7-vs-base-mem.svg)
- [📄table](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7-vs-base.md)
- [📈time plot](bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6%2B-80e36d7-vs-base.svg)

