# Results vs. base

- fork: Fidget-Spinner
- ref: dynamic_opcode_targe
- machine: linux-x86_64
- commit hash: 178b03e
- commit date: 2025-09-17
- overall geometric mean: 1.002x faster
- HPT reliability: 92.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| docutils       | 2.50 sec                                                              | 2.48 sec: 1.01x faster                                                          |
| html5lib       | 58.0 ms                                                               | 60.1 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                                    |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 247 ms                                                                | 242 ms: 1.02x faster                                                            |
| async_tree_memoization     | 306 ms                                                                | 302 ms: 1.01x faster                                                            |
| async_tree_cpu_io_mixed_tg | 477 ms                                                                | 473 ms: 1.01x faster                                                            |
| async_generators           | 313 ms                                                                | 317 ms: 1.01x slower                                                            |
| coroutines                 | 22.7 ms                                                               | 23.2 ms: 1.02x slower                                                           |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                                    |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_io, async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 82.9 ms                                                               | 79.7 ms: 1.04x faster                                                           |
| float          | 66.5 ms                                                               | 67.2 ms: 1.01x slower                                                           |
| pidigits       | 192 ms                                                                | 194 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 3.13 ms                                                               | 2.95 ms: 1.06x faster                                                           |
| regex_dna      | 190 ms                                                                | 182 ms: 1.04x faster                                                            |
| regex_v8       | 21.7 ms                                                               | 21.2 ms: 1.02x faster                                                           |
| regex_compile  | 118 ms                                                                | 119 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 8.89 ms                                                               | 8.84 ms: 1.01x faster                                                           |
| xml_etree_iterparse  | 94.2 ms                                                               | 94.7 ms: 1.00x slower                                                           |
| unpickle_pure_python | 199 us                                                                | 200 us: 1.01x slower                                                            |
| json_loads           | 25.2 us                                                               | 25.5 us: 1.01x slower                                                           |
| pickle_pure_python   | 294 us                                                                | 298 us: 1.01x slower                                                            |
| tomli_loads          | 1.76 sec                                                              | 1.80 sec: 1.03x slower                                                          |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                                    |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                               | 12.6 ms: 1.00x slower                                                           |
| python_startup_no_site | 7.31 ms                                                               | 7.34 ms: 1.00x slower                                                           |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|-----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 47.1 ms                                                               | 45.1 ms: 1.04x faster                                                           |
| genshi_text     | 19.6 ms                                                               | 19.1 ms: 1.03x faster                                                           |
| django_template | 32.5 ms                                                               | 32.3 ms: 1.01x faster                                                           |
| mako            | 11.2 ms                                                               | 11.6 ms: 1.04x slower                                                           |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot               | 3.13 ms                                                               | 2.95 ms: 1.06x faster                                                           |
| genshi_xml                 | 47.1 ms                                                               | 45.1 ms: 1.04x faster                                                           |
| regex_dna                  | 190 ms                                                                | 182 ms: 1.04x faster                                                            |
| scimark_sparse_mat_mult    | 4.06 ms                                                               | 3.90 ms: 1.04x faster                                                           |
| nbody                      | 82.9 ms                                                               | 79.7 ms: 1.04x faster                                                           |
| scimark_sor                | 101 ms                                                                | 97.2 ms: 1.04x faster                                                           |
| scimark_fft                | 284 ms                                                                | 275 ms: 1.03x faster                                                            |
| genshi_text                | 19.6 ms                                                               | 19.1 ms: 1.03x faster                                                           |
| typing_runtime_protocols   | 145 us                                                                | 141 us: 1.03x faster                                                            |
| regex_v8                   | 21.7 ms                                                               | 21.2 ms: 1.02x faster                                                           |
| fannkuch                   | 369 ms                                                                | 360 ms: 1.02x faster                                                            |
| richards_super             | 43.0 ms                                                               | 42.1 ms: 1.02x faster                                                           |
| scimark_lu                 | 99.0 ms                                                               | 96.8 ms: 1.02x faster                                                           |
| async_tree_none_tg         | 247 ms                                                                | 242 ms: 1.02x faster                                                            |
| pyflate                    | 399 ms                                                                | 390 ms: 1.02x faster                                                            |
| richards                   | 37.0 ms                                                               | 36.2 ms: 1.02x faster                                                           |
| pycparser                  | 1.07 sec                                                              | 1.05 sec: 1.02x faster                                                          |
| async_tree_memoization     | 306 ms                                                                | 302 ms: 1.01x faster                                                            |
| create_gc_cycles           | 2.02 ms                                                               | 2.00 ms: 1.01x faster                                                           |
| django_template            | 32.5 ms                                                               | 32.3 ms: 1.01x faster                                                           |
| pprint_pformat             | 1.38 sec                                                              | 1.37 sec: 1.01x faster                                                          |
| async_tree_cpu_io_mixed_tg | 477 ms                                                                | 473 ms: 1.01x faster                                                            |
| scimark_monte_carlo        | 55.1 ms                                                               | 54.7 ms: 1.01x faster                                                           |
| mdp                        | 1.10 sec                                                              | 1.10 sec: 1.01x faster                                                          |
| pprint_safe_repr           | 679 ms                                                                | 674 ms: 1.01x faster                                                            |
| nqueens                    | 74.9 ms                                                               | 74.4 ms: 1.01x faster                                                           |
| bpe_tokeniser              | 4.02 sec                                                              | 4.00 sec: 1.01x faster                                                          |
| json_dumps                 | 8.89 ms                                                               | 8.84 ms: 1.01x faster                                                           |
| docutils                   | 2.50 sec                                                              | 2.48 sec: 1.01x faster                                                          |
| go                         | 97.7 ms                                                               | 97.3 ms: 1.00x faster                                                           |
| sqlglot_v2_transpile       | 1.43 ms                                                               | 1.43 ms: 1.00x faster                                                           |
| python_startup             | 12.6 ms                                                               | 12.6 ms: 1.00x slower                                                           |
| python_startup_no_site     | 7.31 ms                                                               | 7.34 ms: 1.00x slower                                                           |
| sympy_str                  | 260 ms                                                                | 261 ms: 1.00x slower                                                            |
| sqlglot_v2_normalize       | 95.4 ms                                                               | 95.8 ms: 1.00x slower                                                           |
| xml_etree_iterparse        | 94.2 ms                                                               | 94.7 ms: 1.00x slower                                                           |
| unpickle_pure_python       | 199 us                                                                | 200 us: 1.01x slower                                                            |
| deltablue                  | 2.86 ms                                                               | 2.88 ms: 1.01x slower                                                           |
| telco                      | 154 ms                                                                | 155 ms: 1.01x slower                                                            |
| sympy_integrate            | 18.0 ms                                                               | 18.1 ms: 1.01x slower                                                           |
| pathlib                    | 17.3 ms                                                               | 17.4 ms: 1.01x slower                                                           |
| regex_compile              | 118 ms                                                                | 119 ms: 1.01x slower                                                            |
| chaos                      | 49.4 ms                                                               | 49.8 ms: 1.01x slower                                                           |
| sympy_sum                  | 148 ms                                                                | 149 ms: 1.01x slower                                                            |
| shortest_path              | 440 ms                                                                | 444 ms: 1.01x slower                                                            |
| comprehensions             | 14.2 us                                                               | 14.3 us: 1.01x slower                                                           |
| raytrace                   | 232 ms                                                                | 235 ms: 1.01x slower                                                            |
| float                      | 66.5 ms                                                               | 67.2 ms: 1.01x slower                                                           |
| pidigits                   | 192 ms                                                                | 194 ms: 1.01x slower                                                            |
| json_loads                 | 25.2 us                                                               | 25.5 us: 1.01x slower                                                           |
| logging_format             | 6.28 us                                                               | 6.36 us: 1.01x slower                                                           |
| meteor_contest             | 99.9 ms                                                               | 101 ms: 1.01x slower                                                            |
| deepcopy_memo              | 24.2 us                                                               | 24.6 us: 1.01x slower                                                           |
| async_generators           | 313 ms                                                                | 317 ms: 1.01x slower                                                            |
| pickle_pure_python         | 294 us                                                                | 298 us: 1.01x slower                                                            |
| generators                 | 26.9 ms                                                               | 27.4 ms: 1.02x slower                                                           |
| coroutines                 | 22.7 ms                                                               | 23.2 ms: 1.02x slower                                                           |
| deepcopy                   | 220 us                                                                | 225 us: 1.02x slower                                                            |
| logging_simple             | 5.54 us                                                               | 5.68 us: 1.03x slower                                                           |
| tomli_loads                | 1.76 sec                                                              | 1.80 sec: 1.03x slower                                                          |
| deepcopy_reduce            | 2.35 us                                                               | 2.41 us: 1.03x slower                                                           |
| html5lib                   | 58.0 ms                                                               | 60.1 ms: 1.04x slower                                                           |
| mako                       | 11.2 ms                                                               | 11.6 ms: 1.04x slower                                                           |
| gc_traversal               | 4.38 ms                                                               | 4.60 ms: 1.05x slower                                                           |
| spectral_norm              | 81.0 ms                                                               | 85.8 ms: 1.06x slower                                                           |
| logging_silent             | 77.8 ns                                                               | 83.0 ns: 1.07x slower                                                           |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                                    |

Benchmark hidden because not significant (28): async_tree_memoization_tg, sphinx, async_tree_io, async_tree_io_tg, async_tree_none, xml_etree_process, pylint, xml_etree_parse, async_tree_cpu_io_mixed, sqlglot_v2_parse, k_core, subparsers, 2to3, bench_thread_pool, crypto_pyaes, asyncio_websockets, sympy_expand, dulwich_log, hexiom, sqlglot_v2_optimize, connected_components, sqlite_synth, many_optionals, json, thrift, coverage, xml_etree_generate, bench_mp_pool

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 92.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x