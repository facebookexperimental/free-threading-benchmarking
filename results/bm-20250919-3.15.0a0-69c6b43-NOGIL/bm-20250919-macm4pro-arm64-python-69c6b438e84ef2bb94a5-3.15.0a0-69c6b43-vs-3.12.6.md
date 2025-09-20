# Results vs. 3.12.6

- fork: python
- ref: 69c6b438e84ef2bb94a5
- machine: darwin-arm64
- commit hash: 69c6b43
- commit date: 2025-09-19
- overall geometric mean: 1.086x faster
- HPT reliability: 95.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 985 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.1 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100.0 ms: 1.78x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.2 ms: 1.25x faster                                                   |
| nbody          | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.9 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.0 ms: 1.39x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.09x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.60 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.11x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                   |
| mako            | 4.77 ms                                                  | 5.85 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 761 us: 2.64x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.1 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 602 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100.0 ms: 1.78x faster                                                  |
| create_gc_cycles                 | 830 us                                                   | 474 us: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.0 ms: 1.39x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                   |
| deepcopy                         | 161 us                                                   | 116 us: 1.39x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 30.2 ms: 1.25x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.38 us: 1.17x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 832 ns: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.8 ns: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                    |
| go                               | 70.0 ms                                                  | 62.2 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.9 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.0 ms: 1.09x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.7 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.9 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 985 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.52 us: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.05 ms: 1.00x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.82 us: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 43.9 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.02x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 74.3 us: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 338 us: 1.05x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 345 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 702 ms: 1.06x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.6 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.29 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.6 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.60 ms: 1.20x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 57.2 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.85 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 592 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 332 us: 1.70x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): pidigits, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250919-3.15.0a0-69c6b43-NOGIL/bm-20250919-macm4pro-arm64-python-69c6b438e84ef2bb94a5-3.15.0a0-69c6b43.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 95.22% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x