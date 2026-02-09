# Results vs. 3.12.6

- fork: python
- ref: 432ddd99e2b06a75a4f4
- machine: darwin-arm64
- commit hash: 432ddd9
- commit date: 2026-02-09
- overall geometric mean: 1.107x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 415 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.7 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.9 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| nbody          | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| tomli_loads          | 957 ms                                                   | 883 ms: 1.08x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.07 ms: 5.10x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 785 us: 2.56x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 596 ms: 1.83x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 511 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 789 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.25 us: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.3 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 53.9 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 883 ms: 1.08x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.64 us: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.05x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.2 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 322 ms: 1.02x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 656 ms: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.04 ms: 1.00x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.7 ms: 1.00x slower                                                    |
| json                             | 1.93 ms                                                  | 1.94 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.6 us: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.7 ms: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.0 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 333 us: 1.04x slower                                                     |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.10x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.8 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 562 us: 1.34x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.9 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260209-3.15.0a5+-432ddd9-NOGIL/bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.107x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.36x