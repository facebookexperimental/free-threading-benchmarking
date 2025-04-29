# Results vs. 3.13.0rc2

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: darwin-arm64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.020x faster
- HPT reliability: 65.44%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                    |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.5 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.3 ms: 1.05x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.5 ms: 1.05x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 966 ms: 1.03x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.12 ms: 1.10x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.5 us: 1.15x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.29 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.75 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 746 us: 2.74x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 441 us: 2.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.07x faster                                                     |
| mdp                              | 1.06 sec                                                       | 567 ms: 1.87x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.6 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.5 ms: 1.17x faster                                                    |
| deepcopy                         | 145 us                                                         | 124 us: 1.17x faster                                                     |
| go                               | 72.6 ms                                                        | 62.3 ms: 1.16x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.1 us: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 815 ns: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.5 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 966 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 231 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.3 ms: 1.05x slower                                                    |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                     |
| json                             | 1.94 ms                                                        | 2.05 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.97 ms: 1.06x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.26 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.29 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                     |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.5 ns: 1.10x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.12 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 727 ms: 1.12x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.8 ms: 1.12x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.9 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.75 ms: 1.13x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.2 us: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| json_loads                       | 10.8 us                                                        | 12.5 us: 1.15x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.77 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.59 us: 1.16x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.84 us: 1.16x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.1 ms: 1.17x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.5 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.11 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.58 us: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.28x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.5 ms: 1.31x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.8 ms: 1.31x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.86 ms: 1.41x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 594 us: 1.44x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 65.44% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.17x