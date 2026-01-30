# Results vs. 3.12.6

- fork: python
- ref: 5f57f6970bdea45cc2b1
- machine: darwin-arm64
- commit hash: 5f57f69
- commit date: 2026-01-30
- overall geometric mean: 1.118x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 975 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.90x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.3 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.3 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.2 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| tomli_loads          | 957 ms                                                   | 860 ms: 1.11x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 105 us: 1.02x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.60 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.99 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 10.7 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.07x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.07 ms: 5.10x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 764 us: 2.63x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.90x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| mdp                              | 1.09 sec                                                 | 595 ms: 1.83x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 496 us: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| deepcopy                         | 161 us                                                   | 104 us: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.49x faster                                                    |
| float                            | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.17 us: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.5 ms: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 809 ns: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.18x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 53.8 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                     |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 860 ms: 1.11x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 453 ms: 1.10x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.1 ms: 1.09x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.58 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.2 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.2 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 975 ms: 1.05x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 69.1 us: 1.03x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.89 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.6 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 673 ms: 1.01x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.08 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.3 ms: 1.02x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 105 us: 1.02x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.7 ms: 1.02x slower                                                    |
| thrift                           | 322 us                                                   | 330 us: 1.02x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 59.0 ms: 1.02x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 182 ms: 1.09x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 56.5 ms: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.8 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.0 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.60 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.99 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 561 us: 1.34x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.3 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (5): async_tree_eager, scimark_monte_carlo, dask, richards, pprint_safe_repr
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260130-3.15.0a5+-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.118x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.36x