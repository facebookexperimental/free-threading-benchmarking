# Results vs. 3.12.6

- fork: python
- ref: 4d0e8ee649ceff96b130
- machine: darwin-arm64
- commit hash: 4d0e8ee
- commit date: 2026-03-29
- overall geometric mean: 1.160x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.61x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.5 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                    | 1.20x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.2 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                    |
| tomli_loads          | 957 ms                                                   | 813 ms: 1.18x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.1 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.64 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.76 ms: 1.00x faster                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| mdp                              | 1.09 sec                                                 | 530 ms: 2.06x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.8 us: 1.63x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.61x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                    |
| float                            | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.13 us: 1.38x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 52.9 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 41.9 ms: 1.30x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.1 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| k_core                           | 1.12 sec                                                 | 896 ms: 1.25x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 114 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.6 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.2 ms: 1.21x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.3 ms: 1.20x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.2 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.5 ms: 1.18x faster                                                    |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.3 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 813 ms: 1.18x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 44.5 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.81 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.7 us: 1.10x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.64 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 637 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.1 us: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 935 ns: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.9 ms: 1.03x faster                                                    |
| thrift                           | 322 us                                                   | 313 us: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.5 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.76 ms: 1.00x faster                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.04x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 952 us: 1.15x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.42 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.5 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (2): regex_v8, pickle_pure_python
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260329-3.15.0a7+-4d0e8ee/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.160x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.24x