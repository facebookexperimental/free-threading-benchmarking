# Results vs. 3.13.0rc2

- fork: python
- ref: d1d5dce14f90d777608e
- machine: darwin-arm64
- commit hash: d1d5dce
- commit date: 2025-07-04
- overall geometric mean: 1.018x faster
- HPT reliability: 74.92%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.4 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmark hidden because not significant (2): coroutines, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.20x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.1 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 976 ms: 1.02x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.59 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                   |
| django_template | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 804 us: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 496 us: 2.00x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 575 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.4 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                   |
| deepcopy                         | 145 us                                                         | 121 us: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| go                               | 72.6 ms                                                        | 60.6 ms: 1.20x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.20x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 815 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 58.1 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 976 ms: 1.02x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.59 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.1 ms: 1.05x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.06x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.01 ms: 1.06x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.26 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 343 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.03 ms: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 696 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                                   |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.6 us: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.17x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.93 us: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.61 us: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.90 us: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.6 ms: 1.27x slower                                                   |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.9 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.0 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.75 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): coroutines, pathlib, pycparser, async_tree_eager_cpu_io_mixed, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.018x faster

# HPT report

- Reliability score: 74.92% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x