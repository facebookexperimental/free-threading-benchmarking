# Results vs. 3.13.0rc2

- fork: python
- ref: ef1fce0a69a19360643f
- machine: darwin-arm64
- commit hash: ef1fce0
- commit date: 2026-10-29
- overall geometric mean: 1.010x faster
- HPT reliability: 67.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 438 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 286 ms: 1.83x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 284 ms: 1.83x faster                                                        |
| async_generators                 | 193 ms                                                         | 109 ms: 1.78x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 288 ms: 1.41x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 294 ms: 1.32x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.06x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 287 ms: 1.05x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.3 ms: 1.14x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 262 ms: 1.26x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.71x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                                |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed, async_tree_eager_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| float          | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.2 ms: 1.37x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.5 ms: 1.06x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 62.8 ms: 1.31x slower                                                       |
| Geometric mean | (ref)                                                          | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 870 ms: 1.15x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 28.8 ms: 1.14x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                       |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 754 us: 2.71x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 455 us: 2.18x faster                                                        |
| pylint                           | 106 ms                                                         | 50.7 ms: 2.08x faster                                                       |
| mdp                              | 1.06 sec                                                       | 571 ms: 1.85x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 286 ms: 1.83x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 284 ms: 1.83x faster                                                        |
| async_generators                 | 193 ms                                                         | 109 ms: 1.78x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.22 ms: 1.49x faster                                                       |
| k_core                           | 1.46 sec                                                       | 999 ms: 1.46x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 288 ms: 1.41x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 294 ms: 1.32x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.67 ms: 1.27x faster                                                       |
| go                               | 72.6 ms                                                        | 58.9 ms: 1.23x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.4 us: 1.21x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 870 ms: 1.15x faster                                                        |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 57.5 ms: 1.11x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| xml_etree_parse                  | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.06x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 89.5 ms: 1.06x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 287 ms: 1.05x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                       |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                        |
| float                            | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.96 ms: 1.06x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                       |
| sphinx                           | 409 ms                                                         | 438 ms: 1.07x slower                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 346 ms: 1.08x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.41 us: 1.08x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.64 us: 1.08x slower                                                       |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 52.0 ms: 1.09x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.09x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.4 ms: 1.09x slower                                                       |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 714 ms: 1.10x slower                                                        |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                        |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.13x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 468 us: 1.14x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 28.8 ms: 1.14x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.3 ms: 1.14x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.2 ms: 1.15x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                        |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.16x slower                                                       |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.03 us: 1.18x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.74 ms: 1.20x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.1 ns: 1.21x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 40.7 ms: 1.21x slower                                                       |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                       |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 262 ms: 1.26x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                       |
| coverage                         | 31.2 ms                                                        | 40.5 ms: 1.30x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 62.8 ms: 1.31x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.2 ms: 1.37x slower                                                       |
| generators                       | 15.7 ms                                                        | 22.7 ms: 1.45x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 62.4 ms: 1.46x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.71x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, json_loads, fannkuch, telco, async_tree_eager_cpu_io_mixed, async_tree_eager_memoization, async_tree_none_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261029-3.16.0a1+dev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 67.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.23x