# Results

- fork: Fidget-Spinner/tracing_jit_regalloc
- version: 3.15.0a1+
- config: JIT
- commit hash: [d47bed2](https://github.com/Fidget%2dSpinner/cpython/commit/d47bed2)
- commit date: 2025-11-06T11:56:06+00:00
- commit merge base: [b1554146c29182803d1df23d6367c07a429d21ba](https://github.com/python/cpython/commit/b1554146c29182803d1df23d6367c07a429d21ba)
- ref: tracing_jit_regalloc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19153267511)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, pycparser, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2-vs-3.12.6.md)
- [📈time plot](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, pycparser, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.061x faster (HPT: reliability of 99.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: 🔴 docutils, pycparser
- [🧠memory plot](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2-vs-base-mem.svg)
- [📄table](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2-vs-base.md)
- [📈time plot](bm-20251106-vultr-x86_64-Fidget%252dSpinner-tracing_jit_regalloc-3.15.0a1%2B-d47bed2-vs-base.svg)

