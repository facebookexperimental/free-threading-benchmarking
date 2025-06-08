# Results vs. base

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.004x slower
- HPT reliability: 79.69%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 113 ms                                                                                                            | 113 ms: 1.00x slower                                                                                                  |
| docutils       | 1.03 sec                                                                                                          | 1.04 sec: 1.01x slower                                                                                                |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io                    | 254 ms                                                                                                            | 247 ms: 1.03x faster                                                                                                  |
| async_tree_none                  | 110 ms                                                                                                            | 108 ms: 1.02x faster                                                                                                  |
| async_tree_eager_io              | 248 ms                                                                                                            | 242 ms: 1.02x faster                                                                                                  |
| async_tree_eager_tg              | 87.7 ms                                                                                                           | 86.1 ms: 1.02x faster                                                                                                 |
| async_tree_cpu_io_mixed          | 264 ms                                                                                                            | 261 ms: 1.01x faster                                                                                                  |
| async_tree_eager                 | 42.1 ms                                                                                                           | 41.5 ms: 1.01x faster                                                                                                 |
| async_tree_none_tg               | 105 ms                                                                                                            | 104 ms: 1.01x faster                                                                                                  |
| async_tree_io_tg                 | 251 ms                                                                                                            | 248 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                                                            | 245 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                                                            | 220 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 262 ms                                                                                                            | 259 ms: 1.01x faster                                                                                                  |
| asyncio_websockets               | 191 ms                                                                                                            | 190 ms: 1.01x faster                                                                                                  |
| async_tree_memoization           | 146 ms                                                                                                            | 145 ms: 1.00x faster                                                                                                  |
| async_generators                 | 172 ms                                                                                                            | 180 ms: 1.05x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (7): asyncio_tcp_ssl, async_tree_eager_memoization_tg, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_eager_io_tg, coroutines, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 29.7 ms                                                                                                           | 30.7 ms: 1.03x slower                                                                                                 |
| nbody          | 46.9 ms                                                                                                           | 48.8 ms: 1.04x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 47.5 ms                                                                                                           | 47.9 ms: 1.01x slower                                                                                                 |
| regex_dna      | 95.8 ms                                                                                                           | 96.8 ms: 1.01x slower                                                                                                 |
| regex_effbot   | 1.44 ms                                                                                                           | 1.45 ms: 1.01x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 928 ms                                                                                                            | 846 ms: 1.10x faster                                                                                                  |
| xml_etree_process    | 25.1 ms                                                                                                           | 23.2 ms: 1.08x faster                                                                                                 |
| xml_etree_generate   | 35.5 ms                                                                                                           | 33.7 ms: 1.05x faster                                                                                                 |
| unpickle_pure_python | 95.3 us                                                                                                           | 93.4 us: 1.02x faster                                                                                                 |
| pickle_pure_python   | 143 us                                                                                                            | 141 us: 1.02x faster                                                                                                  |
| json_dumps           | 4.44 ms                                                                                                           | 4.38 ms: 1.01x faster                                                                                                 |
| pickle_list          | 2.15 us                                                                                                           | 2.14 us: 1.01x faster                                                                                                 |
| unpickle_list        | 1.97 us                                                                                                           | 1.96 us: 1.00x faster                                                                                                 |
| pickle               | 5.95 us                                                                                                           | 5.99 us: 1.01x slower                                                                                                 |
| unpickle             | 6.23 us                                                                                                           | 6.32 us: 1.01x slower                                                                                                 |
| xml_etree_iterparse  | 43.9 ms                                                                                                           | 44.7 ms: 1.02x slower                                                                                                 |
| xml_etree_parse      | 60.6 ms                                                                                                           | 63.4 ms: 1.05x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (2): pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.10 ms                                                                                                           | 6.12 ms: 1.00x slower                                                                                                 |
| python_startup         | 8.52 ms                                                                                                           | 8.54 ms: 1.00x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako           | 4.90 ms                                                                                                           | 4.35 ms: 1.13x faster                                                                                                 |
| genshi_text    | 9.86 ms                                                                                                           | 9.81 ms: 1.01x faster                                                                                                 |
| genshi_xml     | 21.4 ms                                                                                                           | 21.6 ms: 1.01x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json | results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako                             | 4.90 ms                                                                                                           | 4.35 ms: 1.13x faster                                                                                                 |
| tomli_loads                      | 928 ms                                                                                                            | 846 ms: 1.10x faster                                                                                                  |
| xml_etree_process                | 25.1 ms                                                                                                           | 23.2 ms: 1.08x faster                                                                                                 |
| pprint_safe_repr                 | 351 ms                                                                                                            | 328 ms: 1.07x faster                                                                                                  |
| pprint_pformat                   | 710 ms                                                                                                            | 667 ms: 1.06x faster                                                                                                  |
| xml_etree_generate               | 35.5 ms                                                                                                           | 33.7 ms: 1.05x faster                                                                                                 |
| async_tree_io                    | 254 ms                                                                                                            | 247 ms: 1.03x faster                                                                                                  |
| async_tree_none                  | 110 ms                                                                                                            | 108 ms: 1.02x faster                                                                                                  |
| async_tree_eager_io              | 248 ms                                                                                                            | 242 ms: 1.02x faster                                                                                                  |
| unpickle_pure_python             | 95.3 us                                                                                                           | 93.4 us: 1.02x faster                                                                                                 |
| telco                            | 2.99 ms                                                                                                           | 2.94 ms: 1.02x faster                                                                                                 |
| pickle_pure_python               | 143 us                                                                                                            | 141 us: 1.02x faster                                                                                                  |
| async_tree_eager_tg              | 87.7 ms                                                                                                           | 86.1 ms: 1.02x faster                                                                                                 |
| fannkuch                         | 176 ms                                                                                                            | 173 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed          | 264 ms                                                                                                            | 261 ms: 1.01x faster                                                                                                  |
| subparsers                       | 9.57 ms                                                                                                           | 9.43 ms: 1.01x faster                                                                                                 |
| async_tree_eager                 | 42.1 ms                                                                                                           | 41.5 ms: 1.01x faster                                                                                                 |
| async_tree_none_tg               | 105 ms                                                                                                            | 104 ms: 1.01x faster                                                                                                  |
| json_dumps                       | 4.44 ms                                                                                                           | 4.38 ms: 1.01x faster                                                                                                 |
| comprehensions                   | 7.41 us                                                                                                           | 7.32 us: 1.01x faster                                                                                                 |
| async_tree_io_tg                 | 251 ms                                                                                                            | 248 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 248 ms                                                                                                            | 245 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                                                            | 220 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 262 ms                                                                                                            | 259 ms: 1.01x faster                                                                                                  |
| pyflate                          | 192 ms                                                                                                            | 190 ms: 1.01x faster                                                                                                  |
| sqlite_synth                     | 944 ns                                                                                                            | 938 ns: 1.01x faster                                                                                                  |
| pickle_list                      | 2.15 us                                                                                                           | 2.14 us: 1.01x faster                                                                                                 |
| create_gc_cycles                 | 916 us                                                                                                            | 910 us: 1.01x faster                                                                                                  |
| asyncio_websockets               | 191 ms                                                                                                            | 190 ms: 1.01x faster                                                                                                  |
| genshi_text                      | 9.86 ms                                                                                                           | 9.81 ms: 1.01x faster                                                                                                 |
| sqlglot_v2_optimize              | 23.1 ms                                                                                                           | 22.9 ms: 1.00x faster                                                                                                 |
| async_tree_memoization           | 146 ms                                                                                                            | 145 ms: 1.00x faster                                                                                                  |
| bench_mp_pool                    | 43.5 ms                                                                                                           | 43.3 ms: 1.00x faster                                                                                                 |
| unpickle_list                    | 1.97 us                                                                                                           | 1.96 us: 1.00x faster                                                                                                 |
| python_startup_no_site           | 6.10 ms                                                                                                           | 6.12 ms: 1.00x slower                                                                                                 |
| python_startup                   | 8.52 ms                                                                                                           | 8.54 ms: 1.00x slower                                                                                                 |
| 2to3                             | 113 ms                                                                                                            | 113 ms: 1.00x slower                                                                                                  |
| sympy_sum                        | 54.9 ms                                                                                                           | 55.1 ms: 1.00x slower                                                                                                 |
| raytrace                         | 117 ms                                                                                                            | 118 ms: 1.00x slower                                                                                                  |
| docutils                         | 1.03 sec                                                                                                          | 1.04 sec: 1.01x slower                                                                                                |
| dulwich_log                      | 17.6 ms                                                                                                           | 17.7 ms: 1.01x slower                                                                                                 |
| pickle                           | 5.95 us                                                                                                           | 5.99 us: 1.01x slower                                                                                                 |
| bench_thread_pool                | 431 us                                                                                                            | 434 us: 1.01x slower                                                                                                  |
| generators                       | 17.3 ms                                                                                                           | 17.4 ms: 1.01x slower                                                                                                 |
| genshi_xml                       | 21.4 ms                                                                                                           | 21.6 ms: 1.01x slower                                                                                                 |
| pathlib                          | 11.0 ms                                                                                                           | 11.0 ms: 1.01x slower                                                                                                 |
| regex_compile                    | 47.5 ms                                                                                                           | 47.9 ms: 1.01x slower                                                                                                 |
| deepcopy                         | 108 us                                                                                                            | 109 us: 1.01x slower                                                                                                  |
| typing_runtime_protocols         | 61.9 us                                                                                                           | 62.5 us: 1.01x slower                                                                                                 |
| regex_dna                        | 95.8 ms                                                                                                           | 96.8 ms: 1.01x slower                                                                                                 |
| regex_effbot                     | 1.44 ms                                                                                                           | 1.45 ms: 1.01x slower                                                                                                 |
| mdp                              | 508 ms                                                                                                            | 513 ms: 1.01x slower                                                                                                  |
| nqueens                          | 38.7 ms                                                                                                           | 39.2 ms: 1.01x slower                                                                                                 |
| scimark_monte_carlo              | 28.8 ms                                                                                                           | 29.2 ms: 1.01x slower                                                                                                 |
| meteor_contest                   | 47.7 ms                                                                                                           | 48.4 ms: 1.01x slower                                                                                                 |
| sympy_str                        | 97.5 ms                                                                                                           | 99.0 ms: 1.01x slower                                                                                                 |
| unpickle                         | 6.23 us                                                                                                           | 6.32 us: 1.01x slower                                                                                                 |
| sqlglot_v2_parse                 | 545 us                                                                                                            | 554 us: 1.02x slower                                                                                                  |
| richards_super                   | 24.2 ms                                                                                                           | 24.6 ms: 1.02x slower                                                                                                 |
| spectral_norm                    | 45.4 ms                                                                                                           | 46.2 ms: 1.02x slower                                                                                                 |
| scimark_sor                      | 49.8 ms                                                                                                           | 50.7 ms: 1.02x slower                                                                                                 |
| bpe_tokeniser                    | 1.95 sec                                                                                                          | 1.98 sec: 1.02x slower                                                                                                |
| sqlglot_v2_transpile             | 668 us                                                                                                            | 681 us: 1.02x slower                                                                                                  |
| xml_etree_iterparse              | 43.9 ms                                                                                                           | 44.7 ms: 1.02x slower                                                                                                 |
| sympy_expand                     | 165 ms                                                                                                            | 169 ms: 1.02x slower                                                                                                  |
| scimark_lu                       | 47.0 ms                                                                                                           | 48.1 ms: 1.02x slower                                                                                                 |
| chaos                            | 26.1 ms                                                                                                           | 26.7 ms: 1.02x slower                                                                                                 |
| sympy_integrate                  | 7.30 ms                                                                                                           | 7.48 ms: 1.02x slower                                                                                                 |
| richards                         | 21.2 ms                                                                                                           | 21.8 ms: 1.03x slower                                                                                                 |
| pycparser                        | 485 ms                                                                                                            | 499 ms: 1.03x slower                                                                                                  |
| logging_simple                   | 2.50 us                                                                                                           | 2.57 us: 1.03x slower                                                                                                 |
| hexiom                           | 2.73 ms                                                                                                           | 2.82 ms: 1.03x slower                                                                                                 |
| float                            | 29.7 ms                                                                                                           | 30.7 ms: 1.03x slower                                                                                                 |
| k_core                           | 950 ms                                                                                                            | 986 ms: 1.04x slower                                                                                                  |
| logging_format                   | 2.71 us                                                                                                           | 2.82 us: 1.04x slower                                                                                                 |
| nbody                            | 46.9 ms                                                                                                           | 48.8 ms: 1.04x slower                                                                                                 |
| crypto_pyaes                     | 37.2 ms                                                                                                           | 38.7 ms: 1.04x slower                                                                                                 |
| go                               | 55.1 ms                                                                                                           | 57.4 ms: 1.04x slower                                                                                                 |
| xml_etree_parse                  | 60.6 ms                                                                                                           | 63.4 ms: 1.05x slower                                                                                                 |
| async_generators                 | 172 ms                                                                                                            | 180 ms: 1.05x slower                                                                                                  |
| scimark_fft                      | 129 ms                                                                                                            | 137 ms: 1.06x slower                                                                                                  |
| connected_components             | 202 ms                                                                                                            | 215 ms: 1.07x slower                                                                                                  |
| shortest_path                    | 218 ms                                                                                                            | 233 ms: 1.07x slower                                                                                                  |
| deepcopy_memo                    | 12.3 us                                                                                                           | 13.2 us: 1.07x slower                                                                                                 |
| deltablue                        | 1.51 ms                                                                                                           | 1.65 ms: 1.09x slower                                                                                                 |
| scimark_sparse_mat_mult          | 1.83 ms                                                                                                           | 2.09 ms: 1.14x slower                                                                                                 |
| unpack_sequence                  | 30.1 ns                                                                                                           | 36.5 ns: 1.21x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (24): asyncio_tcp_ssl, json, async_tree_eager_memoization_tg, async_tree_eager_memoization, regex_v8, django_template, coverage, deepcopy_reduce, logging_silent, async_tree_memoization_tg, gc_traversal, async_tree_eager_io_tg, pidigits, dask, many_optionals, coroutines, pickle_dict, sqlglot_v2_normalize, sphinx, json_loads, thrift, html5lib, asyncio_tcp, pylint

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 79.69% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x