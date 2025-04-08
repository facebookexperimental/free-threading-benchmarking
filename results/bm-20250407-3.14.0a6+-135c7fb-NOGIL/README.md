# Results

- fork: mpage/exp_no_vectorize
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [135c7fb](https://github.com/mpage/cpython/commit/135c7fb)
- commit date: 2025-04-07T18:26:58-07:00
- commit merge base: [e2b35ee22950bc5dc5410606f2e94a56b3454020](https://github.com/python/cpython/commit/e2b35ee22950bc5dc5410606f2e94a56b3454020)
- ref: exp_no_vectorize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14323029059)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb.json)

### vs. 3.12.6

- Geometric mean: 1.011x slower (HPT: reliability of 99.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-3.12.6.md)
- [📈time plot](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x slower (HPT: reliability of 99.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-base-mem.svg)
- [📄table](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-base.md)
- [📈time plot](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6%2B-135c7fb-vs-default_base_vs_NOGIL.svg)

