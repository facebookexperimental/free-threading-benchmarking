# Results vs. 3.12.6

- fork: python
- ref: v3.14.0a5
- machine: darwin-arm64
- commit hash: 3ae9101
- commit date: 2025-02-11
- overall geometric mean: 1.010x slower
- HPT reliability: 99.24%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 128 ms: 1.12x slower                                         |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                       |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                        |
| sphinx         | 434 ms                                                   | 437 ms: 1.01x slower                                         |
| Geometric mean | (ref)                                                    | 1.04x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                         |
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.16x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                         |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 99.9 ms: 1.72x faster                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                         |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                         |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                         |
| coroutines                       | 13.6 ms                                                  | 11.3 ms: 1.20x faster                                        |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                         |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                         |
| async_tree_eager                 | 45.6 ms                                                  | 57.7 ms: 1.27x slower                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.6 ms: 2.79x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 34.2 ms: 1.11x faster                                        |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                         |
| nbody          | 54.2 ms                                                  | 72.6 ms: 1.34x slower                                        |
| Geometric mean | (ref)                                                    | 1.06x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                        |
| regex_dna      | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                        |
| regex_compile  | 54.6 ms                                                  | 57.3 ms: 1.05x slower                                        |
| regex_v8       | 9.59 ms                                                  | 10.3 ms: 1.08x slower                                        |
| Geometric mean | (ref)                                                    | 1.03x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.2 ms: 1.25x faster                                        |
| xml_etree_parse      | 67.9 ms                                                  | 57.6 ms: 1.18x faster                                        |
| xml_etree_generate   | 38.9 ms                                                  | 40.5 ms: 1.04x slower                                        |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.09x slower                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.7 ms: 1.11x slower                                        |
| tomli_loads          | 957 ms                                                   | 1.07 sec: 1.11x slower                                       |
| json_dumps           | 4.26 ms                                                  | 5.13 ms: 1.21x slower                                        |
| unpickle_pure_python | 103 us                                                   | 127 us: 1.23x slower                                         |
| pickle_pure_python   | 139 us                                                   | 173 us: 1.24x slower                                         |
| Geometric mean       | (ref)                                                    | 1.06x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.26 ms: 1.16x slower                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.68 ms: 1.17x slower                                        |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                        |
| genshi_text     | 10.5 ms                                                  | 12.7 ms: 1.21x slower                                        |
| mako            | 4.77 ms                                                  | 6.22 ms: 1.30x slower                                        |
| django_template | 13.6 ms                                                  | 17.9 ms: 1.32x slower                                        |
| Geometric mean  | (ref)                                                    | 1.25x slower                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.05 ms: 2.29x faster                                        |
| gc_traversal                     | 2.01 ms                                                  | 906 us: 2.22x faster                                         |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                         |
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.16x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                         |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 99.9 ms: 1.72x faster                                        |
| create_gc_cycles                 | 830 us                                                   | 494 us: 1.68x faster                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                         |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                         |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                         |
| deepcopy                         | 161 us                                                   | 125 us: 1.29x faster                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.2 ms: 1.25x faster                                        |
| coroutines                       | 13.6 ms                                                  | 11.3 ms: 1.20x faster                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 57.6 ms: 1.18x faster                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                        |
| sqlite_synth                     | 967 ns                                                   | 848 ns: 1.14x faster                                         |
| deepcopy_memo                    | 18.3 us                                                  | 16.3 us: 1.12x faster                                        |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                         |
| float                            | 37.9 ms                                                  | 34.2 ms: 1.11x faster                                        |
| regex_dna                        | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                        |
| pathlib                          | 12.4 ms                                                  | 11.4 ms: 1.08x faster                                        |
| k_core                           | 1.12 sec                                                 | 1.03 sec: 1.08x faster                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.36 us: 1.07x faster                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 38.0 ms: 1.04x faster                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.16 sec: 1.04x faster                                       |
| comprehensions                   | 9.84 us                                                  | 9.58 us: 1.03x faster                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                         |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                         |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                       |
| pycparser                        | 497 ms                                                   | 502 ms: 1.01x slower                                         |
| sphinx                           | 434 ms                                                   | 437 ms: 1.01x slower                                         |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                        |
| generators                       | 21.9 ms                                                  | 22.6 ms: 1.03x slower                                        |
| dulwich_log                      | 21.3 ms                                                  | 21.9 ms: 1.03x slower                                        |
| go                               | 70.0 ms                                                  | 72.2 ms: 1.03x slower                                        |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                        |
| xml_etree_generate               | 38.9 ms                                                  | 40.5 ms: 1.04x slower                                        |
| spectral_norm                    | 54.4 ms                                                  | 56.7 ms: 1.04x slower                                        |
| regex_compile                    | 54.6 ms                                                  | 57.3 ms: 1.05x slower                                        |
| pyflate                          | 216 ms                                                   | 230 ms: 1.06x slower                                         |
| mdp                              | 1.09 sec                                                 | 1.17 sec: 1.07x slower                                       |
| regex_v8                         | 9.59 ms                                                  | 10.3 ms: 1.08x slower                                        |
| logging_silent                   | 50.9 ns                                                  | 55.0 ns: 1.08x slower                                        |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.09x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                         |
| raytrace                         | 145 ms                                                   | 158 ms: 1.09x slower                                         |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.1 ms: 1.09x slower                                        |
| thrift                           | 322 us                                                   | 352 us: 1.09x slower                                         |
| sympy_sum                        | 57.6 ms                                                  | 63.1 ms: 1.10x slower                                        |
| nqueens                          | 43.5 ms                                                  | 47.8 ms: 1.10x slower                                        |
| sqlglot_optimize                 | 23.4 ms                                                  | 25.8 ms: 1.10x slower                                        |
| xml_etree_process                | 26.7 ms                                                  | 29.7 ms: 1.11x slower                                        |
| tomli_loads                      | 957 ms                                                   | 1.07 sec: 1.11x slower                                       |
| sqlglot_normalize                | 126 ms                                                   | 140 ms: 1.11x slower                                         |
| logging_simple                   | 2.57 us                                                  | 2.87 us: 1.12x slower                                        |
| logging_format                   | 2.80 us                                                  | 3.14 us: 1.12x slower                                        |
| 2to3                             | 114 ms                                                   | 128 ms: 1.12x slower                                         |
| shortest_path                    | 219 ms                                                   | 247 ms: 1.13x slower                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                         |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.85 ms: 1.13x slower                                        |
| chaos                            | 28.9 ms                                                  | 32.7 ms: 1.13x slower                                        |
| scimark_fft                      | 142 ms                                                   | 161 ms: 1.14x slower                                         |
| crypto_pyaes                     | 38.8 ms                                                  | 44.2 ms: 1.14x slower                                        |
| sympy_str                        | 104 ms                                                   | 119 ms: 1.14x slower                                         |
| scimark_sor                      | 61.0 ms                                                  | 69.7 ms: 1.14x slower                                        |
| python_startup                   | 8.01 ms                                                  | 9.26 ms: 1.16x slower                                        |
| sympy_integrate                  | 8.02 ms                                                  | 9.29 ms: 1.16x slower                                        |
| connected_components             | 201 ms                                                   | 233 ms: 1.16x slower                                         |
| typing_runtime_protocols         | 71.0 us                                                  | 82.6 us: 1.16x slower                                        |
| sqlglot_transpile                | 696 us                                                   | 812 us: 1.17x slower                                         |
| sqlglot_parse                    | 577 us                                                   | 675 us: 1.17x slower                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.68 ms: 1.17x slower                                        |
| meteor_contest                   | 47.7 ms                                                  | 56.0 ms: 1.17x slower                                        |
| sympy_expand                     | 167 ms                                                   | 197 ms: 1.18x slower                                         |
| genshi_xml                       | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                        |
| deltablue                        | 1.73 ms                                                  | 2.08 ms: 1.20x slower                                        |
| json_dumps                       | 4.26 ms                                                  | 5.13 ms: 1.21x slower                                        |
| richards                         | 22.4 ms                                                  | 27.1 ms: 1.21x slower                                        |
| fannkuch                         | 176 ms                                                   | 213 ms: 1.21x slower                                         |
| genshi_text                      | 10.5 ms                                                  | 12.7 ms: 1.21x slower                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.53 ms: 1.22x slower                                        |
| richards_super                   | 25.4 ms                                                  | 31.0 ms: 1.22x slower                                        |
| unpickle_pure_python             | 103 us                                                   | 127 us: 1.23x slower                                         |
| pickle_pure_python               | 139 us                                                   | 173 us: 1.24x slower                                         |
| pprint_safe_repr                 | 328 ms                                                   | 409 ms: 1.25x slower                                         |
| pprint_pformat                   | 665 ms                                                   | 836 ms: 1.26x slower                                         |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.6 ms: 1.26x slower                                        |
| async_tree_eager                 | 45.6 ms                                                  | 57.7 ms: 1.27x slower                                        |
| scimark_lu                       | 51.3 ms                                                  | 65.4 ms: 1.27x slower                                        |
| hexiom                           | 3.04 ms                                                  | 3.92 ms: 1.29x slower                                        |
| mako                             | 4.77 ms                                                  | 6.22 ms: 1.30x slower                                        |
| django_template                  | 13.6 ms                                                  | 17.9 ms: 1.32x slower                                        |
| nbody                            | 54.2 ms                                                  | 72.6 ms: 1.34x slower                                        |
| telco                            | 2.61 ms                                                  | 3.56 ms: 1.36x slower                                        |
| coverage                         | 26.9 ms                                                  | 38.0 ms: 1.42x slower                                        |
| bench_thread_pool                | 419 us                                                   | 626 us: 1.49x slower                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.6 ms: 2.79x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.01x slower                                                 |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (5) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.010x slower

# HPT report

- Reliability score: 99.24% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x