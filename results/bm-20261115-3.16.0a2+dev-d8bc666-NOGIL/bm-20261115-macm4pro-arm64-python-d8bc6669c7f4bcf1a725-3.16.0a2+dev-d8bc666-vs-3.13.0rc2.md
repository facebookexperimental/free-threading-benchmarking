# Results vs. 3.13.0rc2

- fork: python
- ref: d8bc6669c7f4bcf1a725
- machine: darwin-arm64
- commit hash: d8bc666
- commit date: 2026-11-15
- overall geometric mean: 1.011x slower
- HPT reliability: 91.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 127 ms: 1.14x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                      |
| sphinx         | 409 ms                                                         | 446 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                          | 1.05x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 297 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 301 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.73x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 302 ms: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.6 ms: 1.07x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 269 ms: 1.29x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 163 ms: 1.59x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.95x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 148 ms: 1.13x faster                                                        |
| float          | 31.4 ms                                                        | 33.2 ms: 1.06x slower                                                       |
| nbody          | 42.5 ms                                                        | 58.7 ms: 1.38x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.8 ms: 1.33x slower                                                       |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 882 ms: 1.13x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.4 ms: 1.11x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 60.4 ms: 1.03x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.3 ms: 1.16x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 157 us: 1.21x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.76 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                       |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 787 us: 2.59x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 472 us: 2.11x faster                                                        |
| pylint                           | 106 ms                                                         | 52.0 ms: 2.03x faster                                                       |
| mdp                              | 1.06 sec                                                       | 579 ms: 1.83x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 297 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 301 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.73x faster                                                        |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.28 ms: 1.46x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 302 ms: 1.34x faster                                                        |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| go                               | 72.6 ms                                                        | 60.0 ms: 1.21x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 54.2 us: 1.19x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 814 ns: 1.16x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 14.5 us: 1.14x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 882 ms: 1.13x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.13x faster                                                      |
| pidigits                         | 166 ms                                                         | 148 ms: 1.13x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.4 ms: 1.11x faster                                                       |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 58.3 ms: 1.10x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 60.4 ms: 1.03x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                      |
| dulwich_log                      | 19.8 ms                                                        | 19.6 ms: 1.01x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                       |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                       |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| pycparser                        | 470 ms                                                         | 491 ms: 1.04x slower                                                        |
| float                            | 31.4 ms                                                        | 33.2 ms: 1.06x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.6 ms: 1.07x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 8.16 ms: 1.08x slower                                                       |
| sphinx                           | 409 ms                                                         | 446 ms: 1.09x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 41.5 ms: 1.10x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.70 us: 1.10x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                        |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.3 ms: 1.13x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.76 ms: 1.14x slower                                                       |
| 2to3                             | 112 ms                                                         | 127 ms: 1.14x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 469 us: 1.14x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 741 ms: 1.14x slower                                                        |
| connected_components             | 208 ms                                                         | 238 ms: 1.14x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.3 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.17x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.8 ms: 1.19x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 157 us: 1.21x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.29 us: 1.22x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.79 ms: 1.23x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.7 ms: 1.24x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 50.5 ns: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                       |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 269 ms: 1.29x slower                                                        |
| coverage                         | 31.2 ms                                                        | 41.4 ms: 1.33x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 63.8 ms: 1.33x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                       |
| nbody                            | 42.5 ms                                                        | 58.7 ms: 1.38x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.6 ms: 1.50x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 66.4 ms: 1.55x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 163 ms: 1.59x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.95x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (5): async_tree_memoization, html5lib, json, async_tree_none, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261115-3.16.0a2+dev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 91.41% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x