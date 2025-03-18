# Results vs. 3.12.6

- fork: python
- ref: v3.14.0a6
- machine: darwin-arm64
- commit hash: 77b2c93
- commit date: 2025-03-14
- overall geometric mean: 1.024x slower
- HPT reliability: 99.86%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 132 ms: 1.15x slower                                         |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                       |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                        |
| sphinx         | 434 ms                                                   | 440 ms: 1.02x slower                                         |
| Geometric mean | (ref)                                                    | 1.06x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                         |
| async_tree_eager_io              | 496 ms                                                   | 234 ms: 2.12x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                         |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                         |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                         |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                         |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                         |
| async_generators                 | 206 ms                                                   | 194 ms: 1.07x faster                                         |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                         |
| async_tree_eager                 | 45.6 ms                                                  | 56.9 ms: 1.25x slower                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                 |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.9 ms: 1.06x faster                                        |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                         |
| nbody          | 54.2 ms                                                  | 77.9 ms: 1.44x slower                                        |
| Geometric mean | (ref)                                                    | 1.11x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                        |
| regex_dna      | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                        |
| regex_v8       | 9.59 ms                                                  | 10.4 ms: 1.09x slower                                        |
| regex_compile  | 54.6 ms                                                  | 59.5 ms: 1.09x slower                                        |
| Geometric mean | (ref)                                                    | 1.02x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                        |
| xml_etree_parse      | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                        |
| xml_etree_generate   | 38.9 ms                                                  | 41.2 ms: 1.06x slower                                        |
| json_loads           | 10.9 us                                                  | 12.0 us: 1.11x slower                                        |
| tomli_loads          | 957 ms                                                   | 1.07 sec: 1.12x slower                                       |
| xml_etree_process    | 26.7 ms                                                  | 30.5 ms: 1.14x slower                                        |
| pickle_pure_python   | 139 us                                                   | 171 us: 1.23x slower                                         |
| json_dumps           | 4.26 ms                                                  | 5.30 ms: 1.24x slower                                        |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.25x slower                                         |
| Geometric mean       | (ref)                                                    | 1.08x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                        |
| python_startup_no_site | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                        |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.1 ms: 1.20x slower                                        |
| genshi_text     | 10.5 ms                                                  | 13.0 ms: 1.24x slower                                        |
| mako            | 4.77 ms                                                  | 6.19 ms: 1.30x slower                                        |
| django_template | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                        |
| Geometric mean  | (ref)                                                    | 1.27x slower                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 908 us: 2.21x faster                                         |
| subparsers                       | 20.8 ms                                                  | 9.41 ms: 2.21x faster                                        |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                         |
| async_tree_eager_io              | 496 ms                                                   | 234 ms: 2.12x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                         |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                         |
| create_gc_cycles                 | 830 us                                                   | 480 us: 1.73x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                         |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                         |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                        |
| deepcopy                         | 161 us                                                   | 130 us: 1.25x faster                                         |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                        |
| sqlite_synth                     | 967 ns                                                   | 841 ns: 1.15x faster                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                        |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                        |
| regex_dna                        | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.6 ms: 1.08x faster                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                         |
| async_generators                 | 206 ms                                                   | 194 ms: 1.07x faster                                         |
| deepcopy_memo                    | 18.3 us                                                  | 17.2 us: 1.06x faster                                        |
| pathlib                          | 12.4 ms                                                  | 11.6 ms: 1.06x faster                                        |
| float                            | 37.9 ms                                                  | 35.9 ms: 1.06x faster                                        |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.05x faster                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.40 us: 1.04x faster                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 38.7 ms: 1.03x faster                                        |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                         |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                         |
| generators                       | 21.9 ms                                                  | 22.1 ms: 1.01x slower                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.26 sec: 1.01x slower                                       |
| sphinx                           | 434 ms                                                   | 440 ms: 1.02x slower                                         |
| pycparser                        | 497 ms                                                   | 510 ms: 1.03x slower                                         |
| comprehensions                   | 9.84 us                                                  | 10.2 us: 1.03x slower                                        |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                       |
| json                             | 1.93 ms                                                  | 2.02 ms: 1.05x slower                                        |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                        |
| xml_etree_generate               | 38.9 ms                                                  | 41.2 ms: 1.06x slower                                        |
| go                               | 70.0 ms                                                  | 74.6 ms: 1.07x slower                                        |
| regex_v8                         | 9.59 ms                                                  | 10.4 ms: 1.09x slower                                        |
| regex_compile                    | 54.6 ms                                                  | 59.5 ms: 1.09x slower                                        |
| pyflate                          | 216 ms                                                   | 236 ms: 1.09x slower                                         |
| spectral_norm                    | 54.4 ms                                                  | 59.5 ms: 1.09x slower                                        |
| mdp                              | 1.09 sec                                                 | 1.20 sec: 1.10x slower                                       |
| thrift                           | 322 us                                                   | 353 us: 1.10x slower                                         |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.4 ms: 1.10x slower                                        |
| raytrace                         | 145 ms                                                   | 159 ms: 1.10x slower                                         |
| logging_silent                   | 50.9 ns                                                  | 56.1 ns: 1.10x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                         |
| sympy_sum                        | 57.6 ms                                                  | 63.7 ms: 1.11x slower                                        |
| json_loads                       | 10.9 us                                                  | 12.0 us: 1.11x slower                                        |
| logging_format                   | 2.80 us                                                  | 3.13 us: 1.11x slower                                        |
| logging_simple                   | 2.57 us                                                  | 2.87 us: 1.12x slower                                        |
| sqlglot_optimize                 | 23.4 ms                                                  | 26.2 ms: 1.12x slower                                        |
| tomli_loads                      | 957 ms                                                   | 1.07 sec: 1.12x slower                                       |
| sqlglot_normalize                | 126 ms                                                   | 142 ms: 1.13x slower                                         |
| shortest_path                    | 219 ms                                                   | 247 ms: 1.13x slower                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                         |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.85 ms: 1.13x slower                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 80.7 us: 1.14x slower                                        |
| xml_etree_process                | 26.7 ms                                                  | 30.5 ms: 1.14x slower                                        |
| scimark_sor                      | 61.0 ms                                                  | 69.8 ms: 1.14x slower                                        |
| python_startup                   | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                        |
| scimark_fft                      | 142 ms                                                   | 163 ms: 1.15x slower                                         |
| nqueens                          | 43.5 ms                                                  | 50.1 ms: 1.15x slower                                        |
| 2to3                             | 114 ms                                                   | 132 ms: 1.15x slower                                         |
| sympy_str                        | 104 ms                                                   | 120 ms: 1.16x slower                                         |
| deltablue                        | 1.73 ms                                                  | 2.00 ms: 1.16x slower                                        |
| sympy_integrate                  | 8.02 ms                                                  | 9.33 ms: 1.16x slower                                        |
| chaos                            | 28.9 ms                                                  | 33.7 ms: 1.17x slower                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 45.4 ms: 1.17x slower                                        |
| connected_components             | 201 ms                                                   | 235 ms: 1.17x slower                                         |
| sqlglot_transpile                | 696 us                                                   | 825 us: 1.18x slower                                         |
| sqlglot_parse                    | 577 us                                                   | 688 us: 1.19x slower                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.48 ms: 1.19x slower                                        |
| genshi_xml                       | 21.8 ms                                                  | 26.1 ms: 1.20x slower                                        |
| richards                         | 22.4 ms                                                  | 27.3 ms: 1.22x slower                                        |
| sympy_expand                     | 167 ms                                                   | 203 ms: 1.22x slower                                         |
| pickle_pure_python               | 139 us                                                   | 171 us: 1.23x slower                                         |
| richards_super                   | 25.4 ms                                                  | 31.4 ms: 1.24x slower                                        |
| genshi_text                      | 10.5 ms                                                  | 13.0 ms: 1.24x slower                                        |
| json_dumps                       | 4.26 ms                                                  | 5.30 ms: 1.24x slower                                        |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.25x slower                                         |
| async_tree_eager                 | 45.6 ms                                                  | 56.9 ms: 1.25x slower                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.3 ms: 1.25x slower                                        |
| meteor_contest                   | 47.7 ms                                                  | 59.9 ms: 1.25x slower                                        |
| pprint_safe_repr                 | 328 ms                                                   | 412 ms: 1.26x slower                                         |
| pprint_pformat                   | 665 ms                                                   | 839 ms: 1.26x slower                                         |
| python_startup_no_site           | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                        |
| fannkuch                         | 176 ms                                                   | 225 ms: 1.28x slower                                         |
| mako                             | 4.77 ms                                                  | 6.19 ms: 1.30x slower                                        |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                         |
| scimark_lu                       | 51.3 ms                                                  | 67.1 ms: 1.31x slower                                        |
| hexiom                           | 3.04 ms                                                  | 3.98 ms: 1.31x slower                                        |
| django_template                  | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                        |
| telco                            | 2.61 ms                                                  | 3.57 ms: 1.37x slower                                        |
| coverage                         | 26.9 ms                                                  | 38.4 ms: 1.43x slower                                        |
| nbody                            | 54.2 ms                                                  | 77.9 ms: 1.44x slower                                        |
| bench_thread_pool                | 419 us                                                   | 613 us: 1.47x slower                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.03x slower                                                 |

Benchmark hidden because not significant (2): pylint, async_tree_eager_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 99.86% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.21x