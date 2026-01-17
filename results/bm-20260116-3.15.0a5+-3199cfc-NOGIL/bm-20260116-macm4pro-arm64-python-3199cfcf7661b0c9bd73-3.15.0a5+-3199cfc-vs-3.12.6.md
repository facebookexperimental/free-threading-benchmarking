# Results vs. 3.12.6

- fork: python
- ref: 3199cfcf7661b0c9bd73
- machine: darwin-arm64
- commit hash: 3199cfc
- commit date: 2026-01-16
- overall geometric mean: 1.095x faster
- HPT reliability: 99.66%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 423 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.0 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                    |
| tomli_loads          | 957 ms                                                   | 880 ms: 1.09x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.50 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.14 ms: 5.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 806 us: 2.49x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 245 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 606 ms: 1.80x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 511 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.30 us: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 816 ns: 1.19x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.1 ns: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 59.4 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 192 ms: 1.12x faster                                                     |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.12x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 880 ms: 1.09x faster                                                     |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                     |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 463 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.7 ms: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 423 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.4 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 331 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.11 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 678 ms: 1.02x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.0 ms: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                     |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.8 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 57.7 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.50 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.5 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.4 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 564 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 267 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.8 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (2): dask, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260116-3.15.0a5+-3199cfc-NOGIL/bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5+-3199cfc.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 99.66% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.36x