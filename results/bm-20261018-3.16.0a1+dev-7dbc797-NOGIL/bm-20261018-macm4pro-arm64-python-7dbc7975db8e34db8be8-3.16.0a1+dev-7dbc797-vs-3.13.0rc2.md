# Results vs. 3.13.0rc2

- fork: python
- ref: 7dbc7975db8e34db8be8
- machine: darwin-arm64
- commit hash: 7dbc797
- commit date: 2026-10-18
- overall geometric mean: 1.006x slower
- HPT reliability: 78.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 439 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 286 ms: 1.82x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 290 ms: 1.40x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 294 ms: 1.31x faster                                                        |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.07x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.04x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 138 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 138 ms: 1.04x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 269 ms: 1.29x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 110 ms: 3.81x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| float          | 31.4 ms                                                        | 32.8 ms: 1.04x slower                                                       |
| nbody          | 42.5 ms                                                        | 59.3 ms: 1.40x slower                                                       |
| Geometric mean | (ref)                                                          | 1.12x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 90.7 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.4 ms: 1.32x slower                                                       |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 880 ms: 1.14x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                        |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                       |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.83 ms: 1.14x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.21 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.72 ms: 1.30x slower                                                       |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.32x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 758 us: 2.69x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 456 us: 2.18x faster                                                        |
| pylint                           | 106 ms                                                         | 52.4 ms: 2.01x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 286 ms: 1.82x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                        |
| mdp                              | 1.06 sec                                                       | 589 ms: 1.80x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.21 ms: 1.49x faster                                                       |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                      |
| async_tree_io_tg                 | 405 ms                                                         | 290 ms: 1.40x faster                                                        |
| deepcopy                         | 145 us                                                         | 109 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 294 ms: 1.31x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                       |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| go                               | 72.6 ms                                                        | 59.8 ms: 1.21x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 786 ns: 1.21x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 56.7 us: 1.14x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 14.4 us: 1.14x faster                                                       |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 880 ms: 1.14x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 57.6 ms: 1.11x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.07x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                        |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 90.7 ms: 1.04x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.04x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 138 ms: 1.03x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.03x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                       |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                        |
| telco                            | 3.07 ms                                                        | 3.17 ms: 1.03x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 138 ms: 1.04x slower                                                        |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                        |
| float                            | 31.4 ms                                                        | 32.8 ms: 1.04x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 8.05 ms: 1.07x slower                                                       |
| sphinx                           | 409 ms                                                         | 439 ms: 1.07x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.09x slower                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.66 us: 1.09x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                       |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                       |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                        |
| thrift                           | 309 us                                                         | 345 us: 1.12x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.20 ms: 1.13x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.13x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.3 ms: 1.13x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 735 ms: 1.13x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 9.83 ms: 1.14x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 42.6 ms: 1.14x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.3 ms: 1.15x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                        |
| connected_components             | 208 ms                                                         | 240 ms: 1.16x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                        |
| chaos                            | 24.3 ms                                                        | 28.6 ms: 1.18x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.21 ms: 1.21x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 40.8 ms: 1.21x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.77 ms: 1.22x slower                                                       |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 50.0 ns: 1.23x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.23x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.42 us: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                        |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.28x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 269 ms: 1.29x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.72 ms: 1.30x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 63.4 ms: 1.32x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 574 us: 1.39x slower                                                        |
| nbody                            | 42.5 ms                                                        | 59.3 ms: 1.40x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.0 ms: 1.47x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 64.1 ms: 1.50x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 110 ms: 3.81x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_cpu_io_mixed, pycparser, async_tree_eager_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261018-3.16.0a1+dev-7dbc797-NOGIL/bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 78.42% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.24x