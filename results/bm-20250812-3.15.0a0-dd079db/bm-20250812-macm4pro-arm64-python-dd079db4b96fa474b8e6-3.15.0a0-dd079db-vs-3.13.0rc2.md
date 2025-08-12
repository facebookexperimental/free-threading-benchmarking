# Results vs. 3.13.0rc2

- fork: python
- ref: dd079db4b96fa474b8e6
- machine: darwin-arm64
- commit hash: dd079db
- commit date: 2025-08-12
- overall geometric mean: 1.022x faster
- HPT reliability: 85.32%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.16x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.81 ms: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.6 ms: 2.99x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 907 ms: 1.10x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 64.6 ms: 1.04x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.16x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 253 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 537 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 956 ms: 1.53x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.33x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| go                               | 72.6 ms                                                        | 55.4 ms: 1.31x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.5 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 907 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.81 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 30.1 ms: 1.04x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 953 us: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.6 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.5 ms: 1.01x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 663 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 64.6 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 435 us: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.9 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.94 ms: 1.09x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.47 us: 1.10x slower                                                   |
| raytrace                         | 109 ms                                                         | 120 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| pycparser                        | 470 ms                                                         | 527 ms: 1.12x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.8 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 318 us: 1.58x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.1 ms: 2.74x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.6 ms: 2.99x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (8): logging_silent, thrift, regex_compile, sympy_integrate, genshi_xml, sphinx, sqlite_synth, docutils
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250812-3.15.0a0-dd079db/bm-20250812-macm4pro-arm64-python-dd079db4b96fa474b8e6-3.15.0a0-dd079db.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 85.32% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x