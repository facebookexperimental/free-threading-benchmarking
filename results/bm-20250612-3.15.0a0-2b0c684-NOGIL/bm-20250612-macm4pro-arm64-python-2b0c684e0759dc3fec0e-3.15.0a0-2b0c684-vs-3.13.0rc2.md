# Results vs. 3.13.0rc2

- fork: python
- ref: 2b0c684e0759dc3fec0e
- machine: darwin-arm64
- commit hash: 2b0c684
- commit date: 2025-06-12
- overall geometric mean: 1.011x faster
- HPT reliability: 81.58%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.4 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.2 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| nbody          | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 983 ms: 1.02x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.60 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.3 ms: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| mako            | 4.41 ms                                                        | 5.72 ms: 1.30x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 801 us: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 499 us: 1.99x faster                                                    |
| mdp                              | 1.06 sec                                                       | 559 ms: 1.89x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.4 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.27x faster                                                    |
| deepcopy                         | 145 us                                                         | 120 us: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.0 ms: 1.19x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 829 ns: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                  |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 983 ms: 1.02x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.60 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.00x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.25 ms: 1.06x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.02 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.00 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.3 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.0 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.6 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.4 us: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.12x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 28.0 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.80 us: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.6 ms: 1.15x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.15x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 379 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 773 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                   |
| raytrace                         | 109 ms                                                         | 130 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 41.8 ms: 1.24x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.82 us: 1.26x slower                                                   |
| nbody                            | 42.5 ms                                                        | 54.3 ms: 1.28x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.14 us: 1.28x slower                                                   |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.4 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.72 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 593 us: 1.44x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 66.5 ms: 1.56x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.79 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.2 ms: 2.70x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 218 ns: 5.38x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 81.58% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x