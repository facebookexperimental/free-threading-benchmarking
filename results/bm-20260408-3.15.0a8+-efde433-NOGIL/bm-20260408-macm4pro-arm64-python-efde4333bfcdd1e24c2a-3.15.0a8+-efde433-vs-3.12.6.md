# Results vs. 3.12.6

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: darwin-arm64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.104x faster
- HPT reliability: 99.90%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 977 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 57.6 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                    |
| tomli_loads          | 957 ms                                                   | 850 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.70 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.05 ms: 5.12x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 784 us: 2.56x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| mdp                              | 1.09 sec                                                 | 600 ms: 1.82x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 502 us: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.56x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 790 ns: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.21 us: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 59.3 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.2 ns: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 850 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 454 ms: 1.10x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.9 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.3 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 977 ms: 1.05x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 671 ms: 1.01x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.9 us: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 54.3 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| nbody                            | 54.2 ms                                                  | 57.6 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.23 ms: 1.08x slower                                                    |
| thrift                           | 322 us                                                   | 348 us: 1.08x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.8 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.5 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.2 ms: 1.19x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.70 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 262 us: 1.34x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 567 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (4): json, xml_etree_process, pprint_safe_repr, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 99.90% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.39x