# Results vs. 3.13.0rc2

- fork: python
- ref: 945bf8ce1bf7ee388175
- machine: darwin-arm64
- commit hash: 945bf8c
- commit date: 2026-02-12
- overall geometric mean: 1.012x faster
- HPT reliability: 53.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| sphinx         | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.8 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.5 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 883 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.89 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.17 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| mako            | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 813 us: 2.51x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.15x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 511 us: 1.94x faster                                                     |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.13 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 60.5 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 790 ns: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.6 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 883 ms: 1.13x faster                                                     |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.03 sec: 1.05x faster                                                   |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 466 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 664 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 424 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.6 ns: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.8 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.8 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| shortest_path                    | 225 ms                                                         | 254 ms: 1.13x slower                                                     |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.6 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.89 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.0 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| raytrace                         | 109 ms                                                         | 130 ms: 1.19x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.17 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.28 us: 1.22x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.2 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.52 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 43.5 ms: 1.29x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.6 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 267 us: 1.33x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 554 us: 1.34x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.4 ms: 1.36x slower                                                    |
| connected_components             | 208 ms                                                         | 302 ms: 1.45x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.5 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (2): coroutines, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260212-3.15.0a6+-945bf8c-NOGIL/bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 53.70% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x