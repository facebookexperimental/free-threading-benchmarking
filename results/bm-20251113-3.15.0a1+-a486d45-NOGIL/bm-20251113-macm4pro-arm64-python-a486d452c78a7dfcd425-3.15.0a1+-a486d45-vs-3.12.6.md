# Results vs. 3.12.6

- fork: python
- ref: a486d452c78a7dfcd425
- machine: darwin-arm64
- commit hash: a486d45
- commit date: 2025-11-13
- overall geometric mean: 1.100x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.6 ms: 1.99x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.5 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.6 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.2 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                    |
| tomli_loads          | 957 ms                                                   | 877 ms: 1.09x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.76 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                    |
| django_template | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.58x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.6 ms: 1.99x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 491 us: 1.69x faster                                                     |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                     |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.08 us: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.21 us: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.6 ms: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.1 ns: 1.15x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 840 ns: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.6 ms: 1.12x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.8 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.7 ms: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 877 ms: 1.09x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.6 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.2 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.8 ms: 1.01x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.6 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.1 us: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.0 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 336 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 688 ms: 1.03x slower                                                     |
| thrift                           | 322 us                                                   | 335 us: 1.04x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.5 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.04x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.3 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| dask                             | 528 ms                                                   | 560 ms: 1.06x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.24 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.1 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.2 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.76 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 66.4 ms: 1.29x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 555 us: 1.33x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                    |
| many_optionals                   | 195 us                                                   | 379 us: 1.94x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): sympy_integrate
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251113-3.15.0a1+-a486d45-NOGIL/bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.36x