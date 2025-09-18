# Results

- fork: Fidget-Spinner/dynamic_opcode_targe
- version: 3.15.0a0
- config: CLANG
- commit hash: [178b03e](https://github.com/Fidget%2dSpinner/cpython/commit/178b03e)
- commit date: 2025-09-17T16:36:41+01:00
- commit merge base: [81c975bcfc1ac0533f9489a37e501ad5d3bdb4eb](https://github.com/python/cpython/commit/81c975bcfc1ac0533f9489a37e501ad5d3bdb4eb)
- ref: dynamic_opcode_targe

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17813555614)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e.json)

### vs. 3.12.6

- Geometric mean: 1.124x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.12.6.md)
- [📈time plot](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 92.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-base-mem.svg)
- [📄table](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-base.md)
- [📈time plot](bm-20250917-vultr-x86_64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17813555614)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e.json)

### vs. 3.12.6

- Geometric mean: 1.147x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.12.6.md)
- [📈time plot](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 98.34%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-base-mem.svg)
- [📄table](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-base.md)
- [📈time plot](bm-20250917-macm4pro-arm64-Fidget%252dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e-vs-base.svg)

