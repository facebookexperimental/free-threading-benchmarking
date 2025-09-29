# Results vs. 3.13.0rc2

- fork: python
- ref: d3e3b2b0ac23e30e3d24
- machine: darwin-arm64
- commit hash: d3e3b2b
- commit date: 2025-09-28
- overall geometric mean: 1.002x faster
- HPT reliability: 72.37%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 990 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.0 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.54 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.93 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.7 ms: 1.15x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| mako            | 4.41 ms                                                        | 5.93 ms: 1.34x slower                                                   |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 760 us: 2.68x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 479 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.02x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 602 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.0 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 999 ms: 1.46x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.5 us: 1.22x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                   |
| go                               | 72.6 ms                                                        | 62.8 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 849 ns: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 990 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                   |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.54 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.1 ms: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.12x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.21 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.9 ns: 1.13x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 365 ms: 1.13x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 742 ms: 1.14x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.7 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.84 us: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.93 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 75.7 us: 1.17x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.5 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.5 ms: 1.20x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 57.4 ms: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.46 us: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.24 ms: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.0 ms: 1.31x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.93 ms: 1.34x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 557 us: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                   |
| many_optionals                   | 200 us                                                         | 340 us: 1.70x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.0 ms: 2.69x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 19.1 ms: 3.05x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250928-3.15.0a0-d3e3b2b-NOGIL/bm-20250928-macm4pro-arm64-python-d3e3b2b0ac23e30e3d24-3.15.0a0-d3e3b2b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 72.37% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x