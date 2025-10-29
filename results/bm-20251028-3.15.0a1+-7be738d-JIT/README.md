# Results

- fork: Fidget-Spinner/tracing_jit_regalloc
- version: 3.15.0a1+
- config: JIT
- commit hash: [7be738d](https://github.com/Fidget%2dSpinner/cpython/commit/7be738d)
- commit date: 2025-10-28T22:42:16+00:00
- commit merge base: [a7160912274003672dc116d918260c0a81551c21](https://github.com/python/cpython/commit/a7160912274003672dc116d918260c0a81551c21)
- ref: tracing_jit_regalloc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18891527067)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d-vs-3.12.6.md)
- [📈time plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, pylint, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x faster (HPT: reliability of 99.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: 🔴 docutils, pylint, sphinx
- [🧠memory plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d-vs-base-mem.svg)
- [📄table](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d-vs-base.md)
- [📈time plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-7be738d-vs-base.svg)

