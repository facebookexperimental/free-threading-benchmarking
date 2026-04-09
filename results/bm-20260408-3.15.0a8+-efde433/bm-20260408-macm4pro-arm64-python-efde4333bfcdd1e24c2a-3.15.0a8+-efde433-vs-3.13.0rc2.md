# Results vs. 3.13.0rc2

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: darwin-arm64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.3 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 392 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.4 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.6 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.6 ms: 1.18x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 817 ms: 1.22x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| json_loads          | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| pickle_pure_python  | 130 us                                                         | 139 us: 1.06x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.64 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 532 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| k_core                           | 1.46 sec                                                       | 895 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.9 us: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| go                               | 72.6 ms                                                        | 51.9 ms: 1.40x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.39x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.4 ms: 1.33x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 817 ms: 1.22x faster                                                     |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                    |
| float                            | 31.4 ms                                                        | 26.6 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.3 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| fannkuch                         | 179 ms                                                         | 167 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 392 ms: 1.04x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 42.0 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 955 us: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.95 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.64 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 313 ms: 1.03x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 634 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 932 ns: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.6 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.43 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.6 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.00 us: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| 2to3                             | 112 ms                                                         | 117 ms: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.06x slower                                                     |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.4 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.19x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.44 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.6 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (3): unpickle_pure_python, typing_runtime_protocols, chaos
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260408-3.15.0a8+-efde433/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.19x