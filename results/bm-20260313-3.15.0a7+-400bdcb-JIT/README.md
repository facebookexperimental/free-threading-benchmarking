# Results

- fork: Fidget-Spinner/resume_tracing
- version: 3.15.0a7+
- config: JIT
- commit hash: [400bdcb](https://github.com/Fidget%2dSpinner/cpython/commit/400bdcb)
- commit date: 2026-03-13T17:26:30+08:00
- commit merge base: [0adc7289c3ab097b5608c0d288d91e1f5f236469](https://github.com/python/cpython/commit/0adc7289c3ab097b5608c0d288d91e1f5f236469)
- ref: resume_tracing

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23045034349)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb.json)

### vs. 3.12.6

- Geometric mean: 1.137x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.12.6.md)
- [📈time plot](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 79.13%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-base-mem.svg)
- [📄table](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-base.md)
- [📈time plot](bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-base.svg)

