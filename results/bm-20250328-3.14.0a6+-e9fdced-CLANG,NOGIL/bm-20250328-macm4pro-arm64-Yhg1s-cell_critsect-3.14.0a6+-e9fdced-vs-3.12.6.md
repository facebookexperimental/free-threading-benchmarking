# Results vs. 3.12.6

- fork: Yhg1s
- ref: cell_critsect
- machine: darwin-arm64
- commit hash: e9fdced
- commit date: 2025-03-28
- overall geometric mean: 1.136x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                             |
| docutils       | 1.02 sec                                                 | 960 ms: 1.06x faster                                             |
| html5lib       | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                            |
| sphinx         | 434 ms                                                   | 397 ms: 1.09x faster                                             |
| Geometric mean | (ref)                                                    | 1.05x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 188 ms: 2.55x faster                                             |
| async_tree_eager_io              | 496 ms                                                   | 195 ms: 2.54x faster                                             |
| async_tree_eager_io_tg           | 446 ms                                                   | 183 ms: 2.43x faster                                             |
| async_tree_io                    | 459 ms                                                   | 203 ms: 2.26x faster                                             |
| async_tree_none_tg               | 172 ms                                                   | 82.2 ms: 2.09x faster                                            |
| async_tree_memoization_tg        | 231 ms                                                   | 120 ms: 1.92x faster                                             |
| async_tree_none                  | 178 ms                                                   | 98.1 ms: 1.82x faster                                            |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                             |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 226 ms: 1.49x faster                                             |
| coroutines                       | 13.6 ms                                                  | 9.09 ms: 1.49x faster                                            |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 236 ms: 1.41x faster                                             |
| async_generators                 | 206 ms                                                   | 166 ms: 1.25x faster                                             |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                             |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                             |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 109 ms: 1.03x faster                                             |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                             |
| async_tree_eager                 | 45.6 ms                                                  | 46.2 ms: 1.01x slower                                            |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 218 ms: 1.02x slower                                             |
| async_tree_eager_tg              | 32.1 ms                                                  | 73.7 ms: 2.29x slower                                            |
| Geometric mean                   | (ref)                                                    | 1.44x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                            |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                             |
| nbody          | 54.2 ms                                                  | 59.6 ms: 1.10x slower                                            |
| Geometric mean | (ref)                                                    | 1.07x faster                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                            |
| regex_compile  | 54.6 ms                                                  | 49.1 ms: 1.11x faster                                            |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.01x slower                                             |
| regex_v8       | 9.59 ms                                                  | 9.92 ms: 1.03x slower                                            |
| Geometric mean | (ref)                                                    | 1.05x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 34.8 ms: 1.48x faster                                            |
| xml_etree_parse      | 67.9 ms                                                  | 55.9 ms: 1.21x faster                                            |
| xml_etree_generate   | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                            |
| tomli_loads          | 957 ms                                                   | 884 ms: 1.08x faster                                             |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                            |
| unpickle_pure_python | 103 us                                                   | 98.7 us: 1.04x faster                                            |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                             |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                            |
| json_dumps           | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                            |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.13 ms: 1.14x slower                                            |
| python_startup_no_site | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                            |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                            |
| genshi_text     | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                            |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                            |
| mako            | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                            |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 745 us: 2.70x faster                                             |
| async_tree_io_tg                 | 480 ms                                                   | 188 ms: 2.55x faster                                             |
| async_tree_eager_io              | 496 ms                                                   | 195 ms: 2.54x faster                                             |
| subparsers                       | 20.8 ms                                                  | 8.28 ms: 2.51x faster                                            |
| async_tree_eager_io_tg           | 446 ms                                                   | 183 ms: 2.43x faster                                             |
| async_tree_io                    | 459 ms                                                   | 203 ms: 2.26x faster                                             |
| async_tree_none_tg               | 172 ms                                                   | 82.2 ms: 2.09x faster                                            |
| async_tree_memoization_tg        | 231 ms                                                   | 120 ms: 1.92x faster                                             |
| create_gc_cycles                 | 830 us                                                   | 451 us: 1.84x faster                                             |
| async_tree_none                  | 178 ms                                                   | 98.1 ms: 1.82x faster                                            |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                             |
| generators                       | 21.9 ms                                                  | 13.8 ms: 1.59x faster                                            |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                             |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 226 ms: 1.49x faster                                             |
| coroutines                       | 13.6 ms                                                  | 9.09 ms: 1.49x faster                                            |
| xml_etree_iterparse              | 51.6 ms                                                  | 34.8 ms: 1.48x faster                                            |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 236 ms: 1.41x faster                                             |
| deepcopy_memo                    | 18.3 us                                                  | 13.3 us: 1.38x faster                                            |
| float                            | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                            |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.31x faster                                            |
| async_generators                 | 206 ms                                                   | 166 ms: 1.25x faster                                             |
| comprehensions                   | 9.84 us                                                  | 7.91 us: 1.24x faster                                            |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                             |
| xml_etree_parse                  | 67.9 ms                                                  | 55.9 ms: 1.21x faster                                            |
| sqlite_synth                     | 967 ns                                                   | 806 ns: 1.20x faster                                             |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                            |
| go                               | 70.0 ms                                                  | 58.7 ms: 1.19x faster                                            |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                            |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                           |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                             |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                            |
| raytrace                         | 145 ms                                                   | 129 ms: 1.13x faster                                             |
| xml_etree_generate               | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                            |
| scimark_sor                      | 61.0 ms                                                  | 54.5 ms: 1.12x faster                                            |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                           |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                            |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                            |
| pycparser                        | 497 ms                                                   | 446 ms: 1.11x faster                                             |
| regex_compile                    | 54.6 ms                                                  | 49.1 ms: 1.11x faster                                            |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                             |
| spectral_norm                    | 54.4 ms                                                  | 49.5 ms: 1.10x faster                                            |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                            |
| sphinx                           | 434 ms                                                   | 397 ms: 1.09x faster                                             |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                            |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                            |
| tomli_loads                      | 957 ms                                                   | 884 ms: 1.08x faster                                             |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                             |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                            |
| docutils                         | 1.02 sec                                                 | 960 ms: 1.06x faster                                             |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                            |
| hexiom                           | 3.04 ms                                                  | 2.91 ms: 1.04x faster                                            |
| unpickle_pure_python             | 103 us                                                   | 98.7 us: 1.04x faster                                            |
| html5lib                         | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                            |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 109 ms: 1.03x faster                                             |
| typing_runtime_protocols         | 71.0 us                                                  | 68.8 us: 1.03x faster                                            |
| chaos                            | 28.9 ms                                                  | 28.1 ms: 1.03x faster                                            |
| sympy_integrate                  | 8.02 ms                                                  | 7.80 ms: 1.03x faster                                            |
| thrift                           | 322 us                                                   | 313 us: 1.03x faster                                             |
| bench_mp_pool                    | 39.7 ms                                                  | 39.1 ms: 1.02x faster                                            |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                             |
| sympy_sum                        | 57.6 ms                                                  | 56.7 ms: 1.01x faster                                            |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                             |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                             |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.01x faster                                            |
| sympy_str                        | 104 ms                                                   | 104 ms: 1.00x faster                                             |
| scimark_lu                       | 51.3 ms                                                  | 51.1 ms: 1.00x faster                                            |
| mdp                              | 1.09 sec                                                 | 1.10 sec: 1.01x slower                                           |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                             |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.01x slower                                             |
| richards_super                   | 25.4 ms                                                  | 25.6 ms: 1.01x slower                                            |
| sqlalchemy_declarative           | 46.8 ms                                                  | 47.2 ms: 1.01x slower                                            |
| genshi_text                      | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                            |
| crypto_pyaes                     | 38.8 ms                                                  | 39.4 ms: 1.01x slower                                            |
| async_tree_eager                 | 45.6 ms                                                  | 46.2 ms: 1.01x slower                                            |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 218 ms: 1.02x slower                                             |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.33 ms: 1.03x slower                                            |
| pprint_safe_repr                 | 328 ms                                                   | 339 ms: 1.03x slower                                             |
| pprint_pformat                   | 665 ms                                                   | 688 ms: 1.03x slower                                             |
| regex_v8                         | 9.59 ms                                                  | 9.92 ms: 1.03x slower                                            |
| sympy_expand                     | 167 ms                                                   | 176 ms: 1.05x slower                                             |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.06x slower                                            |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                            |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                             |
| shortest_path                    | 219 ms                                                   | 237 ms: 1.08x slower                                             |
| nbody                            | 54.2 ms                                                  | 59.6 ms: 1.10x slower                                            |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                            |
| meteor_contest                   | 47.7 ms                                                  | 53.1 ms: 1.11x slower                                            |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                            |
| connected_components             | 201 ms                                                   | 228 ms: 1.14x slower                                             |
| python_startup                   | 8.01 ms                                                  | 9.13 ms: 1.14x slower                                            |
| mako                             | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                            |
| many_optionals                   | 195 us                                                   | 228 us: 1.17x slower                                             |
| json_dumps                       | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                            |
| telco                            | 2.61 ms                                                  | 3.26 ms: 1.25x slower                                            |
| python_startup_no_site           | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                            |
| bench_thread_pool                | 419 us                                                   | 580 us: 1.38x slower                                             |
| coverage                         | 26.9 ms                                                  | 38.8 ms: 1.44x slower                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 73.7 ms: 2.29x slower                                            |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                     |

Benchmark hidden because not significant (2): scimark_fft, json
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250328-3.14.0a6+-e9fdced-CLANG,NOGIL/bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.136x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.23x