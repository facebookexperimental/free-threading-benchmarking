# Results vs. 3.12.6

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: cc6b62a
- commit date: 2025-11-17
- overall geometric mean: 1.138x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                     |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.04x faster                                    |
| sphinx         | 434 ms                                                   | 407 ms: 1.07x faster                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                     |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.5 ms: 1.80x faster                                    |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.09x faster                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.4 ms: 2.50x slower                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                     |
| nbody          | 54.2 ms                                                  | 53.9 ms: 1.01x faster                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.5 ms: 1.23x faster                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                    |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                    |
| regex_v8       | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                    |
| tomli_loads          | 957 ms                                                   | 810 ms: 1.18x faster                                     |
| xml_etree_process    | 26.7 ms                                                  | 23.4 ms: 1.14x faster                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                    |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                    |
| unpickle_pure_python | 103 us                                                   | 92.4 us: 1.11x faster                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.0 ms: 1.10x faster                                    |
| pickle_pure_python   | 139 us                                                   | 130 us: 1.07x faster                                     |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.03x faster                                    |
| Geometric mean       | (ref)                                                    | 1.13x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.35 ms: 1.10x faster                                    |
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                    |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                     |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.5 ms: 1.80x faster                                    |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                    |
| mdp                              | 1.09 sec                                                 | 609 ms: 1.79x faster                                     |
| deepcopy_memo                    | 18.3 us                                                  | 10.9 us: 1.68x faster                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                     |
| deepcopy                         | 161 us                                                   | 100.0 us: 1.62x faster                                   |
| richards                         | 22.4 ms                                                  | 14.2 ms: 1.58x faster                                    |
| richards_super                   | 25.4 ms                                                  | 16.3 ms: 1.56x faster                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                     |
| comprehensions                   | 9.84 us                                                  | 7.23 us: 1.36x faster                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                    |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                     |
| regex_compile                    | 54.6 ms                                                  | 44.5 ms: 1.23x faster                                    |
| go                               | 70.0 ms                                                  | 57.1 ms: 1.23x faster                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                    |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                     |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                     |
| tomli_loads                      | 957 ms                                                   | 810 ms: 1.18x faster                                     |
| subparsers                       | 20.8 ms                                                  | 17.7 ms: 1.17x faster                                    |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                    |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                    |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                     |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.4 ms: 1.14x faster                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                    |
| pprint_pformat                   | 665 ms                                                   | 582 ms: 1.14x faster                                     |
| pprint_safe_repr                 | 328 ms                                                   | 287 ms: 1.14x faster                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                     |
| spectral_norm                    | 54.4 ms                                                  | 48.2 ms: 1.13x faster                                    |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                    |
| unpickle_pure_python             | 103 us                                                   | 92.4 us: 1.11x faster                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.11x faster                                   |
| mako                             | 4.77 ms                                                  | 4.35 ms: 1.10x faster                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.0 ms: 1.10x faster                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.09x faster                                    |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.5 us: 1.08x faster                                    |
| pickle_pure_python               | 139 us                                                   | 130 us: 1.07x faster                                     |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                     |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                     |
| sphinx                           | 434 ms                                                   | 407 ms: 1.07x faster                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                     |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                    |
| logging_silent                   | 50.9 ns                                                  | 48.4 ns: 1.05x faster                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                    |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.04x faster                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.03x faster                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.02 ms: 1.03x faster                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                     |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                    |
| nqueens                          | 43.5 ms                                                  | 42.6 ms: 1.02x faster                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.3 ms: 1.02x faster                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                     |
| sqlite_synth                     | 967 ns                                                   | 950 ns: 1.02x faster                                     |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                     |
| nbody                            | 54.2 ms                                                  | 53.9 ms: 1.01x faster                                    |
| regex_v8                         | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                    |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                     |
| dask                             | 528 ms                                                   | 545 ms: 1.03x slower                                     |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.36 ms: 1.04x slower                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                    |
| telco                            | 2.61 ms                                                  | 2.76 ms: 1.06x slower                                    |
| sympy_expand                     | 167 ms                                                   | 179 ms: 1.07x slower                                     |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                    |
| create_gc_cycles                 | 830 us                                                   | 908 us: 1.09x slower                                     |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                     |
| coverage                         | 26.9 ms                                                  | 33.4 ms: 1.24x slower                                    |
| many_optionals                   | 195 us                                                   | 361 us: 1.85x slower                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.4 ms: 2.50x slower                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                             |

Benchmark hidden because not significant (3): pylint, meteor_contest, fannkuch
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251117-3.15.0a1+-cc6b62a-JIT/bm-20251117-macm4pro-arm64-python-main-3.15.0a1+-cc6b62a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.138x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.25x