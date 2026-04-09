# Results vs. 3.12.6

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: darwin-arm64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.164x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                    |
| sphinx         | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.4 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.6 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.6 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.9 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| tomli_loads          | 957 ms                                                   | 817 ms: 1.17x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.75 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.3 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 139 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.64 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.02 ms: 5.16x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| mdp                              | 1.09 sec                                                 | 532 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.4 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.9 us: 1.63x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                    |
| float                            | 37.9 ms                                                  | 26.6 ms: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.00 us: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| go                               | 70.0 ms                                                  | 51.9 ms: 1.35x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.0 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| k_core                           | 1.12 sec                                                 | 895 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.1 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.20x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 45.9 ms: 1.19x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.6 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.6 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 817 ms: 1.17x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.75 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 392 ms: 1.11x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.6 us: 1.10x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.64 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| fannkuch                         | 176 ms                                                   | 167 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 634 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 932 ns: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.3 us: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.04x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.4 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 139 us: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                    |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                     |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.95 ms: 1.13x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 955 us: 1.15x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.44 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.6 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (2): pidigits, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260408-3.15.0a8+-efde433/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.164x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.24x