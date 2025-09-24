# Results vs. 3.12.6

- fork: python
- ref: 1a2e00c97acfe9f79722
- machine: darwin-arm64
- commit hash: 1a2e00c
- commit date: 2025-09-23
- overall geometric mean: 1.104x faster
- HPT reliability: 99.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 966 ms: 1.06x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.33x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 84.3 ms: 2.04x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.90x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 97.6 ms: 1.83x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 237 ms: 1.41x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.8 ms: 1.05x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.1 ms: 2.37x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.40x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                    |
| nbody          | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.5 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.4 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 56.4 ms: 1.20x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                   |
| tomli_loads          | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.50 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 745 us: 2.70x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.33x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 84.3 ms: 2.04x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 122 ms: 1.90x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 97.6 ms: 1.83x faster                                                   |
| mdp                              | 1.09 sec                                                 | 599 ms: 1.82x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 466 us: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 230 ms: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                   |
| deepcopy                         | 161 us                                                   | 114 us: 1.41x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 237 ms: 1.41x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                   |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.4 ms: 1.20x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.22 us: 1.20x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 813 ns: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 60.9 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.5 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.5 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 966 ms: 1.06x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.4 ms: 1.04x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.48 us: 1.04x faster                                                   |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.93 ms: 1.01x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 43.6 ms: 1.00x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.1 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 59.8 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.8 us: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 223 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.8 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.06x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 708 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 56.3 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 224 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.50 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 590 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.48x slower                                                   |
| many_optionals                   | 195 us                                                   | 326 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.1 ms: 2.37x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): chaos, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250923-3.15.0a0-1a2e00c-NOGIL/bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 99.64% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x