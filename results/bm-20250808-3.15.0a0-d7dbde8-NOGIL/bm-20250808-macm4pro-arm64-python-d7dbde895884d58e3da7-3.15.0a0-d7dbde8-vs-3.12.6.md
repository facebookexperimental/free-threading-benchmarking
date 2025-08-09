# Results vs. 3.12.6

- fork: python
- ref: d7dbde895884d58e3da7
- machine: darwin-arm64
- commit hash: d7dbde8
- commit date: 2025-08-08
- overall geometric mean: 1.087x faster
- HPT reliability: 97.48%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 991 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.1 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.5 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 61.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.1 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                   |
| tomli_loads          | 957 ms                                                   | 999 ms: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 774 us: 2.60x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.1 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 593 ms: 1.84x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.5 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 485 us: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| deepcopy                         | 161 us                                                   | 121 us: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.32x faster                                                   |
| float                            | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.23 us: 1.20x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 815 ns: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.1 ms: 1.17x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.2 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| k_core                           | 1.12 sec                                                 | 984 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| go                               | 70.0 ms                                                  | 62.0 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.3 ns: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.7 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                   |
| raytrace                         | 145 ms                                                   | 135 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.4 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 991 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.60 us: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.09 ms: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.87 us: 1.02x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 146 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 999 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.2 us: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.7 ms: 1.05x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 355 ms: 1.08x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 723 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.2 ms: 1.11x slower                                                   |
| nbody                            | 54.2 ms                                                  | 61.2 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.7 ms: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.22 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 598 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.5 ms: 1.47x slower                                                   |
| many_optionals                   | 195 us                                                   | 324 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): sympy_integrate, pidigits
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250808-3.15.0a0-d7dbde8-NOGIL/bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 97.48% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x