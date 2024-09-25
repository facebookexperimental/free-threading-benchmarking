# Results vs. base

- fork: mpage
- ref: cec1c0b3fa171b6ab3ca
- machine: linux-x86_64
- commit hash: cec1c0b
- commit date: 2024-09-20
- overall geometric mean: 1.87x slower
- HPT reliability: 91.01%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.86x

| Benchmark      | bm-20240920-vultr-x86_64-python-main-3.14.0a0-342e654 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:-----------------------------------------------------:|:--------------------------------------------------------------------:|
| richards       | 43.2 ms                                               | 66.8 ms: 1.55x slower                                                |
| deltablue      | 3.07 ms                                               | 6.95 ms: 2.26x slower                                                |
| Geometric mean | (ref)                                                 | 1.87x slower                                                         |
Ignored benchmarks (95) of results/bm-20240920-3.14.0a0-cec1c0b/bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b.json: 2to3, async_generators, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, bench_mp_pool, bench_thread_pool, bpe_tokeniser, chaos, comprehensions, coroutines, coverage, create_gc_cycles, crypto_pyaes, deepcopy, deepcopy_memo, deepcopy_reduce, django_template, docutils, dulwich_log, fannkuch, float, gc_traversal, generators, genshi_text, genshi_xml, go, hexiom, html5lib, json, json_dumps, json_loads, logging_format, logging_silent, logging_simple, mako, mdp, meteor_contest, nbody, nqueens, pathlib, pickle, pickle_dict, pickle_list, pickle_pure_python, pidigits, pprint_pformat, pprint_safe_repr, pycparser, pyflate, pylint, python_startup, python_startup_no_site, raytrace, regex_compile, regex_dna, regex_effbot, regex_v8, richards_super, scimark_fft, scimark_lu, scimark_monte_carlo, scimark_sor, scimark_sparse_mat_mult, spectral_norm, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sqlite_synth, sympy_expand, sympy_integrate, sympy_str, sympy_sum, telco, thrift, tomli_loads, tornado_http, typing_runtime_protocols, unpack_sequence, unpickle, unpickle_list, unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process

# HPT report

- Reliability score: 91.01% likely to be slow
- 90% likely to have a slowdown of 1.54x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.86x