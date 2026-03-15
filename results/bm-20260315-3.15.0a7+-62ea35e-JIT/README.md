# Results

- fork: Fidget-Spinner/resume_tracing
- version: 3.15.0a7+
- config: JIT
- commit hash: [62ea35e](https://github.com/Fidget%2dSpinner/cpython/commit/62ea35e)
- commit date: 2026-03-15T18:03:50+08:00
- commit merge base: [788c3291172b55efa7cf8b33a315e4b0fe63540c](https://github.com/python/cpython/commit/788c3291172b55efa7cf8b33a315e4b0fe63540c)
- ref: resume_tracing

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23108218201)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e.json)

### vs. 3.12.6

- Geometric mean: 1.133x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.12.6.md)
- [📈time plot](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.095x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 84.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-base-mem.svg)
- [📄table](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-base.md)
- [📈time plot](bm-20260315-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23108218201)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e.json)

### vs. 3.12.6

- Geometric mean: 1.301x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.12.6.md)
- [📈time plot](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.206x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-base-mem.svg)
- [📄table](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-base.md)
- [📈time plot](bm-20260315-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-62ea35e-vs-base.svg)

