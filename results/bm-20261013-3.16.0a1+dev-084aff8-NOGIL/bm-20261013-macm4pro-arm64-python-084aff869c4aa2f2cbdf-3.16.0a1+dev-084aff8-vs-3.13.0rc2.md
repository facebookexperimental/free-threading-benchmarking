# Results vs. 3.13.0rc2

- fork: python
- ref: 084aff869c4aa2f2cbdf
- machine: darwin-arm64
- commit hash: 084aff8
- commit date: 2026-10-13
- overall geometric mean: 1.015x slower
- HPT reliability: 89.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                       |
| sphinx         | 409 ms                                                         | 445 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                          | 1.05x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 291 ms: 1.79x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 294 ms: 1.78x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 294 ms: 1.38x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 302 ms: 1.28x faster                                                        |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.02x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.7 ms: 1.09x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 273 ms: 1.31x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 162 ms: 1.58x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 113 ms: 3.90x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (3): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                        |
| float          | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| nbody          | 42.5 ms                                                        | 57.7 ms: 1.36x slower                                                       |
| Geometric mean | (ref)                                                          | 1.12x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.9 ms: 1.33x slower                                                       |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 866 ms: 1.15x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.99 ms: 1.16x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.32 ms: 1.23x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.73 ms: 1.30x slower                                                       |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.33x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 781 us: 2.61x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 469 us: 2.12x faster                                                        |
| pylint                           | 106 ms                                                         | 53.0 ms: 1.99x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 291 ms: 1.79x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 294 ms: 1.78x faster                                                        |
| mdp                              | 1.06 sec                                                       | 597 ms: 1.77x faster                                                        |
| k_core                           | 1.46 sec                                                       | 999 ms: 1.47x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.30 ms: 1.46x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 294 ms: 1.38x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 302 ms: 1.28x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                       |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 795 ns: 1.19x faster                                                        |
| go                               | 72.6 ms                                                        | 61.1 ms: 1.19x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 866 ms: 1.15x faster                                                        |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 57.2 us: 1.13x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.10x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 58.2 ms: 1.10x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                       |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                       |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                        |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 19.7 ms: 1.01x faster                                                       |
| telco                            | 3.07 ms                                                        | 3.08 ms: 1.01x slower                                                       |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.02x slower                                                        |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                        |
| float                            | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 11.7 ms: 1.09x slower                                                       |
| sphinx                           | 409 ms                                                         | 445 ms: 1.09x slower                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.3 ms: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.48 us: 1.11x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                       |
| thrift                           | 309 us                                                         | 346 us: 1.12x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.7 ms: 1.12x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.13x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 733 ms: 1.13x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                       |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.25 ms: 1.14x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 42.7 ms: 1.15x slower                                                       |
| connected_components             | 208 ms                                                         | 240 ms: 1.15x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.16x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 9.99 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                        |
| chaos                            | 24.3 ms                                                        | 29.0 ms: 1.20x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.1 ms: 1.22x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.7 ns: 1.22x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.32 ms: 1.23x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.79 ms: 1.24x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                       |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                        |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                        |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                       |
| mako                             | 4.41 ms                                                        | 5.73 ms: 1.30x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 273 ms: 1.31x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 63.9 ms: 1.33x slower                                                       |
| nbody                            | 42.5 ms                                                        | 57.7 ms: 1.36x slower                                                       |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                        |
| generators                       | 15.7 ms                                                        | 23.6 ms: 1.51x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 66.5 ms: 1.56x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 162 ms: 1.58x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 113 ms: 3.90x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (4): async_tree_none, async_tree_memoization, json_loads, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261013-3.16.0a1+dev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x slower

# HPT report

- Reliability score: 89.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.25x