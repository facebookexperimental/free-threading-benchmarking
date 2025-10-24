# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: interp_tls
- machine: darwin-arm64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.030x faster
- HPT reliability: 94.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                   |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                 |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                  |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.30x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 227 ms: 2.30x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.78x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.69x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 100.0 ms: 1.33x faster                                                 |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.6 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.3 ms: 2.84x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                  |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                   |
| nbody          | 42.5 ms                                                        | 49.6 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                          | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                  |
| regex_v8       | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                  |
| regex_dna      | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                  |
| regex_compile  | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                          | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                  |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                  |
| tomli_loads          | 1000 ms                                                        | 899 ms: 1.11x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                  |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                  |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                  |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                  |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                  |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.90 ms: 1.01x faster                                                  |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                  |
| mako            | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                  |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                  |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.30x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 227 ms: 2.30x faster                                                   |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.78x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.69x faster                                                   |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.0 us: 1.37x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 100.0 ms: 1.33x faster                                                 |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 142 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                  |
| go                               | 72.6 ms                                                        | 56.5 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                  |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 899 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                  |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 915 us: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                 |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                  |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.4 ms: 1.03x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 19.3 ms: 1.03x faster                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                  |
| xml_etree_generate               | 35.8 ms                                                        | 35.0 ms: 1.02x faster                                                  |
| richards_super                   | 24.7 ms                                                        | 24.2 ms: 1.02x faster                                                  |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.6 ms: 1.01x faster                                                  |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                  |
| hexiom                           | 2.85 ms                                                        | 2.82 ms: 1.01x faster                                                  |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                 |
| genshi_text                      | 9.97 ms                                                        | 9.90 ms: 1.01x faster                                                  |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                  |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                   |
| bench_thread_pool                | 412 us                                                         | 415 us: 1.01x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                  |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                  |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                  |
| pprint_safe_repr                 | 322 ms                                                         | 326 ms: 1.01x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 661 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 65.9 us: 1.02x slower                                                  |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                  |
| regex_compile                    | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                  |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                  |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 978 ns: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                  |
| logging_silent                   | 40.6 ns                                                        | 42.0 ns: 1.03x slower                                                  |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.04x slower                                                  |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.05x slower                                                  |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                  |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                  |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.06x slower                                                  |
| nqueens                          | 37.2 ms                                                        | 39.8 ms: 1.07x slower                                                  |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.08x slower                                                  |
| mako                             | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                  |
| sympy_sum                        | 52.3 ms                                                        | 57.0 ms: 1.09x slower                                                  |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.44 us: 1.09x slower                                                  |
| bench_mp_pool                    | 37.8 ms                                                        | 41.4 ms: 1.09x slower                                                  |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.6 ms: 1.11x slower                                                  |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                  |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.6 ms: 1.17x slower                                                  |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                  |
| many_optionals                   | 200 us                                                         | 368 us: 1.83x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.3 ms: 2.84x slower                                                  |
| subparsers                       | 6.26 ms                                                        | 18.0 ms: 2.87x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                           |

Benchmark hidden because not significant (4): json, sympy_integrate, spectral_norm, xml_etree_parse
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251024-3.15.0a1+-04318d0/bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 94.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x