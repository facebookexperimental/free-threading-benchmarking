# Results vs. 3.12.6

- fork: python
- ref: 06292614ff7cef0ba28d
- machine: darwin-arm64
- commit hash: 0629261
- commit date: 2026-02-20
- overall geometric mean: 1.134x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 104 ms: 1.71x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.6 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 47.8 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| tomli_loads          | 957 ms                                                   | 863 ms: 1.11x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 35.7 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.7 ms: 1.05x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 103 us: 1.00x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.06x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| mdp                              | 1.09 sec                                                 | 551 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 234 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 104 ms: 1.71x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                     |
| deepcopy                         | 161 us                                                   | 101 us: 1.60x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.50 us: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| go                               | 70.0 ms                                                  | 55.8 ms: 1.25x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                    |
| k_core                           | 1.12 sec                                                 | 907 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.6 ns: 1.22x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 52.2 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.3 ms: 1.14x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.8 ms: 1.14x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.29 us: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.8 ms: 1.12x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.52 us: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 863 ms: 1.11x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.10x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.6 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.7 ms: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.6 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 47.8 ms: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.7 ms: 1.06x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.1 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.5 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.7 ms: 1.05x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.66 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 317 us: 1.01x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 657 ms: 1.01x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 956 ns: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 103 us: 1.00x slower                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.02x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 39.5 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                     |
| connected_components             | 201 ms                                                   | 211 ms: 1.05x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.09x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 911 us: 1.10x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 255 us: 1.31x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.6 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (5): sympy_sum, sympy_str, pprint_safe_repr, mako, genshi_xml
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260220-3.15.0a6+-0629261/bm-20260220-macm4pro-arm64-python-06292614ff7cef0ba28d-3.15.0a6+-0629261.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.134x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.23x