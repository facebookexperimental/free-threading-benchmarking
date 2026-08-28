# Results vs. 3.12.6

- fork: python
- ref: 24e5a55ccb0c5db68136
- machine: darwin-arm64
- commit hash: 24e5a55
- commit date: 2026-08-27
- overall geometric mean: 1.139x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 942 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                   |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 313 ms: 1.59x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 317 ms: 1.45x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 123 ms: 1.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 333 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 337 ms: 1.32x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 180 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 295 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 41.2 ms: 1.32x faster                                                   |
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.3 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 815 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.3 us: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 69.8 ms: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.23 ms: 1.15x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.59 ms: 1.04x faster                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.05x faster                                                   |
| pylint                           | 128 ms                                                   | 56.8 ms: 2.25x faster                                                   |
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                    |
| deepcopy                         | 161 us                                                   | 97.8 us: 1.65x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 313 ms: 1.59x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.69 us: 1.47x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 317 ms: 1.45x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 123 ms: 1.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 333 ms: 1.44x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.6 us: 1.43x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 337 ms: 1.32x faster                                                    |
| nbody                            | 54.2 ms                                                  | 41.2 ms: 1.32x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| go                               | 70.0 ms                                                  | 53.6 ms: 1.31x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 41.7 ms: 1.30x faster                                                   |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 180 ms: 1.24x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 115 ms: 1.24x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.5 ms: 1.23x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.7 ns: 1.22x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 815 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 295 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 983 ms: 1.14x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.70 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.09x faster                                                   |
| docutils                         | 1.02 sec                                                 | 942 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.8 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.50 ms: 1.07x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 626 ms: 1.06x faster                                                    |
| fannkuch                         | 176 ms                                                   | 166 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 97.3 us: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.1 ms: 1.05x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 925 ns: 1.05x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.59 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.03x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.95 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| thrift                           | 322 us                                                   | 317 us: 1.01x faster                                                    |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.3 ms: 1.01x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 422 us: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 837 us: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.9 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 69.8 ms: 1.03x slower                                                   |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.23 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 245 us: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (2): json_loads, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260827-3.16.0a0-24e5a55/bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.139x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x