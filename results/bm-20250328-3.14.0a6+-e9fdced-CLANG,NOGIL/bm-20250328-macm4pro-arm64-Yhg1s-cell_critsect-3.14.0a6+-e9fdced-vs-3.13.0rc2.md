# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: cell_critsect
- machine: darwin-arm64
- commit hash: e9fdced
- commit date: 2025-03-28
- overall geometric mean: 1.054x faster
- HPT reliability: 72.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                             |
| docutils       | 1.05 sec                                                       | 960 ms: 1.09x faster                                             |
| html5lib       | 23.1 ms                                                        | 22.1 ms: 1.05x faster                                            |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                          | 1.04x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 183 ms: 2.84x faster                                             |
| async_tree_eager_io              | 525 ms                                                         | 195 ms: 2.69x faster                                             |
| async_tree_io_tg                 | 405 ms                                                         | 188 ms: 2.15x faster                                             |
| async_tree_io                    | 386 ms                                                         | 203 ms: 1.90x faster                                             |
| async_tree_none_tg               | 133 ms                                                         | 82.2 ms: 1.61x faster                                            |
| async_tree_memoization_tg        | 186 ms                                                         | 120 ms: 1.54x faster                                             |
| async_tree_none                  | 142 ms                                                         | 98.1 ms: 1.45x faster                                            |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                             |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 226 ms: 1.33x faster                                             |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 236 ms: 1.25x faster                                             |
| coroutines                       | 10.8 ms                                                        | 9.09 ms: 1.18x faster                                            |
| async_generators                 | 193 ms                                                         | 166 ms: 1.17x faster                                             |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                             |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                             |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                             |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 218 ms: 1.05x slower                                             |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                             |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 73.7 ms: 2.55x slower                                            |
| Geometric mean                   | (ref)                                                          | 1.30x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                            |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                             |
| nbody          | 42.5 ms                                                        | 59.6 ms: 1.40x slower                                            |
| Geometric mean | (ref)                                                          | 1.07x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                            |
| regex_v8       | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                            |
| regex_compile  | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                            |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                             |
| Geometric mean | (ref)                                                          | 1.02x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 34.8 ms: 1.32x faster                                            |
| tomli_loads          | 1000 ms                                                        | 884 ms: 1.13x faster                                             |
| xml_etree_parse      | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                            |
| xml_etree_generate   | 35.8 ms                                                        | 34.6 ms: 1.04x faster                                            |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                            |
| unpickle_pure_python | 99.5 us                                                        | 98.7 us: 1.01x faster                                            |
| json_dumps           | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                            |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                            |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                             |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.13 ms: 1.06x slower                                            |
| python_startup_no_site | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                            |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                            |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                            |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                            |
| mako            | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                            |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 183 ms: 2.84x faster                                             |
| gc_traversal                     | 2.04 ms                                                        | 745 us: 2.74x faster                                             |
| async_tree_eager_io              | 525 ms                                                         | 195 ms: 2.69x faster                                             |
| create_gc_cycles                 | 993 us                                                         | 451 us: 2.20x faster                                             |
| async_tree_io_tg                 | 405 ms                                                         | 188 ms: 2.15x faster                                             |
| async_tree_io                    | 386 ms                                                         | 203 ms: 1.90x faster                                             |
| async_tree_none_tg               | 133 ms                                                         | 82.2 ms: 1.61x faster                                            |
| async_tree_memoization_tg        | 186 ms                                                         | 120 ms: 1.54x faster                                             |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                           |
| async_tree_none                  | 142 ms                                                         | 98.1 ms: 1.45x faster                                            |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                             |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                             |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 226 ms: 1.33x faster                                             |
| xml_etree_iterparse              | 46.1 ms                                                        | 34.8 ms: 1.32x faster                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 236 ms: 1.25x faster                                             |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.24x faster                                            |
| go                               | 72.6 ms                                                        | 58.7 ms: 1.24x faster                                            |
| coroutines                       | 10.8 ms                                                        | 9.09 ms: 1.18x faster                                            |
| sqlite_synth                     | 948 ns                                                         | 806 ns: 1.18x faster                                             |
| scimark_sor                      | 64.0 ms                                                        | 54.5 ms: 1.17x faster                                            |
| async_generators                 | 193 ms                                                         | 166 ms: 1.17x faster                                             |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.16x faster                                            |
| generators                       | 15.7 ms                                                        | 13.8 ms: 1.14x faster                                            |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                             |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                             |
| tomli_loads                      | 1000 ms                                                        | 884 ms: 1.13x faster                                             |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                            |
| xml_etree_parse                  | 62.4 ms                                                        | 55.9 ms: 1.12x faster                                            |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                           |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                            |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                            |
| docutils                         | 1.05 sec                                                       | 960 ms: 1.09x faster                                             |
| regex_v8                         | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                            |
| pycparser                        | 470 ms                                                         | 446 ms: 1.05x faster                                             |
| html5lib                         | 23.1 ms                                                        | 22.1 ms: 1.05x faster                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                             |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                             |
| xml_etree_generate               | 35.8 ms                                                        | 34.6 ms: 1.04x faster                                            |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                             |
| genshi_xml                       | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                            |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                             |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                            |
| unpickle_pure_python             | 99.5 us                                                        | 98.7 us: 1.01x faster                                            |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                            |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                             |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                            |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                             |
| hexiom                           | 2.85 ms                                                        | 2.91 ms: 1.02x slower                                            |
| regex_compile                    | 47.9 ms                                                        | 49.1 ms: 1.02x slower                                            |
| bench_mp_pool                    | 37.8 ms                                                        | 39.1 ms: 1.03x slower                                            |
| sympy_integrate                  | 7.53 ms                                                        | 7.80 ms: 1.04x slower                                            |
| mdp                              | 1.06 sec                                                       | 1.10 sec: 1.04x slower                                           |
| richards_super                   | 24.7 ms                                                        | 25.6 ms: 1.04x slower                                            |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 218 ms: 1.05x slower                                             |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                            |
| pprint_safe_repr                 | 322 ms                                                         | 339 ms: 1.05x slower                                             |
| shortest_path                    | 225 ms                                                         | 237 ms: 1.05x slower                                             |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                            |
| python_startup                   | 8.63 ms                                                        | 9.13 ms: 1.06x slower                                            |
| pprint_pformat                   | 650 ms                                                         | 688 ms: 1.06x slower                                             |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                             |
| logging_silent                   | 40.6 ns                                                        | 43.0 ns: 1.06x slower                                            |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                             |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                             |
| typing_runtime_protocols         | 64.6 us                                                        | 68.8 us: 1.06x slower                                            |
| telco                            | 3.07 ms                                                        | 3.26 ms: 1.06x slower                                            |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                            |
| sqlalchemy_declarative           | 44.4 ms                                                        | 47.2 ms: 1.06x slower                                            |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                            |
| pylint                           | 106 ms                                                         | 112 ms: 1.07x slower                                             |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.33 ms: 1.07x slower                                            |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                            |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                            |
| json_dumps                       | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                            |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                            |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                             |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                            |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                             |
| connected_components             | 208 ms                                                         | 228 ms: 1.10x slower                                             |
| sympy_expand                     | 159 ms                                                         | 176 ms: 1.11x slower                                             |
| meteor_contest                   | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                            |
| spectral_norm                    | 43.7 ms                                                        | 49.5 ms: 1.13x slower                                            |
| many_optionals                   | 200 us                                                         | 228 us: 1.14x slower                                             |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                            |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.14x slower                                             |
| chaos                            | 24.3 ms                                                        | 28.1 ms: 1.16x slower                                            |
| comprehensions                   | 6.80 us                                                        | 7.91 us: 1.16x slower                                            |
| crypto_pyaes                     | 33.6 ms                                                        | 39.4 ms: 1.17x slower                                            |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                             |
| scimark_lu                       | 42.8 ms                                                        | 51.1 ms: 1.20x slower                                            |
| python_startup_no_site           | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                            |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                            |
| mako                             | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                            |
| coverage                         | 31.2 ms                                                        | 38.8 ms: 1.24x slower                                            |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.28 ms: 1.28x slower                                            |
| subparsers                       | 6.26 ms                                                        | 8.28 ms: 1.32x slower                                            |
| nbody                            | 42.5 ms                                                        | 59.6 ms: 1.40x slower                                            |
| bench_thread_pool                | 412 us                                                         | 580 us: 1.41x slower                                             |
| async_tree_eager_tg              | 28.9 ms                                                        | 73.7 ms: 2.55x slower                                            |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                     |

Benchmark hidden because not significant (1): json
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250328-3.14.0a6+-e9fdced-CLANG,NOGIL/bm-20250328-macm4pro-arm64-Yhg1s-cell_critsect-3.14.0a6+-e9fdced.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.054x faster

# HPT report

- Reliability score: 72.79% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x