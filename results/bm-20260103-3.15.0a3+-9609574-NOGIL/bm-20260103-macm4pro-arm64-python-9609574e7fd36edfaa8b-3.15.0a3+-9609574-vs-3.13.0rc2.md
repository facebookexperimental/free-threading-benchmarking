# Results vs. 3.13.0rc2

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.007x faster
- HPT reliability: 74.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| nbody          | 42.5 ms                                                        | 58.8 ms: 1.38x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.5 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.89 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.17 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 805 us: 2.53x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 506 us: 1.96x faster                                                     |
| mdp                              | 1.06 sec                                                       | 608 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.20 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 999 ms: 1.46x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.6 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                     |
| sphinx                           | 409 ms                                                         | 430 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 685 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.5 ms: 1.07x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.1 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.7 ns: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.17 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| thrift                           | 309 us                                                         | 337 us: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.7 us: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.13x slower                                                     |
| pylint                           | 106 ms                                                         | 120 ms: 1.13x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.89 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.5 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.16x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.09 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| connected_components             | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.17 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.28 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.0 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.9 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 57.4 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 270 us: 1.35x slower                                                     |
| nbody                            | 42.5 ms                                                        | 58.8 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (2): scimark_fft, pycparser
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260103-3.15.0a3+-9609574-NOGIL/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 74.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x