# Results vs. 3.13.0rc2

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: darwin-arm64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.024x faster
- HPT reliability: 63.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 977 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.6 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 850 ms: 1.18x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 784 us: 2.60x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 502 us: 1.98x faster                                                     |
| mdp                              | 1.06 sec                                                       | 600 ms: 1.76x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.05 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.3 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 790 ns: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 850 ms: 1.18x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.9 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 977 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 454 ms: 1.03x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 671 ms: 1.03x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.3 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.2 ns: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                    |
| thrift                           | 309 us                                                         | 348 us: 1.13x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.9 us: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.0 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.21 us: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.2 ms: 1.25x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 54.3 ms: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.8 ms: 1.30x slower                                                    |
| many_optionals                   | 200 us                                                         | 262 us: 1.31x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.6 ms: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): json, coroutines
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 63.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x