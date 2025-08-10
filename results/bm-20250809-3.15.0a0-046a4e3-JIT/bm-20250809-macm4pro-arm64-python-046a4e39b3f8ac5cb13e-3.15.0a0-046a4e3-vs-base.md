# Results vs. base

- fork: python
- ref: 046a4e39b3f8ac5cb13e
- machine: darwin-arm64
- commit hash: 046a4e3
- commit date: 2025-08-09
- overall geometric mean: 1.012x faster
- HPT reliability: 96.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                                                            | 117 ms: 1.03x slower                                                                                                  |
| docutils       | 1.04 sec                                                                                                          | 1.05 sec: 1.01x slower                                                                                                |
| html5lib       | 24.6 ms                                                                                                           | 24.1 ms: 1.02x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none                  | 113 ms                                                                                                            | 109 ms: 1.04x faster                                                                                                  |
| async_tree_eager                 | 42.5 ms                                                                                                           | 41.6 ms: 1.02x faster                                                                                                 |
| async_tree_none_tg               | 107 ms                                                                                                            | 105 ms: 1.02x faster                                                                                                  |
| async_tree_eager_tg              | 87.7 ms                                                                                                           | 86.8 ms: 1.01x faster                                                                                                 |
| async_tree_memoization           | 147 ms                                                                                                            | 146 ms: 1.01x faster                                                                                                  |
| coroutines                       | 9.96 ms                                                                                                           | 9.90 ms: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed    | 221 ms                                                                                                            | 223 ms: 1.01x slower                                                                                                  |
| asyncio_websockets               | 190 ms                                                                                                            | 192 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed          | 264 ms                                                                                                            | 266 ms: 1.01x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 247 ms                                                                                                            | 249 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 261 ms                                                                                                            | 265 ms: 1.01x slower                                                                                                  |
| asyncio_tcp_ssl                  | 674 ms                                                                                                            | 701 ms: 1.04x slower                                                                                                  |
| async_generators                 | 173 ms                                                                                                            | 184 ms: 1.06x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (8): async_tree_io, async_tree_eager_io, async_tree_eager_io_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 31.6 ms                                                                                                           | 31.1 ms: 1.02x faster                                                                                                 |
| pidigits       | 164 ms                                                                                                            | 165 ms: 1.00x slower                                                                                                  |
| nbody          | 51.4 ms                                                                                                           | 56.8 ms: 1.11x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 49.7 ms                                                                                                           | 47.9 ms: 1.04x faster                                                                                                 |
| regex_dna      | 97.6 ms                                                                                                           | 96.4 ms: 1.01x faster                                                                                                 |
| regex_v8       | 9.72 ms                                                                                                           | 9.66 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 968 ms                                                                                                            | 822 ms: 1.18x faster                                                                                                  |
| xml_etree_process    | 26.1 ms                                                                                                           | 23.6 ms: 1.11x faster                                                                                                 |
| unpickle_pure_python | 102 us                                                                                                            | 92.4 us: 1.11x faster                                                                                                 |
| xml_etree_generate   | 36.7 ms                                                                                                           | 33.8 ms: 1.09x faster                                                                                                 |
| pickle_pure_python   | 148 us                                                                                                            | 141 us: 1.05x faster                                                                                                  |
| json_dumps           | 3.85 ms                                                                                                           | 3.78 ms: 1.02x faster                                                                                                 |
| unpickle_list        | 2.06 us                                                                                                           | 2.04 us: 1.01x faster                                                                                                 |
| xml_etree_parse      | 62.6 ms                                                                                                           | 62.1 ms: 1.01x faster                                                                                                 |
| pickle_dict          | 12.9 us                                                                                                           | 13.0 us: 1.01x slower                                                                                                 |
| unpickle             | 6.45 us                                                                                                           | 6.54 us: 1.01x slower                                                                                                 |
| json_loads           | 10.9 us                                                                                                           | 11.1 us: 1.02x slower                                                                                                 |
| xml_etree_iterparse  | 43.2 ms                                                                                                           | 44.2 ms: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (2): pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.20 ms                                                                                                           | 6.24 ms: 1.01x slower                                                                                                 |
| python_startup         | 8.64 ms                                                                                                           | 8.72 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 5.07 ms                                                                                                           | 4.44 ms: 1.14x faster                                                                                                 |
| django_template | 15.9 ms                                                                                                           | 15.3 ms: 1.04x faster                                                                                                 |
| genshi_xml      | 22.2 ms                                                                                                           | 21.8 ms: 1.02x faster                                                                                                 |
| genshi_text     | 10.1 ms                                                                                                           | 9.89 ms: 1.02x faster                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.06x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                        | results/bm-20250809-3.15.0a0-046a4e3/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json | results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads                      | 968 ms                                                                                                            | 822 ms: 1.18x faster                                                                                                  |
| mako                             | 5.07 ms                                                                                                           | 4.44 ms: 1.14x faster                                                                                                 |
| pprint_safe_repr                 | 332 ms                                                                                                            | 293 ms: 1.13x faster                                                                                                  |
| fannkuch                         | 193 ms                                                                                                            | 170 ms: 1.13x faster                                                                                                  |
| pprint_pformat                   | 671 ms                                                                                                            | 595 ms: 1.13x faster                                                                                                  |
| xml_etree_process                | 26.1 ms                                                                                                           | 23.6 ms: 1.11x faster                                                                                                 |
| unpickle_pure_python             | 102 us                                                                                                            | 92.4 us: 1.11x faster                                                                                                 |
| xml_etree_generate               | 36.7 ms                                                                                                           | 33.8 ms: 1.09x faster                                                                                                 |
| scimark_fft                      | 138 ms                                                                                                            | 129 ms: 1.07x faster                                                                                                  |
| telco                            | 3.08 ms                                                                                                           | 2.92 ms: 1.06x faster                                                                                                 |
| pickle_pure_python               | 148 us                                                                                                            | 141 us: 1.05x faster                                                                                                  |
| django_template                  | 15.9 ms                                                                                                           | 15.3 ms: 1.04x faster                                                                                                 |
| pyflate                          | 202 ms                                                                                                            | 194 ms: 1.04x faster                                                                                                  |
| sqlglot_v2_parse                 | 578 us                                                                                                            | 555 us: 1.04x faster                                                                                                  |
| deepcopy_memo                    | 13.4 us                                                                                                           | 12.9 us: 1.04x faster                                                                                                 |
| comprehensions                   | 7.67 us                                                                                                           | 7.38 us: 1.04x faster                                                                                                 |
| scimark_sor                      | 52.8 ms                                                                                                           | 50.9 ms: 1.04x faster                                                                                                 |
| regex_compile                    | 49.7 ms                                                                                                           | 47.9 ms: 1.04x faster                                                                                                 |
| scimark_lu                       | 49.0 ms                                                                                                           | 47.3 ms: 1.04x faster                                                                                                 |
| richards                         | 21.9 ms                                                                                                           | 21.1 ms: 1.04x faster                                                                                                 |
| async_tree_none                  | 113 ms                                                                                                            | 109 ms: 1.04x faster                                                                                                  |
| sqlglot_v2_transpile             | 700 us                                                                                                            | 677 us: 1.03x faster                                                                                                  |
| richards_super                   | 24.6 ms                                                                                                           | 23.9 ms: 1.03x faster                                                                                                 |
| deepcopy                         | 114 us                                                                                                            | 111 us: 1.03x faster                                                                                                  |
| deepcopy_reduce                  | 1.18 us                                                                                                           | 1.15 us: 1.03x faster                                                                                                 |
| logging_silent                   | 41.6 ns                                                                                                           | 40.5 ns: 1.03x faster                                                                                                 |
| chaos                            | 27.3 ms                                                                                                           | 26.7 ms: 1.03x faster                                                                                                 |
| raytrace                         | 121 ms                                                                                                            | 119 ms: 1.02x faster                                                                                                  |
| html5lib                         | 24.6 ms                                                                                                           | 24.1 ms: 1.02x faster                                                                                                 |
| typing_runtime_protocols         | 65.1 us                                                                                                           | 63.7 us: 1.02x faster                                                                                                 |
| genshi_xml                       | 22.2 ms                                                                                                           | 21.8 ms: 1.02x faster                                                                                                 |
| async_tree_eager                 | 42.5 ms                                                                                                           | 41.6 ms: 1.02x faster                                                                                                 |
| genshi_text                      | 10.1 ms                                                                                                           | 9.89 ms: 1.02x faster                                                                                                 |
| json_dumps                       | 3.85 ms                                                                                                           | 3.78 ms: 1.02x faster                                                                                                 |
| spectral_norm                    | 45.1 ms                                                                                                           | 44.3 ms: 1.02x faster                                                                                                 |
| sqlglot_v2_normalize             | 47.1 ms                                                                                                           | 46.3 ms: 1.02x faster                                                                                                 |
| float                            | 31.6 ms                                                                                                           | 31.1 ms: 1.02x faster                                                                                                 |
| async_tree_none_tg               | 107 ms                                                                                                            | 105 ms: 1.02x faster                                                                                                  |
| hexiom                           | 2.87 ms                                                                                                           | 2.83 ms: 1.01x faster                                                                                                 |
| logging_simple                   | 2.41 us                                                                                                           | 2.38 us: 1.01x faster                                                                                                 |
| scimark_monte_carlo              | 31.0 ms                                                                                                           | 30.6 ms: 1.01x faster                                                                                                 |
| meteor_contest                   | 50.1 ms                                                                                                           | 49.4 ms: 1.01x faster                                                                                                 |
| regex_dna                        | 97.6 ms                                                                                                           | 96.4 ms: 1.01x faster                                                                                                 |
| thrift                           | 310 us                                                                                                            | 307 us: 1.01x faster                                                                                                  |
| async_tree_eager_tg              | 87.7 ms                                                                                                           | 86.8 ms: 1.01x faster                                                                                                 |
| unpickle_list                    | 2.06 us                                                                                                           | 2.04 us: 1.01x faster                                                                                                 |
| go                               | 57.8 ms                                                                                                           | 57.3 ms: 1.01x faster                                                                                                 |
| xml_etree_parse                  | 62.6 ms                                                                                                           | 62.1 ms: 1.01x faster                                                                                                 |
| bench_thread_pool                | 439 us                                                                                                            | 436 us: 1.01x faster                                                                                                  |
| dulwich_log                      | 18.2 ms                                                                                                           | 18.1 ms: 1.01x faster                                                                                                 |
| async_tree_memoization           | 147 ms                                                                                                            | 146 ms: 1.01x faster                                                                                                  |
| regex_v8                         | 9.72 ms                                                                                                           | 9.66 ms: 1.01x faster                                                                                                 |
| coroutines                       | 9.96 ms                                                                                                           | 9.90 ms: 1.01x faster                                                                                                 |
| sqlite_synth                     | 954 ns                                                                                                            | 949 ns: 1.01x faster                                                                                                  |
| sympy_sum                        | 56.3 ms                                                                                                           | 56.1 ms: 1.00x faster                                                                                                 |
| bpe_tokeniser                    | 2.00 sec                                                                                                          | 1.99 sec: 1.00x faster                                                                                                |
| pathlib                          | 10.9 ms                                                                                                           | 10.9 ms: 1.00x faster                                                                                                 |
| sqlglot_v2_optimize              | 23.1 ms                                                                                                           | 23.0 ms: 1.00x faster                                                                                                 |
| pidigits                         | 164 ms                                                                                                            | 165 ms: 1.00x slower                                                                                                  |
| sympy_str                        | 101 ms                                                                                                            | 101 ms: 1.01x slower                                                                                                  |
| pickle_dict                      | 12.9 us                                                                                                           | 13.0 us: 1.01x slower                                                                                                 |
| python_startup_no_site           | 6.20 ms                                                                                                           | 6.24 ms: 1.01x slower                                                                                                 |
| crypto_pyaes                     | 37.5 ms                                                                                                           | 37.8 ms: 1.01x slower                                                                                                 |
| async_tree_eager_cpu_io_mixed    | 221 ms                                                                                                            | 223 ms: 1.01x slower                                                                                                  |
| asyncio_websockets               | 190 ms                                                                                                            | 192 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed          | 264 ms                                                                                                            | 266 ms: 1.01x slower                                                                                                  |
| create_gc_cycles                 | 936 us                                                                                                            | 944 us: 1.01x slower                                                                                                  |
| generators                       | 17.5 ms                                                                                                           | 17.6 ms: 1.01x slower                                                                                                 |
| json                             | 1.92 ms                                                                                                           | 1.94 ms: 1.01x slower                                                                                                 |
| python_startup                   | 8.64 ms                                                                                                           | 8.72 ms: 1.01x slower                                                                                                 |
| sympy_expand                     | 170 ms                                                                                                            | 172 ms: 1.01x slower                                                                                                  |
| mdp                              | 536 ms                                                                                                            | 542 ms: 1.01x slower                                                                                                  |
| docutils                         | 1.04 sec                                                                                                          | 1.05 sec: 1.01x slower                                                                                                |
| async_tree_eager_cpu_io_mixed_tg | 247 ms                                                                                                            | 249 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 261 ms                                                                                                            | 265 ms: 1.01x slower                                                                                                  |
| sympy_integrate                  | 7.46 ms                                                                                                           | 7.56 ms: 1.01x slower                                                                                                 |
| unpickle                         | 6.45 us                                                                                                           | 6.54 us: 1.01x slower                                                                                                 |
| coverage                         | 32.7 ms                                                                                                           | 33.1 ms: 1.01x slower                                                                                                 |
| gc_traversal                     | 2.06 ms                                                                                                           | 2.09 ms: 1.02x slower                                                                                                 |
| bench_mp_pool                    | 43.6 ms                                                                                                           | 44.5 ms: 1.02x slower                                                                                                 |
| json_loads                       | 10.9 us                                                                                                           | 11.1 us: 1.02x slower                                                                                                 |
| xml_etree_iterparse              | 43.2 ms                                                                                                           | 44.2 ms: 1.02x slower                                                                                                 |
| 2to3                             | 114 ms                                                                                                            | 117 ms: 1.03x slower                                                                                                  |
| many_optionals                   | 314 us                                                                                                            | 323 us: 1.03x slower                                                                                                  |
| k_core                           | 958 ms                                                                                                            | 992 ms: 1.04x slower                                                                                                  |
| asyncio_tcp_ssl                  | 674 ms                                                                                                            | 701 ms: 1.04x slower                                                                                                  |
| deltablue                        | 1.56 ms                                                                                                           | 1.66 ms: 1.06x slower                                                                                                 |
| async_generators                 | 173 ms                                                                                                            | 184 ms: 1.06x slower                                                                                                  |
| shortest_path                    | 218 ms                                                                                                            | 234 ms: 1.07x slower                                                                                                  |
| connected_components             | 202 ms                                                                                                            | 218 ms: 1.08x slower                                                                                                  |
| unpack_sequence                  | 31.0 ns                                                                                                           | 33.8 ns: 1.09x slower                                                                                                 |
| nbody                            | 51.4 ms                                                                                                           | 56.8 ms: 1.11x slower                                                                                                 |
| scimark_sparse_mat_mult          | 1.95 ms                                                                                                           | 2.16 ms: 1.11x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (18): pycparser, async_tree_io, async_tree_eager_io, async_tree_eager_io_tg, async_tree_io_tg, pickle, logging_format, async_tree_memoization_tg, sphinx, subparsers, pickle_list, async_tree_eager_memoization, dask, regex_effbot, async_tree_eager_memoization_tg, nqueens, pylint, asyncio_tcp

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 96.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x