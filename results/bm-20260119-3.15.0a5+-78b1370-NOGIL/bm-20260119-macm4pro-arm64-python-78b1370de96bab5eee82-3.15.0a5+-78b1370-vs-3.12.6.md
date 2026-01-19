# Results vs. 3.12.6

- fork: python
- ref: 78b1370de96bab5eee82
- machine: darwin-arm64
- commit hash: 78b1370
- commit date: 2026-01-19
- overall geometric mean: 1.120x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 969 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.88x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.6 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| nbody          | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.6 ms: 1.10x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.1 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| tomli_loads          | 957 ms                                                   | 872 ms: 1.10x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.50 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.98 ms: 5.21x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 763 us: 2.63x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.88x faster                                                     |
| mdp                              | 1.09 sec                                                 | 591 ms: 1.85x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 489 us: 1.70x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.50x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.10 us: 1.22x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 809 ns: 1.20x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.0 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.1 ns: 1.18x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| raytrace                         | 145 ms                                                   | 125 ms: 1.16x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 189 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 53.9 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.3 ms: 1.10x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.6 ms: 1.10x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 872 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 453 ms: 1.10x faster                                                     |
| generators                       | 21.9 ms                                                  | 20.1 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.1 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 969 ms: 1.05x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 69.9 us: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.91 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.05 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.9 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.00x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 667 ms: 1.00x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.7 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.08 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 59.1 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 40.3 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 183 ms: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 57.3 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.8 ms: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.96 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.50 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 564 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.3 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 90.6 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (3): pprint_safe_repr, dask, async_tree_eager
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260119-3.15.0a5+-78b1370-NOGIL/bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.36x