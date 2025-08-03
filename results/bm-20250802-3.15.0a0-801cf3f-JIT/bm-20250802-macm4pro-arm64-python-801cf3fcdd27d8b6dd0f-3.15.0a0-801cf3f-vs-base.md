# Results vs. base

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: darwin-arm64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.004x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 113 ms                                                                                                            | 118 ms: 1.04x slower                                                                                                  |
| docutils       | 1.04 sec                                                                                                          | 1.06 sec: 1.01x slower                                                                                                |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_memoization           | 145 ms                                                                                                            | 146 ms: 1.01x slower                                                                                                  |
| async_tree_none                  | 111 ms                                                                                                            | 112 ms: 1.01x slower                                                                                                  |
| asyncio_websockets               | 190 ms                                                                                                            | 192 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 260 ms                                                                                                            | 263 ms: 1.01x slower                                                                                                  |
| async_tree_eager_memoization_tg  | 129 ms                                                                                                            | 131 ms: 1.01x slower                                                                                                  |
| async_tree_eager_memoization     | 109 ms                                                                                                            | 111 ms: 1.01x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                                                            | 223 ms: 1.02x slower                                                                                                  |
| async_tree_cpu_io_mixed          | 261 ms                                                                                                            | 265 ms: 1.02x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                                                            | 249 ms: 1.02x slower                                                                                                  |
| async_tree_eager                 | 41.3 ms                                                                                                           | 42.0 ms: 1.02x slower                                                                                                 |
| coroutines                       | 9.88 ms                                                                                                           | 10.1 ms: 1.02x slower                                                                                                 |
| asyncio_tcp_ssl                  | 673 ms                                                                                                            | 694 ms: 1.03x slower                                                                                                  |
| async_generators                 | 174 ms                                                                                                            | 185 ms: 1.06x slower                                                                                                  |
| asyncio_tcp                      | 184 ms                                                                                                            | 209 ms: 1.14x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_eager_tg, async_tree_io, async_tree_eager_io_tg, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 30.3 ms                                                                                                           | 31.5 ms: 1.04x slower                                                                                                 |
| nbody          | 48.4 ms                                                                                                           | 57.0 ms: 1.18x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 48.7 ms                                                                                                           | 48.0 ms: 1.01x faster                                                                                                 |
| regex_v8       | 9.58 ms                                                                                                           | 9.61 ms: 1.00x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 942 ms                                                                                                            | 823 ms: 1.14x faster                                                                                                  |
| unpickle_pure_python | 100 us                                                                                                            | 92.8 us: 1.08x faster                                                                                                 |
| xml_etree_process    | 25.3 ms                                                                                                           | 24.0 ms: 1.06x faster                                                                                                 |
| json_dumps           | 4.47 ms                                                                                                           | 4.28 ms: 1.04x faster                                                                                                 |
| xml_etree_parse      | 64.3 ms                                                                                                           | 62.1 ms: 1.03x faster                                                                                                 |
| xml_etree_generate   | 35.6 ms                                                                                                           | 34.5 ms: 1.03x faster                                                                                                 |
| pickle_pure_python   | 143 us                                                                                                            | 140 us: 1.02x faster                                                                                                  |
| unpickle_list        | 1.99 us                                                                                                           | 1.98 us: 1.01x faster                                                                                                 |
| xml_etree_iterparse  | 44.6 ms                                                                                                           | 44.3 ms: 1.01x faster                                                                                                 |
| pickle               | 5.95 us                                                                                                           | 5.98 us: 1.00x slower                                                                                                 |
| json_loads           | 10.9 us                                                                                                           | 11.1 us: 1.02x slower                                                                                                 |
| unpickle             | 6.41 us                                                                                                           | 6.54 us: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (2): pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.20 ms                                                                                                           | 6.24 ms: 1.01x slower                                                                                                 |
| python_startup         | 8.65 ms                                                                                                           | 8.72 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 4.92 ms                                                                                                           | 4.43 ms: 1.11x faster                                                                                                 |
| django_template | 15.3 ms                                                                                                           | 15.5 ms: 1.01x slower                                                                                                 |
| genshi_xml      | 21.5 ms                                                                                                           | 21.8 ms: 1.01x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json | results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads                      | 942 ms                                                                                                            | 823 ms: 1.14x faster                                                                                                  |
| mako                             | 4.92 ms                                                                                                           | 4.43 ms: 1.11x faster                                                                                                 |
| pprint_pformat                   | 660 ms                                                                                                            | 599 ms: 1.10x faster                                                                                                  |
| pprint_safe_repr                 | 327 ms                                                                                                            | 297 ms: 1.10x faster                                                                                                  |
| unpickle_pure_python             | 100 us                                                                                                            | 92.8 us: 1.08x faster                                                                                                 |
| fannkuch                         | 181 ms                                                                                                            | 171 ms: 1.06x faster                                                                                                  |
| xml_etree_process                | 25.3 ms                                                                                                           | 24.0 ms: 1.06x faster                                                                                                 |
| json_dumps                       | 4.47 ms                                                                                                           | 4.28 ms: 1.04x faster                                                                                                 |
| telco                            | 3.04 ms                                                                                                           | 2.92 ms: 1.04x faster                                                                                                 |
| spectral_norm                    | 45.3 ms                                                                                                           | 43.5 ms: 1.04x faster                                                                                                 |
| xml_etree_parse                  | 64.3 ms                                                                                                           | 62.1 ms: 1.03x faster                                                                                                 |
| xml_etree_generate               | 35.6 ms                                                                                                           | 34.5 ms: 1.03x faster                                                                                                 |
| scimark_fft                      | 132 ms                                                                                                            | 129 ms: 1.03x faster                                                                                                  |
| scimark_sor                      | 51.1 ms                                                                                                           | 50.0 ms: 1.02x faster                                                                                                 |
| comprehensions                   | 7.45 us                                                                                                           | 7.30 us: 1.02x faster                                                                                                 |
| pickle_pure_python               | 143 us                                                                                                            | 140 us: 1.02x faster                                                                                                  |
| sqlglot_v2_parse                 | 559 us                                                                                                            | 551 us: 1.01x faster                                                                                                  |
| regex_compile                    | 48.7 ms                                                                                                           | 48.0 ms: 1.01x faster                                                                                                 |
| typing_runtime_protocols         | 64.6 us                                                                                                           | 63.8 us: 1.01x faster                                                                                                 |
| sqlite_synth                     | 953 ns                                                                                                            | 941 ns: 1.01x faster                                                                                                  |
| sqlglot_v2_normalize             | 46.9 ms                                                                                                           | 46.4 ms: 1.01x faster                                                                                                 |
| pathlib                          | 11.0 ms                                                                                                           | 10.9 ms: 1.01x faster                                                                                                 |
| unpickle_list                    | 1.99 us                                                                                                           | 1.98 us: 1.01x faster                                                                                                 |
| logging_silent                   | 41.5 ns                                                                                                           | 41.3 ns: 1.01x faster                                                                                                 |
| xml_etree_iterparse              | 44.6 ms                                                                                                           | 44.3 ms: 1.01x faster                                                                                                 |
| regex_v8                         | 9.58 ms                                                                                                           | 9.61 ms: 1.00x slower                                                                                                 |
| pickle                           | 5.95 us                                                                                                           | 5.98 us: 1.00x slower                                                                                                 |
| async_tree_memoization           | 145 ms                                                                                                            | 146 ms: 1.01x slower                                                                                                  |
| async_tree_none                  | 111 ms                                                                                                            | 112 ms: 1.01x slower                                                                                                  |
| meteor_contest                   | 49.1 ms                                                                                                           | 49.4 ms: 1.01x slower                                                                                                 |
| python_startup_no_site           | 6.20 ms                                                                                                           | 6.24 ms: 1.01x slower                                                                                                 |
| dulwich_log                      | 17.9 ms                                                                                                           | 18.0 ms: 1.01x slower                                                                                                 |
| create_gc_cycles                 | 934 us                                                                                                            | 941 us: 1.01x slower                                                                                                  |
| asyncio_websockets               | 190 ms                                                                                                            | 192 ms: 1.01x slower                                                                                                  |
| python_startup                   | 8.65 ms                                                                                                           | 8.72 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg       | 260 ms                                                                                                            | 263 ms: 1.01x slower                                                                                                  |
| crypto_pyaes                     | 37.1 ms                                                                                                           | 37.5 ms: 1.01x slower                                                                                                 |
| deepcopy                         | 110 us                                                                                                            | 111 us: 1.01x slower                                                                                                  |
| async_tree_eager_memoization_tg  | 129 ms                                                                                                            | 131 ms: 1.01x slower                                                                                                  |
| bench_thread_pool                | 433 us                                                                                                            | 438 us: 1.01x slower                                                                                                  |
| raytrace                         | 118 ms                                                                                                            | 119 ms: 1.01x slower                                                                                                  |
| django_template                  | 15.3 ms                                                                                                           | 15.5 ms: 1.01x slower                                                                                                 |
| thrift                           | 308 us                                                                                                            | 311 us: 1.01x slower                                                                                                  |
| bench_mp_pool                    | 43.6 ms                                                                                                           | 44.2 ms: 1.01x slower                                                                                                 |
| docutils                         | 1.04 sec                                                                                                          | 1.06 sec: 1.01x slower                                                                                                |
| async_tree_eager_memoization     | 109 ms                                                                                                            | 111 ms: 1.01x slower                                                                                                  |
| coverage                         | 32.4 ms                                                                                                           | 32.9 ms: 1.01x slower                                                                                                 |
| json                             | 1.90 ms                                                                                                           | 1.93 ms: 1.01x slower                                                                                                 |
| genshi_xml                       | 21.5 ms                                                                                                           | 21.8 ms: 1.01x slower                                                                                                 |
| subparsers                       | 17.1 ms                                                                                                           | 17.3 ms: 1.01x slower                                                                                                 |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                                                            | 223 ms: 1.02x slower                                                                                                  |
| async_tree_cpu_io_mixed          | 261 ms                                                                                                            | 265 ms: 1.02x slower                                                                                                  |
| sympy_str                        | 100 ms                                                                                                            | 102 ms: 1.02x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                                                            | 249 ms: 1.02x slower                                                                                                  |
| hexiom                           | 2.82 ms                                                                                                           | 2.86 ms: 1.02x slower                                                                                                 |
| mdp                              | 532 ms                                                                                                            | 541 ms: 1.02x slower                                                                                                  |
| async_tree_eager                 | 41.3 ms                                                                                                           | 42.0 ms: 1.02x slower                                                                                                 |
| sympy_integrate                  | 7.48 ms                                                                                                           | 7.61 ms: 1.02x slower                                                                                                 |
| json_loads                       | 10.9 us                                                                                                           | 11.1 us: 1.02x slower                                                                                                 |
| gc_traversal                     | 2.05 ms                                                                                                           | 2.09 ms: 1.02x slower                                                                                                 |
| richards_super                   | 24.2 ms                                                                                                           | 24.6 ms: 1.02x slower                                                                                                 |
| bpe_tokeniser                    | 1.96 sec                                                                                                          | 2.00 sec: 1.02x slower                                                                                                |
| unpickle                         | 6.41 us                                                                                                           | 6.54 us: 1.02x slower                                                                                                 |
| sympy_expand                     | 169 ms                                                                                                            | 173 ms: 1.02x slower                                                                                                  |
| coroutines                       | 9.88 ms                                                                                                           | 10.1 ms: 1.02x slower                                                                                                 |
| go                               | 56.1 ms                                                                                                           | 57.5 ms: 1.02x slower                                                                                                 |
| deepcopy_memo                    | 12.7 us                                                                                                           | 13.0 us: 1.02x slower                                                                                                 |
| generators                       | 17.3 ms                                                                                                           | 17.8 ms: 1.03x slower                                                                                                 |
| chaos                            | 26.1 ms                                                                                                           | 26.9 ms: 1.03x slower                                                                                                 |
| asyncio_tcp_ssl                  | 673 ms                                                                                                            | 694 ms: 1.03x slower                                                                                                  |
| richards                         | 21.3 ms                                                                                                           | 22.0 ms: 1.03x slower                                                                                                 |
| k_core                           | 956 ms                                                                                                            | 990 ms: 1.04x slower                                                                                                  |
| float                            | 30.3 ms                                                                                                           | 31.5 ms: 1.04x slower                                                                                                 |
| 2to3                             | 113 ms                                                                                                            | 118 ms: 1.04x slower                                                                                                  |
| scimark_monte_carlo              | 29.7 ms                                                                                                           | 30.9 ms: 1.04x slower                                                                                                 |
| nqueens                          | 38.1 ms                                                                                                           | 39.7 ms: 1.04x slower                                                                                                 |
| many_optionals                   | 311 us                                                                                                            | 324 us: 1.04x slower                                                                                                  |
| async_generators                 | 174 ms                                                                                                            | 185 ms: 1.06x slower                                                                                                  |
| connected_components             | 201 ms                                                                                                            | 216 ms: 1.08x slower                                                                                                  |
| shortest_path                    | 217 ms                                                                                                            | 234 ms: 1.08x slower                                                                                                  |
| deltablue                        | 1.52 ms                                                                                                           | 1.66 ms: 1.09x slower                                                                                                 |
| unpack_sequence                  | 30.0 ns                                                                                                           | 32.9 ns: 1.10x slower                                                                                                 |
| scimark_sparse_mat_mult          | 1.90 ms                                                                                                           | 2.13 ms: 1.12x slower                                                                                                 |
| asyncio_tcp                      | 184 ms                                                                                                            | 209 ms: 1.14x slower                                                                                                  |
| nbody                            | 48.4 ms                                                                                                           | 57.0 ms: 1.18x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (26): pickle_list, regex_effbot, sqlglot_v2_transpile, pyflate, regex_dna, sqlglot_v2_optimize, scimark_lu, deepcopy_reduce, html5lib, dask, sphinx, pickle_dict, pidigits, async_tree_io_tg, async_tree_none_tg, genshi_text, sympy_sum, logging_simple, logging_format, async_tree_memoization_tg, async_tree_eager_tg, async_tree_io, async_tree_eager_io_tg, pycparser, async_tree_eager_io, pylint

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.03x