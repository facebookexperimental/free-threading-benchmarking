# Results vs. 3.12.6

- fork: python
- ref: 6dad8b88cc39d8f9f41c
- machine: darwin-arm64
- commit hash: 6dad8b8
- commit date: 2026-09-18
- overall geometric mean: 1.002x faster
- HPT reliability: 82.30%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 138 ms: 1.21x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 461 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 317 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 307 ms: 1.45x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 322 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 168 ms: 1.23x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 304 ms: 1.11x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 204 ms: 1.09x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 164 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 315 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.2 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 264 ms: 1.14x slower                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 151 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 282 ms: 1.33x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 168 ms: 1.49x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 71.3 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 62.0 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 69.7 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 40.3 ms: 1.04x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 118 us: 1.15x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.5 ms: 1.18x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 167 us: 1.20x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.45 ms: 1.31x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.29x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| django_template | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.28x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.62 ms: 4.50x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.58x faster                                                    |
| pylint                           | 128 ms                                                   | 54.3 ms: 2.36x faster                                                   |
| mdp                              | 1.09 sec                                                 | 637 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 486 us: 1.71x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 317 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 307 ms: 1.45x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 322 ms: 1.43x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 168 ms: 1.23x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 16.0 us: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 304 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.90 us: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 204 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 164 ms: 1.09x faster                                                    |
| float                            | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.9 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 315 ms: 1.06x faster                                                    |
| go                               | 70.0 ms                                                  | 66.8 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.4 ms: 1.04x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.2 ms: 1.02x faster                                                   |
| pyflate                          | 216 ms                                                   | 214 ms: 1.01x faster                                                    |
| pycparser                        | 497 ms                                                   | 502 ms: 1.01x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 62.1 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| raytrace                         | 145 ms                                                   | 149 ms: 1.03x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.65 us: 1.03x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 52.5 ns: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.03x slower                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 40.3 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.93 us: 1.05x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 45.6 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| sphinx                           | 434 ms                                                   | 461 ms: 1.06x slower                                                    |
| chaos                            | 28.9 ms                                                  | 30.9 ms: 1.07x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.57 ms: 1.07x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                  |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 63.7 ms: 1.11x slower                                                   |
| sympy_str                        | 104 ms                                                   | 116 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.4 ms: 1.12x slower                                                   |
| thrift                           | 322 us                                                   | 361 us: 1.12x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 36.2 ms: 1.12x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 264 ms: 1.14x slower                                                    |
| nbody                            | 54.2 ms                                                  | 62.0 ms: 1.14x slower                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 151 ms: 1.14x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 118 us: 1.15x slower                                                    |
| generators                       | 21.9 ms                                                  | 25.3 ms: 1.15x slower                                                   |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.2 ms: 1.16x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 382 ms: 1.16x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.03 ms: 1.18x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 197 ms: 1.18x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.5 ms: 1.18x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.59 ms: 1.18x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 789 ms: 1.19x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                   |
| richards                         | 22.4 ms                                                  | 26.9 ms: 1.20x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 167 us: 1.20x slower                                                    |
| 2to3                             | 114 ms                                                   | 138 ms: 1.21x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 30.7 ms: 1.21x slower                                                   |
| connected_components             | 201 ms                                                   | 244 ms: 1.21x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 65.2 ms: 1.27x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 69.7 ms: 1.28x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.45 ms: 1.31x slower                                                   |
| django_template                  | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 282 ms: 1.33x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 564 us: 1.35x slower                                                    |
| many_optionals                   | 195 us                                                   | 275 us: 1.41x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 168 ms: 1.49x slower                                                    |
| coverage                         | 26.9 ms                                                  | 41.1 ms: 1.53x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 71.3 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 82.30% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x