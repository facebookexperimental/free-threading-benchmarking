# Results vs. base

- fork: Fidget-Spinner
- ref: dynamic_opcode_targe
- machine: darwin-arm64
- commit hash: 178b03e
- commit date: 2025-09-17
- overall geometric mean: 1.001x faster
- HPT reliability: 98.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 109 ms                                                                  | 108 ms: 1.01x faster                                                              |
| docutils       | 1.04 sec                                                                | 1.03 sec: 1.01x faster                                                            |
| html5lib       | 22.2 ms                                                                 | 21.9 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                                      |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 246 ms                                                                  | 240 ms: 1.02x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 260 ms                                                                  | 256 ms: 1.02x faster                                                              |
| async_tree_cpu_io_mixed          | 261 ms                                                                  | 257 ms: 1.02x faster                                                              |
| coroutines                       | 10.2 ms                                                                 | 10.0 ms: 1.01x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                  | 241 ms: 1.01x faster                                                              |
| async_tree_io_tg                 | 245 ms                                                                  | 242 ms: 1.01x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                  | 217 ms: 1.01x faster                                                              |
| async_tree_eager_tg              | 84.2 ms                                                                 | 83.3 ms: 1.01x faster                                                             |
| asyncio_websockets               | 190 ms                                                                  | 188 ms: 1.01x faster                                                              |
| async_tree_eager_memoization_tg  | 128 ms                                                                  | 127 ms: 1.01x faster                                                              |
| async_generators                 | 171 ms                                                                  | 169 ms: 1.01x faster                                                              |
| async_tree_eager                 | 38.9 ms                                                                 | 38.8 ms: 1.00x faster                                                             |
| Geometric mean                   | (ref)                                                                   | 1.01x faster                                                                      |

Benchmark hidden because not significant (7): async_tree_eager_io, async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_eager_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 28.9 ms                                                                 | 29.3 ms: 1.01x slower                                                             |
| nbody          | 47.4 ms                                                                 | 48.5 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                                   | 1.01x slower                                                                      |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 1.77 ms                                                                 | 1.74 ms: 1.02x faster                                                             |
| regex_compile  | 43.8 ms                                                                 | 43.5 ms: 1.01x faster                                                             |
| regex_v8       | 11.2 ms                                                                 | 11.2 ms: 1.01x faster                                                             |
| regex_dna      | 103 ms                                                                  | 104 ms: 1.01x slower                                                              |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| tomli_loads          | 795 ms                                                                  | 778 ms: 1.02x faster                                                              |
| unpickle_pure_python | 92.2 us                                                                 | 91.4 us: 1.01x faster                                                             |
| pickle_pure_python   | 134 us                                                                  | 134 us: 1.00x faster                                                              |
| xml_etree_process    | 23.7 ms                                                                 | 23.8 ms: 1.00x slower                                                             |
| xml_etree_generate   | 32.6 ms                                                                 | 32.9 ms: 1.01x slower                                                             |
| xml_etree_iterparse  | 43.5 ms                                                                 | 44.3 ms: 1.02x slower                                                             |
| xml_etree_parse      | 59.3 ms                                                                 | 64.6 ms: 1.09x slower                                                             |
| Geometric mean       | (ref)                                                                   | 1.01x slower                                                                      |

