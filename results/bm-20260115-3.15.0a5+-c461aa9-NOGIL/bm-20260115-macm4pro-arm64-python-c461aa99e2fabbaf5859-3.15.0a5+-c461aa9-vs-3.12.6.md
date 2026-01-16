# Results vs. 3.12.6

- fork: python
- ref: c461aa99e2fabbaf5859
- machine: darwin-arm64
- commit hash: c461aa9
- commit date: 2026-01-15
- overall geometric mean: 1.075x faster
- HPT reliability: 94.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.10x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.80x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.7 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.3 ms: 2.97x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 170 ms: 1.05x slower                                                     |
| nbody          | 54.2 ms                                                  | 58.5 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.7 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.03 ms: 1.06x faster                                                    |
| tomli_loads          | 957 ms                                                   | 922 ms: 1.04x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.31 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.27x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.10x slower                                                    |
| mako            | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| django_template | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.20 ms: 4.94x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 823 us: 2.44x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.80x faster                                                     |
| mdp                              | 1.09 sec                                                 | 614 ms: 1.78x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 524 us: 1.58x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.45x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.39 us: 1.17x faster                                                    |
| go                               | 70.0 ms                                                  | 60.5 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 843 ns: 1.15x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                   |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.03 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.7 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 122 ms: 1.05x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 922 ms: 1.04x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| chaos                            | 28.9 ms                                                  | 28.7 ms: 1.01x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 43.1 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 71.8 us: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 336 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.0 ms: 1.03x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.24 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.14 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 693 ms: 1.04x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.7 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                    |
| pidigits                         | 161 ms                                                   | 170 ms: 1.05x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.22 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 343 us: 1.07x slower                                                     |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.7 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.9 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                     |
| nbody                            | 54.2 ms                                                  | 58.5 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                    |
| 2to3                             | 114 ms                                                   | 126 ms: 1.10x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 254 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 56.9 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.4 ms: 1.19x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 62.0 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 248 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.31 ms: 1.28x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 563 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 276 us: 1.41x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.3 ms: 2.97x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (2): dask, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260115-3.15.0a5+-c461aa9-NOGIL/bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 94.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x