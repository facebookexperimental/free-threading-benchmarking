# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: eb89286
- commit date: 2025-12-01
- overall geometric mean: 1.491x faster
- HPT reliability: 91.01%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.05x

| Benchmark      | bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2+-eb89286 | bm-20251201-vultr-x86_64-python-main-3.15.0a2+-eb89286 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| richards       | 42.4 ms                                                                | 21.0 ms: 2.02x faster                                  |
| deltablue      | 3.11 ms                                                                | 2.86 ms: 1.09x faster                                  |
| Geometric mean | (ref)                                                                  | 1.48x faster                                           |
Ignored benchmarks (89) of results/bm-20251201-3.15.0a2+-eb89286/bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2+-eb89286.json: 2to3, async_generators, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, asyncio_websockets, bench_mp_pool, bench_thread_pool, bpe_tokeniser, chaos, comprehensions, coroutines, coverage, create_gc_cycles, crypto_pyaes, deepcopy, deepcopy_memo, deepcopy_reduce, django_template, docutils, dulwich_log, fannkuch, float, gc_traversal, generators, genshi_text, genshi_xml, go, hexiom, html5lib, json, json_dumps, json_loads, logging_format, logging_silent, logging_simple, mako, many_optionals, mdp, meteor_contest, nbody, nqueens, pathlib, pickle_pure_python, pidigits, pprint_pformat, pprint_safe_repr, pycparser, pyflate, pylint, python_startup, python_startup_no_site, raytrace, regex_compile, regex_dna, regex_effbot, regex_v8, richards_super, scimark_fft, scimark_lu, scimark_monte_carlo, scimark_sor, scimark_sparse_mat_mult, spectral_norm, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, sqlite_synth, subparsers, sympy_expand, sympy_integrate, sympy_str, sympy_sum, telco, thrift, tomli_loads, typing_runtime_protocols, unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process

- Geometric mean (including insignificant results): 1.491x faster

# HPT report

- Reliability score: 91.01% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.05x