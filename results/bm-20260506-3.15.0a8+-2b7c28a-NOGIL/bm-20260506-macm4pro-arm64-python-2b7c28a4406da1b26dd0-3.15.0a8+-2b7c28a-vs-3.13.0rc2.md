# Results vs. 3.13.0rc2

- fork: python
- ref: 2b7c28a4406da1b26dd0
- machine: darwin-arm64
- commit hash: 2b7c28a
- commit date: 2026-05-06
- overall geometric mean: 1.044x faster
- HPT reliability: 87.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 237 ms: 2.22x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 235 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_generators                 | 193 ms                                                         | 149 ms: 1.30x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.1 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.3 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 51.7 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 851 ms: 1.18x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.6 ms: 1.13x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.27x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 783 us: 2.61x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 237 ms: 2.22x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 235 ms: 2.21x faster                                                     |
| pylint                           | 106 ms                                                         | 50.8 ms: 2.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 509 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 589 ms: 1.79x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.18 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| async_generators                 | 193 ms                                                         | 149 ms: 1.30x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 58.6 ms: 1.24x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 802 ns: 1.18x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 851 ms: 1.18x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.1 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.6 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.90 sec: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 454 ms: 1.03x faster                                                     |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.2 ms: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.8 ns: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 687 ms: 1.06x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.03 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.1 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 51.7 ms: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.5 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.11x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.4 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.9 us: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.8 ms: 1.16x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.10 us: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.1 ms: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.9 ms: 1.33x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.38x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 61.5 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.3 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (2): dask, telco
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260506-3.15.0a8+-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 87.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x