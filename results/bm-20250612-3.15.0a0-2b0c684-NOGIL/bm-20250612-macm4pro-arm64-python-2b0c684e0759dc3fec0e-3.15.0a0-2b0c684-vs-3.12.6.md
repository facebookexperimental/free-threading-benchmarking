# Results vs. 3.12.6

- fork: python
- ref: 2b0c684e0759dc3fec0e
- machine: darwin-arm64
- commit hash: 2b0c684
- commit date: 2025-06-12
- overall geometric mean: 1.091x faster
- HPT reliability: 97.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 422 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.2 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 983 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.60 ms: 1.08x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 801 us: 2.51x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.79 ms: 2.12x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 559 ms: 1.95x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 499 us: 1.66x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.32x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.80 us: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 829 ns: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| go                               | 70.0 ms                                                  | 61.0 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 130 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.0 ms: 1.06x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 475 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 422 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.02 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.4 us: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 983 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 333 us: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.4 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.8 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.60 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.82 us: 1.10x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.6 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.0 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.14 us: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.1 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 379 ms: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 773 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.25 ms: 1.24x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 66.5 ms: 1.30x slower                                                   |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 593 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.4 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.2 ms: 2.43x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 218 ns: 4.29x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): sympy_integrate, nbody
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 97.71% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x