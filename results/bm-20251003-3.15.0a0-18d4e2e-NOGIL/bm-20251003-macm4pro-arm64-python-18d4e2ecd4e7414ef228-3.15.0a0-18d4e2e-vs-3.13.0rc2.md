# Results vs. 3.13.0rc2

- fork: python
- ref: 18d4e2ecd4e7414ef228
- machine: darwin-arm64
- commit hash: 18d4e2e
- commit date: 2025-10-03
- overall geometric mean: 1.004x slower
- HPT reliability: 86.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.52x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.9 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.4 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| nbody          | 42.5 ms                                                        | 57.5 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.50 ms: 1.13x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.17x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.1 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 984 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.01 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| mako            | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 779 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.52x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 486 us: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                                    |
| mdp                              | 1.06 sec                                                       | 610 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.9 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.23x faster                                                   |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.17x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| go                               | 72.6 ms                                                        | 62.7 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 832 ns: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.50 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.1 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.02 sec: 1.06x faster                                                  |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 984 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.12 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                    |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| fannkuch                         | 179 ms                                                         | 187 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 357 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 725 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                   |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.6 ns: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.14x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.82 us: 1.15x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 74.8 us: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.01 ms: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.8 ms: 1.18x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.3 ms: 1.19x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 57.4 ms: 1.20x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.9 ms: 1.23x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                   |
| raytrace                         | 109 ms                                                         | 134 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.61 us: 1.27x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.3 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.2 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.7 ms: 1.33x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 553 us: 1.34x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.5 ms: 1.35x slower                                                   |
| many_optionals                   | 200 us                                                         | 348 us: 1.74x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.4 ms: 2.74x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 19.4 ms: 3.10x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (3): coroutines, deepcopy_reduce, pidigits
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251003-3.15.0a0-18d4e2e-NOGIL/bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 86.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x