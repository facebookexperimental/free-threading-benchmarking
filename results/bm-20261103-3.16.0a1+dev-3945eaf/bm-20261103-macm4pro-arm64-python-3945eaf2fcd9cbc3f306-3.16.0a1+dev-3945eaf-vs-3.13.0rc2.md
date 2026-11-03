# Results vs. 3.13.0rc2

- fork: python
- ref: 3945eaf2fcd9cbc3f306
- machine: darwin-arm64
- commit hash: 3945eaf
- commit date: 2026-11-03
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| docutils       | 1.05 sec                                                       | 894 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| sphinx         | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.3 ms: 1.96x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 280 ms: 1.86x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 276 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.44x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.86 ms: 1.09x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.2 ms: 1.16x faster                                                       |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| nbody          | 42.5 ms                                                        | 42.3 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.95 ms: 1.20x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.4 ms: 1.06x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 795 ms: 1.26x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.5 us: 1.08x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 7.94 ms: 1.09x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 501 ms: 2.11x faster                                                        |
| pylint                           | 106 ms                                                         | 50.2 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.3 ms: 1.96x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 280 ms: 1.86x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 617 us: 1.61x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.91 ms: 1.60x faster                                                       |
| deepcopy                         | 145 us                                                         | 95.2 us: 1.52x faster                                                       |
| k_core                           | 1.46 sec                                                       | 964 ms: 1.52x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 276 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.44x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                       |
| go                               | 72.6 ms                                                        | 51.3 ms: 1.41x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 45.9 us: 1.41x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 47.7 ms: 1.34x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 795 ms: 1.26x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| pyflate                          | 222 ms                                                         | 181 ms: 1.23x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 8.95 ms: 1.20x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.74 ms: 1.17x faster                                                       |
| docutils                         | 1.05 sec                                                       | 894 ms: 1.17x faster                                                        |
| float                            | 31.4 ms                                                        | 27.2 ms: 1.16x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.16x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.12x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.11x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.8 ms: 1.11x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                      |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 113 ms: 1.09x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.86 ms: 1.09x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.61 ms: 1.09x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 7.94 ms: 1.09x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.3 ms: 1.09x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 92.5 us: 1.08x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.0 ms: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                       |
| json                             | 1.94 ms                                                        | 1.83 ms: 1.06x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 89.4 ms: 1.06x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.93 ms: 1.04x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 908 ns: 1.04x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.24 ms: 1.04x faster                                                       |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.72 ms: 1.04x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.59 us: 1.03x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 630 ms: 1.03x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                       |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                        |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                        |
| nbody                            | 42.5 ms                                                        | 42.3 ms: 1.01x faster                                                       |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.01x slower                                                       |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 98.3 ms: 1.03x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.03x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 54.4 ms: 1.04x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 36.1 ms: 1.08x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.0 ms: 1.08x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.4 ms: 1.09x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                       |
| many_optionals                   | 200 us                                                         | 228 us: 1.14x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.20x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (4): shortest_path, connected_components, mako, logging_silent
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261103-3.16.0a1+dev-3945eaf/bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x