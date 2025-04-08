# Results

- fork: mpage/exp_no_slp_vect_rest
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [587a546](https://github.com/mpage/cpython/commit/587a546)
- commit date: 2025-04-08T13:47:39-07:00
- commit merge base: [e2b35ee22950bc5dc5410606f2e94a56b3454020](https://github.com/python/cpython/commit/e2b35ee22950bc5dc5410606f2e94a56b3454020)
- ref: exp_no_slp_vect_rest

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14343302825)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546.json)

### vs. 3.12.6

- Geometric mean: 1.016x slower (HPT: reliability of 99.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x slower (HPT: reliability of 99.48%, 1.01x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-base-mem.svg)
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-base.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6%2B-587a546-vs-default_base_vs_NOGIL.svg)