Benchmark hidden because not significant (2): json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|------------------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 6.12 ms                                                                 | 6.15 ms: 1.00x slower                                                             |
| python_startup         | 8.54 ms                                                                 | 8.59 ms: 1.01x slower                                                             |
| Geometric mean         | (ref)                                                                   | 1.01x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_text    | 9.03 ms                                                                 | 9.06 ms: 1.00x slower                                                             |
| mako           | 4.59 ms                                                                 | 4.69 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                                   | 1.01x slower                                                                      |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------------|:-----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| bench_thread_pool                | 411 us                                                                  | 396 us: 1.04x faster                                                              |
| async_tree_eager_io_tg           | 246 ms                                                                  | 240 ms: 1.02x faster                                                              |
| many_optionals                   | 313 us                                                                  | 306 us: 1.02x faster                                                              |
| tomli_loads                      | 795 ms                                                                  | 778 ms: 1.02x faster                                                              |
| subparsers                       | 17.3 ms                                                                 | 17.0 ms: 1.02x faster                                                             |
| spectral_norm                    | 46.0 ms                                                                 | 45.1 ms: 1.02x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 260 ms                                                                  | 256 ms: 1.02x faster                                                              |
| regex_effbot                     | 1.77 ms                                                                 | 1.74 ms: 1.02x faster                                                             |
| fannkuch                         | 172 ms                                                                  | 170 ms: 1.02x faster                                                              |
| async_tree_cpu_io_mixed          | 261 ms                                                                  | 257 ms: 1.02x faster                                                              |
| coroutines                       | 10.2 ms                                                                 | 10.0 ms: 1.01x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                  | 241 ms: 1.01x faster                                                              |
| comprehensions                   | 6.97 us                                                                 | 6.88 us: 1.01x faster                                                             |
| async_tree_io_tg                 | 245 ms                                                                  | 242 ms: 1.01x faster                                                              |
| pprint_pformat                   | 626 ms                                                                  | 618 ms: 1.01x faster                                                              |
| hexiom                           | 2.58 ms                                                                 | 2.55 ms: 1.01x faster                                                             |
| html5lib                         | 22.2 ms                                                                 | 21.9 ms: 1.01x faster                                                             |
| pprint_safe_repr                 | 311 ms                                                                  | 308 ms: 1.01x faster                                                              |
| 2to3                             | 109 ms                                                                  | 108 ms: 1.01x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                  | 217 ms: 1.01x faster                                                              |
| async_tree_eager_tg              | 84.2 ms                                                                 | 83.3 ms: 1.01x faster                                                             |
| crypto_pyaes                     | 37.0 ms                                                                 | 36.6 ms: 1.01x faster                                                             |
| asyncio_websockets               | 190 ms                                                                  | 188 ms: 1.01x faster                                                              |
| chaos                            | 25.6 ms                                                                 | 25.4 ms: 1.01x faster                                                             |
| unpickle_pure_python             | 92.2 us                                                                 | 91.4 us: 1.01x faster                                                             |
| deepcopy_reduce                  | 1.06 us                                                                 | 1.05 us: 1.01x faster                                                             |
| pyflate                          | 188 ms                                                                  | 186 ms: 1.01x faster                                                              |
| async_tree_eager_memoization_tg  | 128 ms                                                                  | 127 ms: 1.01x faster                                                              |
| async_generators                 | 171 ms                                                                  | 169 ms: 1.01x faster                                                              |
| regex_compile                    | 43.8 ms                                                                 | 43.5 ms: 1.01x faster                                                             |
| docutils                         | 1.04 sec                                                                | 1.03 sec: 1.01x faster                                                            |
| regex_v8                         | 11.2 ms                                                                 | 11.2 ms: 1.01x faster                                                             |
| nqueens                          | 37.9 ms                                                                 | 37.7 ms: 1.01x faster                                                             |
| logging_silent                   | 38.9 ns                                                                 | 38.7 ns: 1.01x faster                                                             |
| logging_format                   | 2.33 us                                                                 | 2.32 us: 1.01x faster                                                             |
| pickle_pure_python               | 134 us                                                                  | 134 us: 1.00x faster                                                              |
| sqlglot_v2_parse                 | 503 us                                                                  | 501 us: 1.00x faster                                                              |
| async_tree_eager                 | 38.9 ms                                                                 | 38.8 ms: 1.00x faster                                                             |
| gc_traversal                     | 2.03 ms                                                                 | 2.03 ms: 1.00x faster                                                             |
| sqlglot_v2_transpile             | 616 us                                                                  | 614 us: 1.00x faster                                                              |
| sqlglot_v2_optimize              | 21.4 ms                                                                 | 21.4 ms: 1.00x faster                                                             |
| coverage                         | 31.9 ms                                                                 | 32.0 ms: 1.00x slower                                                             |
| genshi_text                      | 9.03 ms                                                                 | 9.06 ms: 1.00x slower                                                             |
| xml_etree_process                | 23.7 ms                                                                 | 23.8 ms: 1.00x slower                                                             |
| pathlib                          | 10.4 ms                                                                 | 10.4 ms: 1.00x slower                                                             |
| meteor_contest                   | 48.1 ms                                                                 | 48.3 ms: 1.00x slower                                                             |
| python_startup_no_site           | 6.12 ms                                                                 | 6.15 ms: 1.00x slower                                                             |
| thrift                           | 292 us                                                                  | 293 us: 1.01x slower                                                              |
| connected_components             | 205 ms                                                                  | 206 ms: 1.01x slower                                                              |
| python_startup                   | 8.54 ms                                                                 | 8.59 ms: 1.01x slower                                                             |
| regex_dna                        | 103 ms                                                                  | 104 ms: 1.01x slower                                                              |
| sympy_str                        | 93.8 ms                                                                 | 94.4 ms: 1.01x slower                                                             |
| scimark_fft                      | 131 ms                                                                  | 132 ms: 1.01x slower                                                              |
| deepcopy_memo                    | 11.1 us                                                                 | 11.2 us: 1.01x slower                                                             |
| xml_etree_generate               | 32.6 ms                                                                 | 32.9 ms: 1.01x slower                                                             |
| float                            | 28.9 ms                                                                 | 29.3 ms: 1.01x slower                                                             |
| deltablue                        | 1.44 ms                                                                 | 1.46 ms: 1.01x slower                                                             |
| scimark_sor                      | 50.6 ms                                                                 | 51.2 ms: 1.01x slower                                                             |
| scimark_monte_carlo              | 28.6 ms                                                                 | 29.1 ms: 1.02x slower                                                             |
| xml_etree_iterparse              | 43.5 ms                                                                 | 44.3 ms: 1.02x slower                                                             |
| mako                             | 4.59 ms                                                                 | 4.69 ms: 1.02x slower                                                             |
| nbody                            | 47.4 ms                                                                 | 48.5 ms: 1.02x slower                                                             |
| xml_etree_parse                  | 59.3 ms                                                                 | 64.6 ms: 1.09x slower                                                             |
| Geometric mean                   | (ref)                                                                   | 1.00x faster                                                                      |

Benchmark hidden because not significant (40): async_tree_eager_io, k_core, async_tree_io, async_tree_memoization, json_loads, pycparser, async_tree_memoization_tg, django_template, bench_mp_pool, pylint, async_tree_none_tg, async_tree_eager_memoization, scimark_sparse_mat_mult, genshi_xml, dulwich_log, json, raytrace, typing_runtime_protocols, richards_super, bpe_tokeniser, sqlglot_v2_normalize, shortest_path, sympy_integrate, dask, pidigits, sqlite_synth, create_gc_cycles, deepcopy, sphinx, generators, telco, logging_simple, mdp, go, sympy_expand, scimark_lu, richards, sympy_sum, json_dumps, async_tree_none

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 98.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x