# Results vs. 3.13.0rc2

- fork: python
- ref: ef06508f8ef1d2943b2f
- machine: darwin-arm64
- commit hash: ef06508
- commit date: 2025-03-23
- overall geometric mean: 1.096x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 134 ms: 1.20x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                   |
| html5lib       | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                    |
| sphinx         | 409 ms                                                         | 446 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 226 ms: 2.31x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 236 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| async_generators                 | 193 ms                                                         | 194 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 233 ms: 1.03x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 57.1 ms: 1.32x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.8 ms: 3.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| float          | 31.4 ms                                                        | 36.4 ms: 1.16x slower                                                    |
| nbody          | 42.5 ms                                                        | 79.0 ms: 1.86x slower                                                    |
| Geometric mean | (ref)                                                          | 1.29x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 59.5 ms: 1.24x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.8 ms: 1.08x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 41.1 ms: 1.15x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 30.6 ms: 1.21x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 128 us: 1.29x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 170 us: 1.31x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.11x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.37 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.37 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.6 ms: 1.24x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 13.2 ms: 1.33x slower                                                    |
| mako            | 4.41 ms                                                        | 6.22 ms: 1.41x slower                                                    |
| django_template | 12.5 ms                                                        | 18.4 ms: 1.47x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.36x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 226 ms: 2.31x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 236 ms: 2.23x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 934 us: 2.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 510 us: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.38x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| deepcopy                         | 145 us                                                         | 129 us: 1.13x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 844 ns: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.8 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| async_generators                 | 193 ms                                                         | 194 ms: 1.01x slower                                                     |
| dulwich_log                      | 19.8 ms                                                        | 20.0 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 233 ms: 1.03x slower                                                     |
| go                               | 72.6 ms                                                        | 75.2 ms: 1.04x slower                                                    |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.04x slower                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 17.3 us: 1.05x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.26 sec: 1.06x slower                                                   |
| pyflate                          | 222 ms                                                         | 236 ms: 1.06x slower                                                     |
| pathlib                          | 11.1 ms                                                        | 11.9 ms: 1.07x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.39 us: 1.08x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.0 ms: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.37 ms: 1.09x slower                                                    |
| sphinx                           | 409 ms                                                         | 446 ms: 1.09x slower                                                     |
| pycparser                        | 470 ms                                                         | 513 ms: 1.09x slower                                                     |
| scimark_sor                      | 64.0 ms                                                        | 70.4 ms: 1.10x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.12x slower                                                    |
| thrift                           | 309 us                                                         | 348 us: 1.13x slower                                                     |
| connected_components             | 208 ms                                                         | 236 ms: 1.13x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.20 sec: 1.13x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 41.1 ms: 1.15x slower                                                    |
| float                            | 31.4 ms                                                        | 36.4 ms: 1.16x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 52.1 ms: 1.17x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.63 ms: 1.18x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 6.00 ms: 1.20x slower                                                    |
| 2to3                             | 112 ms                                                         | 134 ms: 1.20x slower                                                     |
| pylint                           | 106 ms                                                         | 127 ms: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 30.6 ms: 1.21x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 9.21 ms: 1.22x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 64.6 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.37 ms: 1.24x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 59.5 ms: 1.24x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 26.6 ms: 1.24x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 80.9 us: 1.25x slower                                                    |
| fannkuch                         | 179 ms                                                         | 225 ms: 1.26x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 120 ms: 1.26x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 60.8 ms: 1.27x slower                                                    |
| richards                         | 22.1 ms                                                        | 28.2 ms: 1.28x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 204 ms: 1.28x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 31.7 ms: 1.28x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 128 us: 1.29x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 415 ms: 1.29x slower                                                     |
| many_optionals                   | 200 us                                                         | 259 us: 1.29x slower                                                     |
| coverage                         | 31.2 ms                                                        | 40.5 ms: 1.30x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 847 ms: 1.30x slower                                                     |
| logging_format                   | 2.45 us                                                        | 3.19 us: 1.30x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 170 us: 1.31x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.93 us: 1.31x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 162 ms: 1.31x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 57.1 ms: 1.32x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 49.4 ms: 1.33x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 13.2 ms: 1.33x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 59.8 ms: 1.37x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 41.0 ms: 1.37x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.00 ms: 1.38x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 56.1 ns: 1.38x slower                                                    |
| chaos                            | 24.3 ms                                                        | 33.6 ms: 1.38x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 46.8 ms: 1.39x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.22 ms: 1.41x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 4.02 ms: 1.41x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.52 ms: 1.42x slower                                                    |
| generators                       | 15.7 ms                                                        | 22.5 ms: 1.43x slower                                                    |
| django_template                  | 12.5 ms                                                        | 18.4 ms: 1.47x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 607 us: 1.47x slower                                                     |
| raytrace                         | 109 ms                                                         | 162 ms: 1.48x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 10.2 us: 1.50x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.53 ms: 1.52x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 68.6 ms: 1.60x slower                                                    |
| nbody                            | 42.5 ms                                                        | 79.0 ms: 1.86x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.8 ms: 3.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x slower                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250323-3.14.0a6+-ef06508-NOGIL/bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.18x