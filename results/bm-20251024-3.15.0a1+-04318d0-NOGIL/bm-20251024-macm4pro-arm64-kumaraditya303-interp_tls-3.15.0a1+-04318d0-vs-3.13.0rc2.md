# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: interp_tls
- machine: darwin-arm64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.006x slower
- HPT reliability: 78.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                   |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                 |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                  |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 209 ms: 2.52x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.01x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 88.3 ms: 1.50x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.48x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                  |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                           |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                  |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                   |
| nbody          | 42.5 ms                                                        | 61.0 ms: 1.43x slower                                                  |
| Geometric mean | (ref)                                                          | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                  |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                  |
| regex_compile  | 47.9 ms                                                        | 53.9 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                          | 1.04x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                  |
| json_dumps           | 4.65 ms                                                        | 4.07 ms: 1.14x faster                                                  |
| xml_etree_parse      | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                  |
| tomli_loads          | 1000 ms                                                        | 977 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                  |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                  |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                  |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.74 ms: 1.13x slower                                                  |
| python_startup_no_site | 5.95 ms                                                        | 7.08 ms: 1.19x slower                                                  |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 25.2 ms: 1.18x slower                                                  |
| genshi_text     | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                  |
| mako            | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                  |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                  |
| Geometric mean  | (ref)                                                          | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 763 us: 2.68x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 209 ms: 2.52x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 474 us: 2.10x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 201 ms: 2.01x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 213 ms: 1.81x faster                                                   |
| mdp                              | 1.06 sec                                                       | 619 ms: 1.71x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 88.3 ms: 1.50x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.48x faster                                                   |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                  |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                  |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                   |
| go                               | 72.6 ms                                                        | 63.2 ms: 1.15x faster                                                  |
| json_dumps                       | 4.65 ms                                                        | 4.07 ms: 1.14x faster                                                  |
| scimark_sor                      | 64.0 ms                                                        | 56.6 ms: 1.13x faster                                                  |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                  |
| pyflate                          | 222 ms                                                         | 201 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                  |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.03 sec: 1.05x faster                                                 |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                  |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                 |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 977 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                  |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 477 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                  |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                  |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                  |
| fannkuch                         | 179 ms                                                         | 187 ms: 1.05x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                  |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.07x slower                                                  |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.08x slower                                                  |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                   |
| thrift                           | 309 us                                                         | 344 us: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.12x slower                                                  |
| pprint_pformat                   | 650 ms                                                         | 725 ms: 1.12x slower                                                   |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.9 ms: 1.12x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 9.74 ms: 1.13x slower                                                  |
| bench_mp_pool                    | 37.8 ms                                                        | 42.7 ms: 1.13x slower                                                  |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 46.0 ns: 1.13x slower                                                  |
| logging_simple                   | 2.24 us                                                        | 2.55 us: 1.14x slower                                                  |
| hexiom                           | 2.85 ms                                                        | 3.25 ms: 1.14x slower                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.2 ms: 1.14x slower                                                  |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.15x slower                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                  |
| logging_format                   | 2.45 us                                                        | 2.83 us: 1.16x slower                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 75.1 us: 1.16x slower                                                  |
| spectral_norm                    | 43.7 ms                                                        | 51.1 ms: 1.17x slower                                                  |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                  |
| genshi_xml                       | 21.4 ms                                                        | 25.2 ms: 1.18x slower                                                  |
| sympy_str                        | 95.5 ms                                                        | 113 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.9 ms: 1.19x slower                                                  |
| python_startup_no_site           | 5.95 ms                                                        | 7.08 ms: 1.19x slower                                                  |
| nqueens                          | 37.2 ms                                                        | 44.6 ms: 1.20x slower                                                  |
| genshi_text                      | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                  |
| sympy_expand                     | 159 ms                                                         | 193 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.9 ms: 1.23x slower                                                  |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                  |
| comprehensions                   | 6.80 us                                                        | 8.51 us: 1.25x slower                                                  |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.25 ms: 1.27x slower                                                  |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                  |
| coverage                         | 31.2 ms                                                        | 40.9 ms: 1.31x slower                                                  |
| mako                             | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                  |
| bench_thread_pool                | 412 us                                                         | 548 us: 1.33x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.9 ms: 1.33x slower                                                  |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                  |
| nbody                            | 42.5 ms                                                        | 61.0 ms: 1.43x slower                                                  |
| many_optionals                   | 200 us                                                         | 393 us: 1.96x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.5 ms: 2.75x slower                                                  |
| subparsers                       | 6.26 ms                                                        | 19.3 ms: 3.09x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                           |

Benchmark hidden because not significant (4): deepcopy_reduce, async_tree_eager_cpu_io_mixed, regex_dna, telco
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251024-3.15.0a1+-04318d0-NOGIL/bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 78.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x