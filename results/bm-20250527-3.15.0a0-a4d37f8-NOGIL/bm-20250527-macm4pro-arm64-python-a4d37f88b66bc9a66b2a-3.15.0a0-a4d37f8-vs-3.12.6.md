# Results vs. 3.12.6

- fork: python
- ref: a4d37f88b66bc9a66b2a
- machine: darwin-arm64
- commit hash: a4d37f8
- commit date: 2025-05-27
- overall geometric mean: 1.111x faster
- HPT reliability: 99.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 987 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.50x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.47x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 189 ms: 2.35x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.24x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.7 ms: 1.81x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 232 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.40x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.2 ms: 2.37x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.40x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                   |
| nbody          | 54.2 ms                                                  | 53.7 ms: 1.01x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.13 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| json_loads           | 10.9 us                                                  | 12.4 us: 1.14x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.40 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.86 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.9 ms: 1.05x slower                                                   |
| mako            | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                   |
| django_template | 13.6 ms                                                  | 16.0 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 761 us: 2.64x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.50x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.47x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 189 ms: 2.35x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.24x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.53 ms: 2.18x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                   |
| mdp                              | 1.09 sec                                                 | 553 ms: 1.98x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.89x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.7 ms: 1.81x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 475 us: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 232 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.40x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.5 us: 1.35x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.66 us: 1.28x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.23 us: 1.19x faster                                                   |
| go                               | 70.0 ms                                                  | 59.2 ms: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                  |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.59 ms: 1.08x faster                                                   |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.6 ms: 1.07x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.5 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.13 ms: 1.05x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                   |
| docutils                         | 1.02 sec                                                 | 987 ms: 1.04x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.96 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.90 ms: 1.02x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.02x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                   |
| nbody                            | 54.2 ms                                                  | 53.7 ms: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.0 ms: 1.00x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.0 us: 1.01x slower                                                   |
| thrift                           | 322 us                                                   | 329 us: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.6 ms: 1.04x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.05x slower                                                    |
| json                             | 1.93 ms                                                  | 2.02 ms: 1.05x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 22.9 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.4 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.76 us: 1.07x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.05 us: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 52.6 ms: 1.10x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 184 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 372 ms: 1.13x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 757 ms: 1.14x slower                                                    |
| json_loads                       | 10.9 us                                                  | 12.4 us: 1.14x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.40 ms: 1.17x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.0 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.86 ms: 1.20x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.25 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 247 us: 1.26x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 69.1 ms: 1.35x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 591 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.2 ms: 2.37x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 214 ns: 4.21x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250527-3.15.0a0-a4d37f8-NOGIL/bm-20250527-macm4pro-arm64-python-a4d37f88b66bc9a66b2a-3.15.0a0-a4d37f8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 99.75% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x