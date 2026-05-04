# Results vs. 3.12.6

- fork: python
- ref: 3efd2f4db6de0990136a
- machine: darwin-arm64
- commit hash: 3efd2f4
- commit date: 2026-05-04
- overall geometric mean: 1.111x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.5 ms: 2.94x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.9 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.4 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.3 ms: 1.17x faster                                                    |
| tomli_loads          | 957 ms                                                   | 888 ms: 1.08x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 38.1 ms: 1.02x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| mako            | 4.77 ms                                                  | 5.74 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.12 ms: 5.05x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 809 us: 2.48x faster                                                     |
| pylint                           | 128 ms                                                   | 51.7 ms: 2.48x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 603 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 516 us: 1.61x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.21 us: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 802 ns: 1.21x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.24 us: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.7 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.3 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 44.2 ns: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.9 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 888 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 463 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.7 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.4 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.7 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| sphinx                           | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 38.1 ms: 1.02x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.8 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 339 ms: 1.03x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 688 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.22 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.9 ms: 1.07x slower                                                    |
| thrift                           | 322 us                                                   | 344 us: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.1 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 59.0 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.4 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.9 ms: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.74 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.21x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 567 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 271 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.7 ms: 1.48x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.5 ms: 2.94x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260504-3.15.0a8+-3efd2f4-NOGIL/bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8+-3efd2f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.38x