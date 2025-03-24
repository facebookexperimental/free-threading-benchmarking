# Results vs. 3.12.6

- fork: python
- ref: ef06508f8ef1d2943b2f
- machine: darwin-arm64
- commit hash: ef06508
- commit date: 2025-03-23
- overall geometric mean: 1.025x slower
- HPT reliability: 99.87%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 134 ms: 1.18x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                    |
| sphinx         | 434 ms                                                   | 446 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 236 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 226 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                     |
| async_generators                 | 206 ms                                                   | 194 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 233 ms: 1.01x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.11x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 57.1 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.8 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 36.4 ms: 1.04x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                     |
| nbody          | 54.2 ms                                                  | 79.0 ms: 1.46x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| regex_compile  | 54.6 ms                                                  | 59.5 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 41.1 ms: 1.06x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.08 sec: 1.13x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 30.6 ms: 1.15x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.17 ms: 1.21x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 170 us: 1.22x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.37 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.37 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.6 ms: 1.22x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| mako            | 4.77 ms                                                  | 6.22 ms: 1.30x slower                                                    |
| django_template | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.53 ms: 2.18x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 934 us: 2.15x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 236 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 226 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 510 us: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| deepcopy                         | 161 us                                                   | 129 us: 1.25x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 57.8 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 844 ns: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 20.0 ms: 1.06x faster                                                    |
| async_generators                 | 206 ms                                                   | 194 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 17.3 us: 1.06x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.39 us: 1.05x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.9 ms: 1.04x faster                                                    |
| float                            | 37.9 ms                                                  | 36.4 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 233 ms: 1.01x slower                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.26 sec: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                     |
| generators                       | 21.9 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| sphinx                           | 434 ms                                                   | 446 ms: 1.03x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.0 ms: 1.03x slower                                                    |
| pycparser                        | 497 ms                                                   | 513 ms: 1.03x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                   |
| comprehensions                   | 9.84 us                                                  | 10.2 us: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 41.1 ms: 1.06x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                    |
| go                               | 70.0 ms                                                  | 75.2 ms: 1.07x slower                                                    |
| thrift                           | 322 us                                                   | 348 us: 1.08x slower                                                     |
| regex_compile                    | 54.6 ms                                                  | 59.5 ms: 1.09x slower                                                    |
| pyflate                          | 216 ms                                                   | 236 ms: 1.09x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.20 sec: 1.10x slower                                                   |
| spectral_norm                    | 54.4 ms                                                  | 59.8 ms: 1.10x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 56.1 ns: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.11x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 52.1 ms: 1.11x slower                                                    |
| raytrace                         | 145 ms                                                   | 162 ms: 1.11x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 64.6 ms: 1.12x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.08 sec: 1.13x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 49.4 ms: 1.14x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.19 us: 1.14x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.93 us: 1.14x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 80.9 us: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.15x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 30.6 ms: 1.15x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 9.21 ms: 1.15x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 70.4 ms: 1.15x slower                                                    |
| sympy_str                        | 104 ms                                                   | 120 ms: 1.16x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 6.00 ms: 1.16x slower                                                    |
| chaos                            | 28.9 ms                                                  | 33.6 ms: 1.16x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.00 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.37 ms: 1.17x slower                                                    |
| connected_components             | 201 ms                                                   | 236 ms: 1.17x slower                                                     |
| 2to3                             | 114 ms                                                   | 134 ms: 1.18x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 46.8 ms: 1.20x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.17 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.52 ms: 1.22x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 26.6 ms: 1.22x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 170 us: 1.22x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 204 ms: 1.22x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.25x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 31.7 ms: 1.25x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 57.1 ms: 1.25x slower                                                    |
| richards                         | 22.4 ms                                                  | 28.2 ms: 1.26x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 415 ms: 1.27x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 41.0 ms: 1.27x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 847 ms: 1.27x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 60.8 ms: 1.27x slower                                                    |
| fannkuch                         | 176 ms                                                   | 225 ms: 1.28x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.37 ms: 1.29x slower                                                    |
| mako                             | 4.77 ms                                                  | 6.22 ms: 1.30x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 4.02 ms: 1.32x slower                                                    |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 68.6 ms: 1.34x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.63 ms: 1.39x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 607 us: 1.45x slower                                                     |
| nbody                            | 54.2 ms                                                  | 79.0 ms: 1.46x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.5 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.8 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.03x slower                                                             |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250323-3.14.0a6+-ef06508-NOGIL/bm-20250323-macm4pro-arm64-python-ef06508f8ef1d2943b2f-3.14.0a6+-ef06508.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.025x slower

# HPT report

- Reliability score: 99.87% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.22x