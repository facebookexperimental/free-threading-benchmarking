# Results vs. 3.13.0rc2

- fork: python
- ref: b70d45ab22e1d0f3b8a0
- machine: darwin-arm64
- commit hash: b70d45a
- commit date: 2025-03-21
- overall geometric mean: 1.091x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 132 ms: 1.18x slower                                                     |
| html5lib       | 23.1 ms                                                        | 25.3 ms: 1.10x slower                                                    |
| sphinx         | 409 ms                                                         | 439 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 192 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 233 ms: 1.12x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 12.5 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 56.6 ms: 1.31x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.3 ms: 3.05x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| float          | 31.4 ms                                                        | 36.3 ms: 1.16x slower                                                    |
| nbody          | 42.5 ms                                                        | 78.7 ms: 1.85x slower                                                    |
| Geometric mean | (ref)                                                          | 1.28x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| regex_compile  | 47.9 ms                                                        | 59.5 ms: 1.24x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.26 ms: 1.13x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 41.3 ms: 1.15x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 30.7 ms: 1.21x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 128 us: 1.29x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 170 us: 1.31x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.11x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.22 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.3 ms: 1.23x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 13.2 ms: 1.32x slower                                                    |
| mako            | 4.41 ms                                                        | 6.25 ms: 1.42x slower                                                    |
| django_template | 12.5 ms                                                        | 18.4 ms: 1.47x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.36x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 925 us: 2.21x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 502 us: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.38x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| deepcopy                         | 145 us                                                         | 129 us: 1.12x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 845 ns: 1.12x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.3 ms: 1.09x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 192 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| go                               | 72.6 ms                                                        | 74.8 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 17.3 us: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.25 sec: 1.06x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.8 ms: 1.06x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.2 ms: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.22 ms: 1.07x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.39 us: 1.07x slower                                                    |
| sphinx                           | 409 ms                                                         | 439 ms: 1.07x slower                                                     |
| pyflate                          | 222 ms                                                         | 239 ms: 1.08x slower                                                     |
| tomli_loads                      | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                   |
| pycparser                        | 470 ms                                                         | 508 ms: 1.08x slower                                                     |
| scimark_sor                      | 64.0 ms                                                        | 69.7 ms: 1.09x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 25.3 ms: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 233 ms: 1.12x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.19 sec: 1.12x slower                                                   |
| thrift                           | 309 us                                                         | 348 us: 1.13x slower                                                     |
| connected_components             | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.26 ms: 1.13x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 41.3 ms: 1.15x slower                                                    |
| float                            | 31.4 ms                                                        | 36.3 ms: 1.16x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.3 ms: 1.16x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.5 ms: 1.16x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.90 ms: 1.18x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.62 ms: 1.18x slower                                                    |
| 2to3                             | 112 ms                                                         | 132 ms: 1.18x slower                                                     |
| pylint                           | 106 ms                                                         | 125 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 9.05 ms: 1.20x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 30.7 ms: 1.21x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.8 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.2 ms: 1.22x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 26.3 ms: 1.23x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 59.5 ms: 1.24x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 119 ms: 1.25x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 60.5 ms: 1.26x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 81.7 us: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| richards                         | 22.1 ms                                                        | 28.0 ms: 1.27x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 203 ms: 1.27x slower                                                     |
| fannkuch                         | 179 ms                                                         | 227 ms: 1.27x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 31.4 ms: 1.27x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.86 us: 1.28x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.14 us: 1.28x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 415 ms: 1.29x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 128 us: 1.29x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 844 ms: 1.30x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 170 us: 1.31x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 56.6 ms: 1.31x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 13.2 ms: 1.32x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 164 ms: 1.33x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 49.7 ms: 1.34x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.4 ms: 1.35x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 59.2 ms: 1.35x slower                                                    |
| chaos                            | 24.3 ms                                                        | 33.3 ms: 1.37x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 46.3 ms: 1.38x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.00 ms: 1.38x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 56.2 ns: 1.38x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.99 ms: 1.40x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.25 ms: 1.42x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.52 ms: 1.42x slower                                                    |
| generators                       | 15.7 ms                                                        | 22.3 ms: 1.42x slower                                                    |
| django_template                  | 12.5 ms                                                        | 18.4 ms: 1.47x slower                                                    |
| raytrace                         | 109 ms                                                         | 161 ms: 1.48x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 10.1 us: 1.49x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.41 ms: 1.50x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 625 us: 1.52x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 67.3 ms: 1.57x slower                                                    |
| nbody                            | 42.5 ms                                                        | 78.7 ms: 1.85x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.3 ms: 3.05x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x slower                                                             |

Benchmark hidden because not significant (3): async_tree_eager_memoization, dulwich_log, docutils
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250321-3.14.0a6+-b70d45a-NOGIL/bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.17x