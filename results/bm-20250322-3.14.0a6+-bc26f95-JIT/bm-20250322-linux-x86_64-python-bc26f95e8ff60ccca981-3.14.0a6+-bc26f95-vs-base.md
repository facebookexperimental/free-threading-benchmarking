# Results vs. base

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.009x slower
- HPT reliability: 98.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 404 ms                                                                                                            | 437 ms: 1.08x slower                                                                                                  |
| docutils       | 3.55 sec                                                                                                          | 3.70 sec: 1.04x slower                                                                                                |
| sphinx         | 1.37 sec                                                                                                          | 1.41 sec: 1.03x slower                                                                                                |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 31.8 ms                                                                                                           | 29.4 ms: 1.08x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                                                            | 645 ms: 1.03x faster                                                                                                  |
| async_tree_memoization_tg  | 440 ms                                                                                                            | 460 ms: 1.05x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 664 ms                                                                                                            | 695 ms: 1.05x slower                                                                                                  |
| asyncio_tcp                | 853 ms                                                                                                            | 907 ms: 1.06x slower                                                                                                  |
| async_generators           | 479 ms                                                                                                            | 518 ms: 1.08x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (7): async_tree_none, asyncio_websockets, async_tree_none_tg, asyncio_tcp_ssl, async_tree_io, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 129 ms                                                                                                            | 111 ms: 1.16x faster                                                                                                  |
| float          | 95.4 ms                                                                                                           | 89.9 ms: 1.06x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.08x faster                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 180 ms                                                                                                            | 171 ms: 1.05x faster                                                                                                  |
| regex_dna      | 275 ms                                                                                                            | 283 ms: 1.03x slower                                                                                                  |
| regex_effbot   | 3.99 ms                                                                                                           | 4.50 ms: 1.13x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|---------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pickle_dict         | 45.6 us                                                                                                           | 41.0 us: 1.11x faster                                                                                                 |
| pickle_list         | 6.61 us                                                                                                           | 6.11 us: 1.08x faster                                                                                                 |
| xml_etree_iterparse | 139 ms                                                                                                            | 136 ms: 1.02x faster                                                                                                  |
| tomli_loads         | 2.43 sec                                                                                                          | 2.39 sec: 1.02x faster                                                                                                |
| xml_etree_parse     | 186 ms                                                                                                            | 193 ms: 1.04x slower                                                                                                  |
| pickle              | 16.4 us                                                                                                           | 17.2 us: 1.05x slower                                                                                                 |
| pickle_pure_python  | 399 us                                                                                                            | 424 us: 1.06x slower                                                                                                  |
| unpickle_list       | 6.88 us                                                                                                           | 7.32 us: 1.06x slower                                                                                                 |
| unpickle            | 18.5 us                                                                                                           | 19.7 us: 1.06x slower                                                                                                 |
| Geometric mean      | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (5): unpickle_pure_python, json_dumps, xml_etree_process, json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 44.1 ms                                                                                                           | 46.1 ms: 1.05x slower                                                                                                 |
| genshi_text     | 27.0 ms                                                                                                           | 28.3 ms: 1.05x slower                                                                                                 |
| genshi_xml      | 63.7 ms                                                                                                           | 73.1 ms: 1.15x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.05x slower                                                                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards                   | 57.6 ms                                                                                                           | 47.2 ms: 1.22x faster                                                                                                 |
| nbody                      | 129 ms                                                                                                            | 111 ms: 1.16x faster                                                                                                  |
| coverage                   | 122 ms                                                                                                            | 107 ms: 1.14x faster                                                                                                  |
| scimark_fft                | 438 ms                                                                                                            | 392 ms: 1.12x faster                                                                                                  |
| pickle_dict                | 45.6 us                                                                                                           | 41.0 us: 1.11x faster                                                                                                 |
| dulwich_log                | 89.6 ms                                                                                                           | 82.2 ms: 1.09x faster                                                                                                 |
| deepcopy_reduce            | 3.75 us                                                                                                           | 3.44 us: 1.09x faster                                                                                                 |
| richards_super             | 66.4 ms                                                                                                           | 61.1 ms: 1.09x faster                                                                                                 |
| coroutines                 | 31.8 ms                                                                                                           | 29.4 ms: 1.08x faster                                                                                                 |
| pickle_list                | 6.61 us                                                                                                           | 6.11 us: 1.08x faster                                                                                                 |
| meteor_contest             | 146 ms                                                                                                            | 138 ms: 1.06x faster                                                                                                  |
| float                      | 95.4 ms                                                                                                           | 89.9 ms: 1.06x faster                                                                                                 |
| regex_compile              | 180 ms                                                                                                            | 171 ms: 1.05x faster                                                                                                  |
| deltablue                  | 4.04 ms                                                                                                           | 3.84 ms: 1.05x faster                                                                                                 |
| sqlglot_v2_transpile       | 2.22 ms                                                                                                           | 2.13 ms: 1.04x faster                                                                                                 |
| logging_simple             | 7.86 us                                                                                                           | 7.62 us: 1.03x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                                                            | 645 ms: 1.03x faster                                                                                                  |
| sqlalchemy_declarative     | 173 ms                                                                                                            | 169 ms: 1.03x faster                                                                                                  |
| xml_etree_iterparse        | 139 ms                                                                                                            | 136 ms: 1.02x faster                                                                                                  |
| tomli_loads                | 2.43 sec                                                                                                          | 2.39 sec: 1.02x faster                                                                                                |
| pprint_safe_repr           | 938 ms                                                                                                            | 957 ms: 1.02x slower                                                                                                  |
| mdp                        | 3.46 sec                                                                                                          | 3.53 sec: 1.02x slower                                                                                                |
| json                       | 6.57 ms                                                                                                           | 6.72 ms: 1.02x slower                                                                                                 |
| logging_silent             | 117 ns                                                                                                            | 120 ns: 1.02x slower                                                                                                  |
| pycparser                  | 1.50 sec                                                                                                          | 1.54 sec: 1.03x slower                                                                                                |
| crypto_pyaes               | 93.4 ms                                                                                                           | 95.9 ms: 1.03x slower                                                                                                 |
| regex_dna                  | 275 ms                                                                                                            | 283 ms: 1.03x slower                                                                                                  |
| sphinx                     | 1.37 sec                                                                                                          | 1.41 sec: 1.03x slower                                                                                                |
| scimark_monte_carlo        | 86.9 ms                                                                                                           | 90.0 ms: 1.03x slower                                                                                                 |
| pathlib                    | 28.3 ms                                                                                                           | 29.3 ms: 1.04x slower                                                                                                 |
| xml_etree_parse            | 186 ms                                                                                                            | 193 ms: 1.04x slower                                                                                                  |
| deepcopy_memo              | 36.3 us                                                                                                           | 37.8 us: 1.04x slower                                                                                                 |
| docutils                   | 3.55 sec                                                                                                          | 3.70 sec: 1.04x slower                                                                                                |
| subparsers                 | 28.4 ms                                                                                                           | 29.6 ms: 1.04x slower                                                                                                 |
| async_tree_memoization_tg  | 440 ms                                                                                                            | 460 ms: 1.05x slower                                                                                                  |
| logging_format             | 8.82 us                                                                                                           | 9.22 us: 1.05x slower                                                                                                 |
| django_template            | 44.1 ms                                                                                                           | 46.1 ms: 1.05x slower                                                                                                 |
| typing_runtime_protocols   | 214 us                                                                                                            | 224 us: 1.05x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 664 ms                                                                                                            | 695 ms: 1.05x slower                                                                                                  |
| genshi_text                | 27.0 ms                                                                                                           | 28.3 ms: 1.05x slower                                                                                                 |
| pickle                     | 16.4 us                                                                                                           | 17.2 us: 1.05x slower                                                                                                 |
| nqueens                    | 107 ms                                                                                                            | 112 ms: 1.05x slower                                                                                                  |
| sympy_str                  | 338 ms                                                                                                            | 355 ms: 1.05x slower                                                                                                  |
| go                         | 156 ms                                                                                                            | 165 ms: 1.05x slower                                                                                                  |
| sympy_expand               | 575 ms                                                                                                            | 611 ms: 1.06x slower                                                                                                  |
| pickle_pure_python         | 399 us                                                                                                            | 424 us: 1.06x slower                                                                                                  |
| unpickle_list              | 6.88 us                                                                                                           | 7.32 us: 1.06x slower                                                                                                 |
| asyncio_tcp                | 853 ms                                                                                                            | 907 ms: 1.06x slower                                                                                                  |
| unpickle                   | 18.5 us                                                                                                           | 19.7 us: 1.06x slower                                                                                                 |
| generators                 | 38.4 ms                                                                                                           | 41.0 ms: 1.07x slower                                                                                                 |
| pprint_pformat             | 1.88 sec                                                                                                          | 2.01 sec: 1.07x slower                                                                                                |
| async_generators           | 479 ms                                                                                                            | 518 ms: 1.08x slower                                                                                                  |
| 2to3                       | 404 ms                                                                                                            | 437 ms: 1.08x slower                                                                                                  |
| thrift                     | 965 us                                                                                                            | 1.06 ms: 1.10x slower                                                                                                 |
| create_gc_cycles           | 3.29 ms                                                                                                           | 3.62 ms: 1.10x slower                                                                                                 |
| comprehensions             | 20.9 us                                                                                                           | 23.0 us: 1.10x slower                                                                                                 |
| sqlalchemy_imperative      | 21.9 ms                                                                                                           | 24.2 ms: 1.10x slower                                                                                                 |
| hexiom                     | 8.50 ms                                                                                                           | 9.43 ms: 1.11x slower                                                                                                 |
| regex_effbot               | 3.99 ms                                                                                                           | 4.50 ms: 1.13x slower                                                                                                 |
| many_optionals             | 1.18 ms                                                                                                           | 1.34 ms: 1.14x slower                                                                                                 |
| genshi_xml                 | 63.7 ms                                                                                                           | 73.1 ms: 1.15x slower                                                                                                 |
| unpack_sequence            | 62.7 ns                                                                                                           | 72.2 ns: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 68.6 ms                                                                                                           | 80.7 ms: 1.18x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (40): unpickle_pure_python, mako, spectral_norm, python_startup, async_tree_none, sympy_integrate, scimark_sparse_mat_mult, sqlglot_v2_parse, python_startup_no_site, fannkuch, json_dumps, asyncio_websockets, xml_etree_process, pidigits, async_tree_none_tg, chaos, json_loads, shortest_path, scimark_lu, bpe_tokeniser, sqlite_synth, telco, bench_thread_pool, scimark_sor, sqlglot_v2_normalize, gc_traversal, asyncio_tcp_ssl, deepcopy, pyflate, async_tree_io, connected_components, sympy_sum, async_tree_io_tg, k_core, async_tree_memoization, regex_v8, bench_mp_pool, xml_etree_generate, pylint, raytrace

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 98.20% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x