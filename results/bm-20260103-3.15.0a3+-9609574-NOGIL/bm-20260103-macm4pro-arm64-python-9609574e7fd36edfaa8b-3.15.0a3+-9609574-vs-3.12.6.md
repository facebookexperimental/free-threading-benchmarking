# Results vs. 3.12.6

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.087x faster
- HPT reliability: 97.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 58.8 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.01 sec: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.89 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.20 ms: 4.94x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 805 us: 2.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| mdp                              | 1.09 sec                                                 | 608 ms: 1.80x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 506 us: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.22x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.28 us: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.7 ns: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.7 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 999 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.6 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.11x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.46 us: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| sphinx                           | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.3 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.09 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.7 us: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.17 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 685 ms: 1.03x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.7 ms: 1.05x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.01 sec: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                    |
| nbody                            | 54.2 ms                                                  | 58.8 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.4 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| shortest_path                    | 219 ms                                                   | 255 ms: 1.16x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.7 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 248 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.89 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 270 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.0 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): scimark_monte_carlo, docutils
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260103-3.15.0a3+-9609574-NOGIL/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 97.27% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x