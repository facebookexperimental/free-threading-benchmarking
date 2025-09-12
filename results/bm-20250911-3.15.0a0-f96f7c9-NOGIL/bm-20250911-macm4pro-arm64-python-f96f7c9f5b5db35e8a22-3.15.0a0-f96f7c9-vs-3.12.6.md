# Results vs. 3.12.6

- fork: python
- ref: f96f7c9f5b5db35e8a22
- machine: darwin-arm64
- commit hash: f96f7c9
- commit date: 2025-09-11
- overall geometric mean: 1.079x faster
- HPT reliability: 91.29%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.3 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.04 ms: 1.06x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 981 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.58 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.8 ms: 1.14x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| mako            | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.62x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| mdp                              | 1.09 sec                                                 | 607 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 474 us: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.38x faster                                                   |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| float                            | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.44 us: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 830 ns: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| go                               | 70.0 ms                                                  | 62.1 ms: 1.13x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.5 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.5 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.9 ns: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 134 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 204 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.3 ms: 1.06x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.04 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.52 us: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.07 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.3 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 981 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 74.1 us: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.7 ms: 1.06x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.1 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                   |
| thrift                           | 322 us                                                   | 343 us: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 188 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.0 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 361 ms: 1.10x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 737 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.1 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.31 ms: 1.11x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 58.0 ms: 1.13x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.8 ms: 1.14x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.6 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.58 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 579 us: 1.38x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 333 us: 1.71x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.3 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): logging_format, async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250911-3.15.0a0-f96f7c9-NOGIL/bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 91.29% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x