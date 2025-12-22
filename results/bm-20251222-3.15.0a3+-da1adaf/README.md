# Results

- fork: chris-eibl/msvc_tail_call_new
- version: 3.15.0a3+
- config: 
- commit hash: [da1adaf](https://github.com/chris%2deibl/cpython/commit/da1adaf)
- commit date: 2025-12-22T19:16:34+01:00
- commit merge base: [700e9fad70da3f1da008c3231749e3861fbce897](https://github.com/python/cpython/commit/700e9fad70da3f1da008c3231749e3861fbce897)
- ref: msvc_tail_call_new

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20441405056)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf-vs-3.12.6.md)
- [📈time plot](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf-vs-3.13.0rc2.md)
- [📈time plot](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 86.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf-vs-base-mem.svg)
- [📄table](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf-vs-base.md)
- [📈time plot](bm-20251222-vultr-x86_64-chris%252deibl-msvc_tail_call_new-3.15.0a3%2B-da1adaf-vs-base.svg)

