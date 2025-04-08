# Results

- fork: mpage/exp_no_slp_vectorize
- version: 3.14.0a6+
- config: 
- commit hash: [09d4621](https://github.com/mpage/cpython/commit/09d4621)
- commit date: 2025-04-08T00:11:32-07:00
- commit merge base: [e2b35ee22950bc5dc5410606f2e94a56b3454020](https://github.com/python/cpython/commit/e2b35ee22950bc5dc5410606f2e94a56b3454020)
- ref: exp_no_slp_vectorize

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14339790346)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621.json)

### vs. 3.12.6

- Geometric mean: 1.126x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.md)
- [📈time plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base-mem.svg)
- [📄table](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.md)
- [📈time plot](bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14327400350)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621.json)

### vs. 3.12.6

- Geometric mean: 1.125x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.045x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base-mem.svg)
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6%2B-09d4621-vs-base.svg)

