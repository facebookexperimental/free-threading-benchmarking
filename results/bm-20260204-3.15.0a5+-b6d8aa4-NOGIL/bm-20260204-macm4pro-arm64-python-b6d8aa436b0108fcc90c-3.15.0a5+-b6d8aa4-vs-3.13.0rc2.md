# Results vs. 3.13.0rc2

- fork: python
- ref: b6d8aa436b0108fcc90c
- machine: darwin-arm64
- commit hash: b6d8aa4
- commit date: 2026-02-04
- overall geometric mean: 1.039x faster
- HPT reliability: 82.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 979 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 236 ms: 2.22x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.8 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.4 ms: 3.16x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.3 ms: 1.30x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 8.95 ms: 1.19x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 846 ms: 1.18x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.8 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.21x slower                                                    |
| mako            | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 236 ms: 2.22x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 501 us: 1.98x faster                                                     |
| mdp                              | 1.06 sec                                                       | 592 ms: 1.79x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 984 ms: 1.49x faster                                                     |
| deepcopy                         | 145 us                                                         | 104 us: 1.40x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 58.5 ms: 1.24x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 781 ns: 1.21x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 8.95 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.0 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 846 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 189 ms: 1.17x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| fannkuch                         | 179 ms                                                         | 165 ms: 1.08x faster                                                     |
| docutils                         | 1.05 sec                                                       | 979 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 448 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.02x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 25.4 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                    |
| thrift                           | 309 us                                                         | 325 us: 1.05x slower                                                     |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.95 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.8 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.38 us: 1.06x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.0 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.62 us: 1.07x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.8 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 70.1 us: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.7 ms: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 59.5 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 183 ms: 1.15x slower                                                     |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.07 us: 1.19x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.12 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.21x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 259 us: 1.29x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.3 ms: 1.29x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.3 ms: 1.30x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 58.6 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.4 ms: 3.16x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260204-3.15.0a5+-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 82.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x