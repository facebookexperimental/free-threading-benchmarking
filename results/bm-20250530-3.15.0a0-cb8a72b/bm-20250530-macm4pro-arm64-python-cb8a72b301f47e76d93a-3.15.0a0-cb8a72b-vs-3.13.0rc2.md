# Results vs. 3.13.0rc2

- fork: python
- ref: cb8a72b301f47e76d93a
- machine: darwin-arm64
- commit hash: cb8a72b
- commit date: 2025-05-30
- overall geometric mean: 1.029x faster
- HPT reliability: 96.29%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 920 ms: 1.09x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.6 ms: 1.06x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.48 ms: 1.04x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.9 us: 1.03x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.1 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.60 ms: 1.00x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.16 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.84 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 511 ms: 2.07x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 949 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                   |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| go                               | 72.6 ms                                                        | 55.9 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.9 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 920 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 936 us: 1.06x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.6 ms: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.05x faster                                                   |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.48 ms: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 96.9 us: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.35 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.1 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.84 ms: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.4 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.60 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.00x slower                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.16 ms: 1.03x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 45.6 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 491 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.1 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.43 us: 1.09x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 717 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.9 ms: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.75 us: 1.13x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.9 ms: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.68 ms: 1.55x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 195 ns: 4.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (4): sphinx, regex_compile, sqlite_synth, meteor_contest
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250530-3.15.0a0-cb8a72b/bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 96.29% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x