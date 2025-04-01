# Results vs. 3.13.0rc2

- fork: python
- ref: 45a3ab5a81769eadd94d
- machine: darwin-arm64
- commit hash: 45a3ab5
- commit date: 2025-03-31
- overall geometric mean: 1.121x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 139 ms: 1.25x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                   |
| html5lib       | 23.1 ms                                                        | 26.0 ms: 1.12x slower                                                    |
| sphinx         | 409 ms                                                         | 450 ms: 1.10x slower                                                     |
| Geometric mean | (ref)                                                          | 1.12x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 234 ms: 2.23x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.21x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                     |
| async_generators                 | 193 ms                                                         | 203 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 13.0 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 60.7 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.4 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| float          | 31.4 ms                                                        | 38.1 ms: 1.21x slower                                                    |
| nbody          | 42.5 ms                                                        | 74.8 ms: 1.76x slower                                                    |
| Geometric mean | (ref)                                                          | 1.26x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 64.8 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.26 ms: 1.13x slower                                                    |
| tomli_loads          | 1000 ms                                                        | 1.15 sec: 1.15x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 42.8 ms: 1.20x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 32.4 ms: 1.28x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 181 us: 1.39x slower                                                     |
| unpickle_pure_python | 99.5 us                                                        | 141 us: 1.42x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.19 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.25 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 28.7 ms: 1.34x slower                                                    |
| mako            | 4.41 ms                                                        | 6.30 ms: 1.43x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 14.7 ms: 1.47x slower                                                    |
| django_template | 12.5 ms                                                        | 20.8 ms: 1.67x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.47x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 234 ms: 2.23x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 923 us: 2.21x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 500 us: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| mdp                              | 1.06 sec                                                       | 666 ms: 1.59x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.37x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 152 ms: 1.21x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 259 ms: 1.13x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 862 ns: 1.10x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| deepcopy                         | 145 us                                                         | 143 us: 1.01x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 20.2 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                     |
| docutils                         | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 39.7 ms: 1.05x slower                                                    |
| async_generators                 | 193 ms                                                         | 203 ms: 1.05x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.19 ms: 1.07x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 12.0 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.33 sec: 1.09x slower                                                   |
| sphinx                           | 409 ms                                                         | 450 ms: 1.10x slower                                                     |
| pyflate                          | 222 ms                                                         | 248 ms: 1.12x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 26.0 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| go                               | 72.6 ms                                                        | 81.8 ms: 1.13x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.26 ms: 1.13x slower                                                    |
| scimark_sor                      | 64.0 ms                                                        | 73.2 ms: 1.14x slower                                                    |
| pycparser                        | 470 ms                                                         | 539 ms: 1.15x slower                                                     |
| tomli_loads                      | 1000 ms                                                        | 1.15 sec: 1.15x slower                                                   |
| connected_components             | 208 ms                                                         | 240 ms: 1.16x slower                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 19.1 us: 1.16x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 52.4 ms: 1.18x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 42.8 ms: 1.20x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 13.0 ms: 1.21x slower                                                    |
| pylint                           | 106 ms                                                         | 128 ms: 1.21x slower                                                     |
| float                            | 31.4 ms                                                        | 38.1 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 6.07 ms: 1.21x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 9.16 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.25 ms: 1.22x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.74 ms: 1.22x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.59 us: 1.23x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 59.4 ms: 1.24x slower                                                    |
| 2to3                             | 112 ms                                                         | 139 ms: 1.25x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 32.4 ms: 1.28x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 66.8 ms: 1.28x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                    |
| many_optionals                   | 200 us                                                         | 261 us: 1.30x slower                                                     |
| fannkuch                         | 179 ms                                                         | 233 ms: 1.30x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 162 ms: 1.31x slower                                                     |
| richards                         | 22.1 ms                                                        | 29.3 ms: 1.33x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 127 ms: 1.33x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 28.7 ms: 1.34x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 33.3 ms: 1.35x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 215 ms: 1.35x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 64.8 ms: 1.35x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 87.6 us: 1.35x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 181 us: 1.39x slower                                                     |
| logging_format                   | 2.45 us                                                        | 3.41 us: 1.40x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 61.1 ms: 1.40x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 3.13 us: 1.40x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.50 ms: 1.40x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 60.7 ms: 1.41x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 42.3 ms: 1.41x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 141 us: 1.42x slower                                                     |
| mako                             | 4.41 ms                                                        | 6.30 ms: 1.43x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 58.1 ns: 1.43x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 53.6 ms: 1.44x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 601 us: 1.46x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 14.7 ms: 1.47x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 4.21 ms: 1.48x slower                                                    |
| generators                       | 15.7 ms                                                        | 23.5 ms: 1.50x slower                                                    |
| chaos                            | 24.3 ms                                                        | 36.5 ms: 1.50x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 484 ms: 1.50x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 982 ms: 1.51x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 65.1 ms: 1.52x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.22 ms: 1.53x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 52.1 ms: 1.55x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.81 ms: 1.57x slower                                                    |
| raytrace                         | 109 ms                                                         | 172 ms: 1.58x slower                                                     |
| django_template                  | 12.5 ms                                                        | 20.8 ms: 1.67x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 11.5 us: 1.69x slower                                                    |
| nbody                            | 42.5 ms                                                        | 74.8 ms: 1.76x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.4 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x slower                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250331-3.14.0a6+-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.121x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.17x