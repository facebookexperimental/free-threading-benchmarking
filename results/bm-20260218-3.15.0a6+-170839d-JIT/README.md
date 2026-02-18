# Results

- fork: Fidget-Spinner/no_invalidate_func
- version: 3.15.0a6+
- config: JIT
- commit hash: [170839d](https://github.com/Fidget%2dSpinner/cpython/commit/170839d)
- commit date: 2026-02-18T16:53:26Z
- commit merge base: [645f5c4a737b3eab29d0b7bcd4ec5f8bd36f332d](https://github.com/python/cpython/commit/645f5c4a737b3eab29d0b7bcd4ec5f8bd36f332d)
- commit date: 2026-02-18T16:53:26+00:00
- ref: no_invalidate_func

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22149285005)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d.json)

### vs. 3.12.6

- Geometric mean: 1.131x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.12.6.md)
- [📈time plot](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.093x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 78.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-base-mem.svg)
- [📄table](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-base.md)
- [📈time plot](bm-20260218-vultr-x86_64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22149285005)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d.json)

### vs. 3.12.6

- Geometric mean: 1.253x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.12.6.md)
- [📈time plot](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.161x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-base-mem.svg)
- [📄table](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-base.md)
- [📈time plot](bm-20260218-macm4pro-arm64-Fidget%252dSpinner-no_invalidate_func-3.15.0a6%2B-170839d-vs-base.svg)

