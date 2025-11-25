# Results

- fork: Fidget-Spinner/jit_lower_trace_limi
- version: 3.15.0a2+
- config: JIT
- commit hash: [f96af45](https://github.com/Fidget%2dSpinner/cpython/commit/f96af45)
- commit date: 2025-11-24T22:41:08Z
- commit merge base: [dc62b622524bf49eb539f444841049fdfbe2681e](https://github.com/python/cpython/commit/dc62b622524bf49eb539f444841049fdfbe2681e)
- commit date: 2025-11-24T22:41:08+00:00
- ref: jit_lower_trace_limi

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19651864805)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.md)
- [📈time plot](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.042x slower (HPT: reliability of 91.01%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- new benchmarks: 2to3, async_generators, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, asyncio_websockets, bench_mp_pool, bench_thread_pool, bpe_tokeniser, chaos, comprehensions, coroutines, coverage, create_gc_cycles, crypto_pyaes, deepcopy, deepcopy_memo, deepcopy_reduce, django_template, dulwich_log, fannkuch, float, gc_traversal, generators, genshi_text, genshi_xml, go, hexiom, html5lib, json, json_dumps, json_loads, logging_format, logging_silent, logging_simple, mako, many_optionals, mdp, meteor_contest, nbody, nqueens, pathlib, pickle_pure_python, pidigits, pprint_pformat, pprint_safe_repr, pycparser, pyflate, pylint, python_startup, python_startup_no_site, raytrace, regex_compile, regex_dna, regex_effbot, regex_v8, richards_super, scimark_fft, scimark_lu, scimark_monte_carlo, scimark_sor, scimark_sparse_mat_mult, spectral_norm, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, sqlite_synth, subparsers, sympy_expand, sympy_integrate, sympy_str, sympy_sum, telco, thrift, tomli_loads, typing_runtime_protocols, unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
- [🧠memory plot](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base-mem.svg)
- [📄table](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.md)
- [📈time plot](bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19651864805)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45.json)

### vs. 3.12.6

- Geometric mean: 1.162x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.md)
- [📈time plot](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x faster (HPT: reliability of 94.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 95.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- new benchmarks: dask
- [🧠memory plot](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base-mem.svg)
- [📄table](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.md)
- [📈time plot](bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.svg)

