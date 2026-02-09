# Results vs. 3.13.0rc2

- fork: python
- ref: 432ddd99e2b06a75a4f4
- machine: darwin-arm64
- commit hash: 432ddd9
- commit date: 2026-02-09
- overall geometric mean: 1.027x faster
- HPT reliability: 69.32%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 415 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.9 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 883 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 57.8 ms: 1.08x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 785 us: 2.60x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 511 us: 1.94x faster                                                     |
| mdp                              | 1.06 sec                                                       | 596 ms: 1.77x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.3 ms: 1.22x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 789 ns: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 53.9 ms: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 883 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.8 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 656 ms: 1.01x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 415 ms: 1.01x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.7 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.0 ms: 1.05x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.04 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.64 us: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.6 us: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.69 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.4 ms: 1.13x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.2 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.18x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.25 us: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 260 us: 1.30x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 56.8 ms: 1.33x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.9 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 562 us: 1.36x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.9 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): json, pprint_safe_repr
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260209-3.15.0a5+-432ddd9-NOGIL/bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5+-432ddd9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 69.32% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x