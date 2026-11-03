# Results vs. 3.13.0rc2

- fork: python
- ref: 3945eaf2fcd9cbc3f306
- machine: darwin-arm64
- commit hash: 3945eaf
- commit date: 2026-11-03
- overall geometric mean: 1.000x slower
- HPT reliability: 80.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 442 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 293 ms: 1.79x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 292 ms: 1.79x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.74x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 296 ms: 1.37x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 295 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 282 ms: 1.07x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.05x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 284 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.6 ms: 1.18x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 152 ms: 1.49x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 112 ms: 3.85x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                        |
| float          | 31.4 ms                                                        | 32.5 ms: 1.03x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.2 ms: 1.37x slower                                                       |
| Geometric mean | (ref)                                                          | 1.11x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.01 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.8 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.7 ms: 1.33x slower                                                       |
| Geometric mean | (ref)                                                          | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 857 ms: 1.17x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.5 ms: 1.16x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.20x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.29x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 760 us: 2.69x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 458 us: 2.17x faster                                                        |
| pylint                           | 106 ms                                                         | 51.7 ms: 2.04x faster                                                       |
| mdp                              | 1.06 sec                                                       | 574 ms: 1.84x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 293 ms: 1.79x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 292 ms: 1.79x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.74x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.20 ms: 1.49x faster                                                       |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 296 ms: 1.37x faster                                                        |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 295 ms: 1.31x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                       |
| go                               | 72.6 ms                                                        | 59.3 ms: 1.22x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.7 us: 1.20x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.01 ms: 1.19x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 857 ms: 1.17x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 818 ns: 1.16x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                       |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| scimark_sor                      | 64.0 ms                                                        | 57.6 ms: 1.11x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 282 ms: 1.07x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 88.8 ms: 1.07x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.05x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 284 ms: 1.03x faster                                                        |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                        |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                      |
| dulwich_log                      | 19.8 ms                                                        | 19.4 ms: 1.02x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                       |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                        |
| telco                            | 3.07 ms                                                        | 3.11 ms: 1.01x slower                                                       |
| pycparser                        | 470 ms                                                         | 482 ms: 1.03x slower                                                        |
| float                            | 31.4 ms                                                        | 32.5 ms: 1.03x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 40.1 ms: 1.06x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 8.05 ms: 1.07x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.07x slower                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 347 ms: 1.08x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                       |
| sphinx                           | 409 ms                                                         | 442 ms: 1.08x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.66 us: 1.09x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                       |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                        |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.10x slower                                                       |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                       |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                        |
| pathlib                          | 11.1 ms                                                        | 12.4 ms: 1.12x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 726 ms: 1.12x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.12x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 470 us: 1.14x slower                                                        |
| connected_components             | 208 ms                                                         | 237 ms: 1.14x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 42.7 ms: 1.15x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.5 ms: 1.16x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.17x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.6 ms: 1.18x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.17 us: 1.20x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.20x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.75 ms: 1.21x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 40.8 ms: 1.21x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.3 ns: 1.21x slower                                                       |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                       |
| raytrace                         | 109 ms                                                         | 137 ms: 1.25x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                       |
| coverage                         | 31.2 ms                                                        | 41.4 ms: 1.33x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 63.7 ms: 1.33x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.2 ms: 1.37x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.1 ms: 1.47x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 152 ms: 1.49x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 68.1 ms: 1.59x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 112 ms: 3.85x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                                |

Benchmark hidden because not significant (4): async_tree_memoization, json, async_tree_eager_memoization, json_loads
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261103-3.16.0a1+dev-3945eaf-NOGIL/bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 80.20% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x