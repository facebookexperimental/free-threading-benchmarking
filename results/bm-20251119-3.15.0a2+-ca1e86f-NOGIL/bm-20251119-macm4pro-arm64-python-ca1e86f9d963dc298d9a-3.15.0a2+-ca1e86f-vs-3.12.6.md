# Results vs. 3.12.6

- fork: python
- ref: ca1e86f9d963dc298d9a
- machine: darwin-arm64
- commit hash: ca1e86f
- commit date: 2025-11-19
- overall geometric mean: 1.120x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 411 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 194 ms: 2.47x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.33x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.24x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 83.3 ms: 2.07x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 121 ms: 1.90x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 96.7 ms: 1.84x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 127 ms: 1.76x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 75.9 ms: 2.36x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.41x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.4 ms: 1.44x faster                                                    |
| nbody          | 54.2 ms                                                  | 53.7 ms: 1.01x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.0 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| tomli_loads          | 957 ms                                                   | 864 ms: 1.11x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.91 ms: 1.24x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.19 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.8 ms: 1.03x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.9 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.49 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 776 us: 2.59x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 194 ms: 2.47x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 191 ms: 2.33x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.24x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 83.3 ms: 2.07x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 121 ms: 1.90x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 96.7 ms: 1.84x faster                                                    |
| mdp                              | 1.09 sec                                                 | 601 ms: 1.82x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 127 ms: 1.76x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 481 us: 1.72x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                     |
| float                            | 37.9 ms                                                  | 26.4 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| go                               | 70.0 ms                                                  | 57.0 ms: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.03 us: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.8 ns: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 819 ns: 1.18x faster                                                     |
| raytrace                         | 145 ms                                                   | 123 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 48.2 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.8 ms: 1.11x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 864 ms: 1.11x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 18.7 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.0 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 459 ms: 1.08x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 411 ms: 1.06x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.5 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.02x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.98 ms: 1.02x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| nbody                            | 54.2 ms                                                  | 53.7 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 329 ms: 1.00x slower                                                     |
| richards                         | 22.4 ms                                                  | 22.5 ms: 1.00x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 673 ms: 1.01x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.6 ms: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.9 ms: 1.02x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.8 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 333 us: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 73.6 us: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 53.4 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 22.9 ms: 1.05x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.9 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| dask                             | 528 ms                                                   | 560 ms: 1.06x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 184 ms: 1.10x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.97 ms: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.49 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.2 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.4 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.91 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.19 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 547 us: 1.31x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.7 ms: 1.48x slower                                                    |
| many_optionals                   | 195 us                                                   | 374 us: 1.91x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 75.9 ms: 2.36x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (1): sympy_integrate
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251119-3.15.0a2+-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.36x