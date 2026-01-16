# Results vs. 3.13.0rc2

- fork: python
- ref: c461aa99e2fabbaf5859
- machine: darwin-arm64
- commit hash: c461aa9
- commit date: 2026-01-15
- overall geometric mean: 1.003x slower
- HPT reliability: 86.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                    |
| sphinx         | 409 ms                                                         | 433 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.3 ms: 3.29x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 170 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 58.5 ms: 1.38x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.7 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 4.03 ms: 1.15x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.6 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 922 ms: 1.08x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.31 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                    |
| mako            | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 823 us: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.07x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 524 us: 1.90x faster                                                     |
| mdp                              | 1.06 sec                                                       | 614 ms: 1.72x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.20 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                   |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                     |
| go                               | 72.6 ms                                                        | 60.5 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.03 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.6 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 843 ns: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 922 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 477 ms: 1.02x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 170 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| sphinx                           | 409 ms                                                         | 433 ms: 1.06x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 693 ms: 1.07x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.7 ms: 1.08x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.09x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.24 ms: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 71.8 us: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| shortest_path                    | 225 ms                                                         | 254 ms: 1.13x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.22 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.15x slower                                                     |
| pylint                           | 106 ms                                                         | 122 ms: 1.15x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 43.1 ms: 1.16x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.7 ms: 1.18x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.9 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.9 ms: 1.19x slower                                                    |
| connected_components             | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.20x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.14 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.31 ms: 1.23x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.39 us: 1.23x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.7 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.4 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 563 us: 1.37x slower                                                     |
| nbody                            | 42.5 ms                                                        | 58.5 ms: 1.38x slower                                                    |
| many_optionals                   | 200 us                                                         | 276 us: 1.38x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 62.0 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.3 ms: 3.29x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260115-3.15.0a5+-c461aa9-NOGIL/bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 86.16% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x