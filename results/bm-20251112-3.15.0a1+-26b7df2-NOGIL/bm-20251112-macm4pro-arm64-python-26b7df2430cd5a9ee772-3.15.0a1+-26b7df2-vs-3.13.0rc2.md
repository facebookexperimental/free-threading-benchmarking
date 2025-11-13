# Results vs. 3.13.0rc2

- fork: python
- ref: 26b7df2430cd5a9ee772
- machine: darwin-arm64
- commit hash: 26b7df2
- commit date: 2025-11-12
- overall geometric mean: 1.000x slower
- HPT reliability: 70.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.66x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.9 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.4 ms: 1.12x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmark hidden because not significant (2): coroutines, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.6 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.48 ms: 1.13x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 4.06 ms: 1.15x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.1 ms: 1.07x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 937 ms: 1.07x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.80 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.11 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                    |
| mako            | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.66x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 769 us: 2.65x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 483 us: 2.06x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 87.9 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| deepcopy                         | 145 us                                                         | 115 us: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| go                               | 72.6 ms                                                        | 60.8 ms: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.06 ms: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.9 ms: 1.14x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 836 ns: 1.13x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.48 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.1 ms: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 937 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.00x faster                                                     |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.8 ns: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 719 ms: 1.11x slower                                                     |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.4 ms: 1.12x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.80 ms: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.78 us: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.2 us: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.5 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.16x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 44.4 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 57.2 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.11 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                     |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.5 ms: 1.24x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.47 us: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.26 ms: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.4 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.6 ms: 1.31x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 68.0 ms: 1.59x slower                                                    |
| many_optionals                   | 200 us                                                         | 390 us: 1.95x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 19.2 ms: 3.07x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (3): coroutines, telco, async_tree_eager_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251112-3.15.0a1+-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1+-26b7df2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 70.18% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x