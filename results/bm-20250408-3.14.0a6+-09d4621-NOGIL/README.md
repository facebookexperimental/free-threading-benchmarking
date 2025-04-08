# Results

- fork: mpage/exp_no_slp_vectorize
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [09d4621](https://github.com/mpage/cpython/commit/09d4621)
- commit date: 2025-04-08T00:11:32-07:00
- commit merge base: [e2b35ee22950bc5dc5410606f2e94a56b3454020](https://github.com/python/cpython/commit/e2b35ee22950bc5dc5410606f2e94a56b3454020)
- ref: exp_no_slp_vectorize

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14339786251)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621.json)

### vs. 3.12.6

- Geometric mean: 1.033x faster (HPT: reliability of 76.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.md)
- [📈time plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x faster (HPT: reliability of 90.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 99.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base-mem.svg)
- [📄table](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.md)
- [📈time plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-default_base_vs_NOGIL.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14327398435)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 99.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 99.69%, 1.01x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.057x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base-mem.svg)
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-default_base_vs_NOGIL.svg)

