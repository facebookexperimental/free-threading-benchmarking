# Results vs. 3.13.0rc2

- fork: python
- ref: cb8a72b301f47e76d93a
- machine: darwin-arm64
- commit hash: cb8a72b
- commit date: 2025-05-30
- overall geometric mean: 1.017x faster
- HPT reliability: 61.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 989 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.6 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.0 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.0 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.51 ms: 1.03x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 991 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.3 us: 1.14x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.41 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.86 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.66 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 761 us: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 481 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 562 ms: 1.88x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.6 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.6 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 819 ns: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 989 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.51 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 991 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                   |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.95 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.03 ms: 1.07x slower                                                   |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.30 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.41 ms: 1.09x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.4 ms: 1.11x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.3 us: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.7 us: 1.14x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.2 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.86 ms: 1.15x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.89 us: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.0 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 381 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 778 ms: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.25x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.82 us: 1.26x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.10 us: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.66 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.5 ms: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.0 ms: 1.32x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 596 us: 1.45x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.63 ms: 1.54x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 68.3 ms: 1.60x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.0 ms: 2.66x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 215 ns: 5.30x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (3): pathlib, pycparser, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250530-3.15.0a0-cb8a72b-NOGIL/bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 61.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x