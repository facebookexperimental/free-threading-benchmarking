# Results vs. base

- fork: python
- ref: 98b4cd6fe9348ac24d5c
- machine: darwin-arm64
- commit hash: 98b4cd6
- commit date: 2025-09-02
- overall geometric mean: 1.022x slower
- HPT reliability: 99.71%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 117 ms                                                                                                            | 124 ms: 1.06x slower                                                                                                    |
| docutils       | 1.06 sec                                                                                                          | 1.00 sec: 1.06x faster                                                                                                  |
| html5lib       | 24.4 ms                                                                                                           | 23.8 ms: 1.02x faster                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg                 | 253 ms                                                                                                            | 201 ms: 1.26x faster                                                                                                    |
| async_tree_eager_io_tg           | 250 ms                                                                                                            | 198 ms: 1.26x faster                                                                                                    |
| async_tree_eager_io              | 252 ms                                                                                                            | 207 ms: 1.22x faster                                                                                                    |
| async_tree_io                    | 254 ms                                                                                                            | 212 ms: 1.20x faster                                                                                                    |
| async_tree_none_tg               | 106 ms                                                                                                            | 88.3 ms: 1.20x faster                                                                                                   |
| async_tree_memoization_tg        | 148 ms                                                                                                            | 125 ms: 1.19x faster                                                                                                    |
| async_tree_eager_memoization_tg  | 130 ms                                                                                                            | 113 ms: 1.15x faster                                                                                                    |
| async_tree_memoization           | 150 ms                                                                                                            | 131 ms: 1.14x faster                                                                                                    |
| async_tree_none                  | 114 ms                                                                                                            | 102 ms: 1.12x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg       | 262 ms                                                                                                            | 237 ms: 1.11x faster                                                                                                    |
| async_tree_eager_tg              | 86.8 ms                                                                                                           | 79.1 ms: 1.10x faster                                                                                                   |
| async_tree_cpu_io_mixed          | 265 ms                                                                                                            | 244 ms: 1.08x faster                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 247 ms                                                                                                            | 228 ms: 1.08x faster                                                                                                    |
| asyncio_websockets               | 193 ms                                                                                                            | 188 ms: 1.03x faster                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 222 ms                                                                                                            | 224 ms: 1.01x slower                                                                                                    |
| async_generators                 | 176 ms                                                                                                            | 182 ms: 1.04x slower                                                                                                    |
| coroutines                       | 9.97 ms                                                                                                           | 11.0 ms: 1.11x slower                                                                                                   |
| async_tree_eager                 | 41.8 ms                                                                                                           | 49.5 ms: 1.18x slower                                                                                                   |
| Geometric mean                   | (ref)                                                                                                             | 1.09x faster                                                                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 168 ms                                                                                                            | 166 ms: 1.01x faster                                                                                                    |
| nbody          | 47.6 ms                                                                                                           | 58.0 ms: 1.22x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 10.0 ms                                                                                                           | 9.36 ms: 1.07x faster                                                                                                   |
| regex_compile  | 48.8 ms                                                                                                           | 53.6 ms: 1.10x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 43.9 ms                                                                                                           | 38.6 ms: 1.14x faster                                                                                                   |
| xml_etree_parse      | 62.8 ms                                                                                                           | 60.1 ms: 1.04x faster                                                                                                   |
| json_loads           | 11.2 us                                                                                                           | 11.4 us: 1.02x slower                                                                                                   |
| xml_etree_generate   | 35.4 ms                                                                                                           | 37.1 ms: 1.05x slower                                                                                                   |
| tomli_loads          | 916 ms                                                                                                            | 975 ms: 1.06x slower                                                                                                    |
| json_dumps           | 3.81 ms                                                                                                           | 4.06 ms: 1.07x slower                                                                                                   |
| pickle_pure_python   | 147 us                                                                                                            | 157 us: 1.07x slower                                                                                                    |
| xml_etree_process    | 25.0 ms                                                                                                           | 27.4 ms: 1.09x slower                                                                                                   |
| unpickle_pure_python | 98.5 us                                                                                                           | 112 us: 1.14x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.83 ms                                                                                                           | 9.67 ms: 1.10x slower                                                                                                   |
| python_startup_no_site | 6.31 ms                                                                                                           | 7.02 ms: 1.11x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 15.5 ms                                                                                                           | 16.6 ms: 1.07x slower                                                                                                   |
| genshi_xml      | 21.9 ms                                                                                                           | 24.5 ms: 1.12x slower                                                                                                   |
| genshi_text     | 9.97 ms                                                                                                           | 11.8 ms: 1.19x slower                                                                                                   |
| mako            | 4.89 ms                                                                                                           | 5.90 ms: 1.21x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.15x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                        | results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json | results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal                     | 2.09 ms                                                                                                           | 779 us: 2.69x faster                                                                                                    |
| create_gc_cycles                 | 943 us                                                                                                            | 479 us: 1.97x faster                                                                                                    |
| async_tree_io_tg                 | 253 ms                                                                                                            | 201 ms: 1.26x faster                                                                                                    |
| async_tree_eager_io_tg           | 250 ms                                                                                                            | 198 ms: 1.26x faster                                                                                                    |
| async_tree_eager_io              | 252 ms                                                                                                            | 207 ms: 1.22x faster                                                                                                    |
| async_tree_io                    | 254 ms                                                                                                            | 212 ms: 1.20x faster                                                                                                    |
| async_tree_none_tg               | 106 ms                                                                                                            | 88.3 ms: 1.20x faster                                                                                                   |
| async_tree_memoization_tg        | 148 ms                                                                                                            | 125 ms: 1.19x faster                                                                                                    |
| async_tree_eager_memoization_tg  | 130 ms                                                                                                            | 113 ms: 1.15x faster                                                                                                    |
| sqlite_synth                     | 953 ns                                                                                                            | 828 ns: 1.15x faster                                                                                                    |
| async_tree_memoization           | 150 ms                                                                                                            | 131 ms: 1.14x faster                                                                                                    |
| xml_etree_iterparse              | 43.9 ms                                                                                                           | 38.6 ms: 1.14x faster                                                                                                   |
| async_tree_none                  | 114 ms                                                                                                            | 102 ms: 1.12x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg       | 262 ms                                                                                                            | 237 ms: 1.11x faster                                                                                                    |
| async_tree_eager_tg              | 86.8 ms                                                                                                           | 79.1 ms: 1.10x faster                                                                                                   |
| async_tree_cpu_io_mixed          | 265 ms                                                                                                            | 244 ms: 1.08x faster                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 247 ms                                                                                                            | 228 ms: 1.08x faster                                                                                                    |
| regex_v8                         | 10.0 ms                                                                                                           | 9.36 ms: 1.07x faster                                                                                                   |
| docutils                         | 1.06 sec                                                                                                          | 1.00 sec: 1.06x faster                                                                                                  |
| pycparser                        | 496 ms                                                                                                            | 474 ms: 1.05x faster                                                                                                    |
| xml_etree_parse                  | 62.8 ms                                                                                                           | 60.1 ms: 1.04x faster                                                                                                   |
| asyncio_websockets               | 193 ms                                                                                                            | 188 ms: 1.03x faster                                                                                                    |
| html5lib                         | 24.4 ms                                                                                                           | 23.8 ms: 1.02x faster                                                                                                   |
| pidigits                         | 168 ms                                                                                                            | 166 ms: 1.01x faster                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 222 ms                                                                                                            | 224 ms: 1.01x slower                                                                                                    |
| bpe_tokeniser                    | 1.99 sec                                                                                                          | 2.01 sec: 1.01x slower                                                                                                  |
| dask                             | 522 ms                                                                                                            | 528 ms: 1.01x slower                                                                                                    |
| json_loads                       | 11.2 us                                                                                                           | 11.4 us: 1.02x slower                                                                                                   |
| pyflate                          | 198 ms                                                                                                            | 203 ms: 1.02x slower                                                                                                    |
| many_optionals                   | 327 us                                                                                                            | 336 us: 1.03x slower                                                                                                    |
| async_generators                 | 176 ms                                                                                                            | 182 ms: 1.04x slower                                                                                                    |
| pylint                           | 115 ms                                                                                                            | 119 ms: 1.04x slower                                                                                                    |
| dulwich_log                      | 18.2 ms                                                                                                           | 19.0 ms: 1.04x slower                                                                                                   |
| fannkuch                         | 178 ms                                                                                                            | 186 ms: 1.05x slower                                                                                                    |
| k_core                           | 953 ms                                                                                                            | 997 ms: 1.05x slower                                                                                                    |
| xml_etree_generate               | 35.4 ms                                                                                                           | 37.1 ms: 1.05x slower                                                                                                   |
| subparsers                       | 17.5 ms                                                                                                           | 18.5 ms: 1.06x slower                                                                                                   |
| pprint_safe_repr                 | 330 ms                                                                                                            | 348 ms: 1.06x slower                                                                                                    |
| 2to3                             | 117 ms                                                                                                            | 124 ms: 1.06x slower                                                                                                    |
| tomli_loads                      | 916 ms                                                                                                            | 975 ms: 1.06x slower                                                                                                    |
| pprint_pformat                   | 666 ms                                                                                                            | 708 ms: 1.06x slower                                                                                                    |
| json_dumps                       | 3.81 ms                                                                                                           | 4.06 ms: 1.07x slower                                                                                                   |
| generators                       | 18.0 ms                                                                                                           | 19.2 ms: 1.07x slower                                                                                                   |
| sqlglot_v2_normalize             | 47.2 ms                                                                                                           | 50.4 ms: 1.07x slower                                                                                                   |
| pickle_pure_python               | 147 us                                                                                                            | 157 us: 1.07x slower                                                                                                    |
| scimark_fft                      | 133 ms                                                                                                            | 143 ms: 1.07x slower                                                                                                    |
| django_template                  | 15.5 ms                                                                                                           | 16.6 ms: 1.07x slower                                                                                                   |
| thrift                           | 316 us                                                                                                            | 338 us: 1.07x slower                                                                                                    |
| telco                            | 2.79 ms                                                                                                           | 3.00 ms: 1.08x slower                                                                                                   |
| deltablue                        | 1.55 ms                                                                                                           | 1.67 ms: 1.08x slower                                                                                                   |
| sympy_integrate                  | 7.52 ms                                                                                                           | 8.13 ms: 1.08x slower                                                                                                   |
| shortest_path                    | 217 ms                                                                                                            | 235 ms: 1.08x slower                                                                                                    |
| sqlglot_v2_optimize              | 23.0 ms                                                                                                           | 24.9 ms: 1.08x slower                                                                                                   |
| logging_simple                   | 2.35 us                                                                                                           | 2.55 us: 1.08x slower                                                                                                   |
| sympy_sum                        | 56.6 ms                                                                                                           | 61.6 ms: 1.09x slower                                                                                                   |
| sqlglot_v2_transpile             | 686 us                                                                                                            | 750 us: 1.09x slower                                                                                                    |
| xml_etree_process                | 25.0 ms                                                                                                           | 27.4 ms: 1.09x slower                                                                                                   |
| python_startup                   | 8.83 ms                                                                                                           | 9.67 ms: 1.10x slower                                                                                                   |
| regex_compile                    | 48.8 ms                                                                                                           | 53.6 ms: 1.10x slower                                                                                                   |
| comprehensions                   | 7.63 us                                                                                                           | 8.39 us: 1.10x slower                                                                                                   |
| go                               | 57.1 ms                                                                                                           | 63.1 ms: 1.11x slower                                                                                                   |
| deepcopy                         | 111 us                                                                                                            | 122 us: 1.11x slower                                                                                                    |
| coroutines                       | 9.97 ms                                                                                                           | 11.0 ms: 1.11x slower                                                                                                   |
| deepcopy_memo                    | 12.9 us                                                                                                           | 14.3 us: 1.11x slower                                                                                                   |
| connected_components             | 202 ms                                                                                                            | 223 ms: 1.11x slower                                                                                                    |
| sqlglot_v2_parse                 | 562 us                                                                                                            | 622 us: 1.11x slower                                                                                                    |
| mdp                              | 543 ms                                                                                                            | 602 ms: 1.11x slower                                                                                                    |
| logging_format                   | 2.55 us                                                                                                           | 2.84 us: 1.11x slower                                                                                                   |
| python_startup_no_site           | 6.31 ms                                                                                                           | 7.02 ms: 1.11x slower                                                                                                   |
| logging_silent                   | 40.9 ns                                                                                                           | 45.5 ns: 1.11x slower                                                                                                   |
| chaos                            | 26.6 ms                                                                                                           | 29.8 ms: 1.12x slower                                                                                                   |
| richards                         | 21.5 ms                                                                                                           | 24.1 ms: 1.12x slower                                                                                                   |
| hexiom                           | 2.83 ms                                                                                                           | 3.17 ms: 1.12x slower                                                                                                   |
| nqueens                          | 38.7 ms                                                                                                           | 43.3 ms: 1.12x slower                                                                                                   |
| genshi_xml                       | 21.9 ms                                                                                                           | 24.5 ms: 1.12x slower                                                                                                   |
| scimark_sor                      | 49.6 ms                                                                                                           | 55.7 ms: 1.12x slower                                                                                                   |
| sympy_str                        | 101 ms                                                                                                            | 113 ms: 1.13x slower                                                                                                    |
| richards_super                   | 24.3 ms                                                                                                           | 27.3 ms: 1.13x slower                                                                                                   |
| raytrace                         | 118 ms                                                                                                            | 133 ms: 1.13x slower                                                                                                    |
| deepcopy_reduce                  | 1.14 us                                                                                                           | 1.29 us: 1.13x slower                                                                                                   |
| meteor_contest                   | 50.2 ms                                                                                                           | 56.9 ms: 1.13x slower                                                                                                   |
| sympy_expand                     | 170 ms                                                                                                            | 193 ms: 1.13x slower                                                                                                    |
| unpickle_pure_python             | 98.5 us                                                                                                           | 112 us: 1.14x slower                                                                                                    |
| scimark_sparse_mat_mult          | 1.94 ms                                                                                                           | 2.22 ms: 1.14x slower                                                                                                   |
| scimark_monte_carlo              | 29.9 ms                                                                                                           | 34.2 ms: 1.15x slower                                                                                                   |
| crypto_pyaes                     | 37.3 ms                                                                                                           | 43.7 ms: 1.17x slower                                                                                                   |
| spectral_norm                    | 43.6 ms                                                                                                           | 51.4 ms: 1.18x slower                                                                                                   |
| coverage                         | 33.7 ms                                                                                                           | 39.8 ms: 1.18x slower                                                                                                   |
| async_tree_eager                 | 41.8 ms                                                                                                           | 49.5 ms: 1.18x slower                                                                                                   |
| genshi_text                      | 9.97 ms                                                                                                           | 11.8 ms: 1.19x slower                                                                                                   |
| scimark_lu                       | 48.3 ms                                                                                                           | 57.8 ms: 1.20x slower                                                                                                   |
| mako                             | 4.89 ms                                                                                                           | 5.90 ms: 1.21x slower                                                                                                   |
| typing_runtime_protocols         | 62.7 us                                                                                                           | 75.9 us: 1.21x slower                                                                                                   |
| nbody                            | 47.6 ms                                                                                                           | 58.0 ms: 1.22x slower                                                                                                   |
| bench_thread_pool                | 427 us                                                                                                            | 592 us: 1.39x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (8): async_tree_eager_memoization, regex_effbot, float, regex_dna, bench_mp_pool, pathlib, json, sphinx

- Geometric mean (including insignificant results): 1.022x slower

# HPT report

- Reliability score: 99.71% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x