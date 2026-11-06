# Results vs. 3.13.0rc2

- fork: python
- ref: d7465429a2becbdf0856
- machine: darwin-arm64
- commit hash: d746542
- commit date: 2026-11-05
- overall geometric mean: 1.004x slower
- HPT reliability: 85.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                       |
| sphinx         | 409 ms                                                         | 442 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                          | 1.04x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 295 ms: 1.76x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 299 ms: 1.75x faster                                                        |
| async_generators                 | 193 ms                                                         | 113 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 299 ms: 1.36x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 300 ms: 1.29x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 141 ms: 1.06x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.14x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.51x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.93x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                                |

Benchmark hidden because not significant (4): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 146 ms: 1.13x faster                                                        |
| float          | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                       |
| nbody          | 42.5 ms                                                        | 59.9 ms: 1.41x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.10 ms: 1.18x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.4 ms: 1.06x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.6 ms: 1.33x slower                                                       |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 878 ms: 1.14x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.3 ms: 1.15x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.67 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                       |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.29x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 461 us: 2.15x faster                                                        |
| pylint                           | 106 ms                                                         | 51.5 ms: 2.05x faster                                                       |
| mdp                              | 1.06 sec                                                       | 581 ms: 1.82x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 295 ms: 1.76x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 299 ms: 1.75x faster                                                        |
| async_generators                 | 193 ms                                                         | 113 ms: 1.71x faster                                                        |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.26 ms: 1.47x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 299 ms: 1.36x faster                                                        |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 300 ms: 1.29x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| go                               | 72.6 ms                                                        | 59.8 ms: 1.21x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 54.1 us: 1.20x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.10 ms: 1.18x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 878 ms: 1.14x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 14.5 us: 1.14x faster                                                       |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                        |
| pidigits                         | 166 ms                                                         | 146 ms: 1.13x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.13x faster                                                      |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 57.7 ms: 1.11x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 89.4 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                        |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                      |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                       |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                       |
| telco                            | 3.07 ms                                                        | 3.08 ms: 1.00x slower                                                       |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                       |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                        |
| float                            | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 141 ms: 1.06x slower                                                        |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 8.07 ms: 1.07x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 40.7 ms: 1.08x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 347 ms: 1.08x slower                                                        |
| sphinx                           | 409 ms                                                         | 442 ms: 1.08x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.67 us: 1.09x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                       |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.67 ms: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.0 ms: 1.12x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 728 ms: 1.12x slower                                                        |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                       |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.14x slower                                                       |
| connected_components             | 208 ms                                                         | 237 ms: 1.14x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 470 us: 1.14x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.3 ms: 1.15x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.16x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 43.4 ms: 1.16x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.6 ms: 1.18x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.19x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.28 us: 1.22x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.8 ns: 1.23x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.78 ms: 1.23x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.5 ms: 1.23x slower                                                       |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.53 ms: 1.25x slower                                                       |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                        |
| coverage                         | 31.2 ms                                                        | 41.3 ms: 1.32x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 63.6 ms: 1.33x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                       |
| nbody                            | 42.5 ms                                                        | 59.9 ms: 1.41x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.2 ms: 1.48x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.51x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 66.1 ms: 1.55x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.93x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (4): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_eager_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261105-3.16.0a1+dev-d746542-NOGIL/bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 85.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x