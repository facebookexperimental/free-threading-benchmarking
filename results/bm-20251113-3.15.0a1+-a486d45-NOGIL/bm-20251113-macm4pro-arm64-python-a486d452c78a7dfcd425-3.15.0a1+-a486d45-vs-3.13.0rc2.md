# Results vs. 3.13.0rc2

- fork: python
- ref: a486d452c78a7dfcd425
- machine: darwin-arm64
- commit hash: a486d45
- commit date: 2025-11-13
- overall geometric mean: 1.014x faster
- HPT reliability: 51.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.6 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.5 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.6 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 877 ms: 1.14x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.5 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.76 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.09 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| mako            | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 777 us: 2.63x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 491 us: 2.02x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.85x faster                                                     |
| mdp                              | 1.06 sec                                                       | 610 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.6 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                     |
| go                               | 72.6 ms                                                        | 58.6 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.7 ms: 1.15x faster                                                    |
| float                            | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 877 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 840 ns: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.5 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 466 ms: 1.01x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.2 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.6 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.0 ms: 1.05x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 688 ms: 1.06x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| dask                             | 525 ms                                                         | 560 ms: 1.07x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 51.6 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 335 us: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.1 ns: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.5 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.1 us: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.76 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.3 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.8 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 43.8 ms: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.08 us: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.09 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.2 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.6 ms: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.24 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.1 ms: 1.29x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.2 ms: 1.30x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 555 us: 1.35x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 66.4 ms: 1.55x slower                                                    |
| many_optionals                   | 200 us                                                         | 379 us: 1.89x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.7 ms: 2.69x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.8 ms: 3.01x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, coroutines
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251113-3.15.0a1+-a486d45-NOGIL/bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1+-a486d45.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 51.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x