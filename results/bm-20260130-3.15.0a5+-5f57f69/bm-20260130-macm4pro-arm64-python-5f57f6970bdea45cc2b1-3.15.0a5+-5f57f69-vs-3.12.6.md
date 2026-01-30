# Results vs. 3.12.6

- fork: python
- ref: 5f57f6970bdea45cc2b1
- machine: darwin-arm64
- commit hash: 5f57f69
- commit date: 2026-01-30
- overall geometric mean: 1.200x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 107 ms: 1.07x faster                                                     |
| docutils       | 1.02 sec                                                 | 975 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.6 ms: 1.12x faster                                                    |
| sphinx         | 434 ms                                                   | 378 ms: 1.15x faster                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 212 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 211 ms: 2.11x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 93.9 ms: 1.83x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.5 ms: 1.81x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 240 ms: 1.41x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 38.7 ms: 1.18x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.09x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.06x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.8 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.0 ms: 1.41x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 155 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.9 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.40 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| tomli_loads          | 957 ms                                                   | 817 ms: 1.17x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.7 us: 1.08x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.45 ms: 1.11x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.6 ms: 1.06x faster                                                    |
| mako            | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                    |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.04x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.79 ms: 5.48x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 212 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 211 ms: 2.11x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| mdp                              | 1.09 sec                                                 | 525 ms: 2.08x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 93.9 ms: 1.83x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.5 ms: 1.81x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                     |
| deepcopy                         | 161 us                                                   | 94.5 us: 1.71x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.0 us: 1.67x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 6.84 us: 1.44x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 240 ms: 1.41x faster                                                     |
| float                            | 37.9 ms                                                  | 27.0 ms: 1.41x faster                                                    |
| go                               | 70.0 ms                                                  | 51.0 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.2 ns: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 48.3 ms: 1.26x faster                                                    |
| k_core                           | 1.12 sec                                                 | 894 ms: 1.25x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.6 ms: 1.25x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                     |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.40 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.23x faster                                                     |
| nbody                            | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.13 us: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                    |
| pyflate                          | 216 ms                                                   | 181 ms: 1.20x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.34 us: 1.20x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.1 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 38.7 ms: 1.18x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.7 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.0 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 817 ms: 1.17x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 60.7 us: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.17x faster                                                    |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 21.9 ms: 1.16x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.4 ms: 1.16x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.2 ms: 1.15x faster                                                    |
| sphinx                           | 434 ms                                                   | 378 ms: 1.15x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.69 ms: 1.13x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                    |
| pycparser                        | 497 ms                                                   | 445 ms: 1.12x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 20.6 ms: 1.12x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.22 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.45 ms: 1.11x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 299 ms: 1.10x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 607 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 211 ms: 1.09x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.9 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 298 us: 1.08x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 53.5 ms: 1.08x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 95.7 us: 1.08x faster                                                    |
| json                             | 1.93 ms                                                  | 1.81 ms: 1.07x faster                                                    |
| 2to3                             | 114 ms                                                   | 107 ms: 1.07x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 97.8 ms: 1.07x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.6 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.06x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 166 ms: 1.05x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                    |
| docutils                         | 1.02 sec                                                 | 975 ms: 1.05x faster                                                     |
| pidigits                         | 161 ms                                                   | 155 ms: 1.04x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 1.95 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 940 ns: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.40 ms: 1.02x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 47.2 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 866 us: 1.04x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.1 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.0 ms: 1.15x slower                                                    |
| many_optionals                   | 195 us                                                   | 235 us: 1.20x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.8 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260130-3.15.0a5+-5f57f69/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5+-5f57f69.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.200x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.22x