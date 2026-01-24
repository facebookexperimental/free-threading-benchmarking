# Results vs. 3.12.6

- fork: python
- ref: 58ccf21cbb92e0e99cbe
- machine: darwin-arm64
- commit hash: 58ccf21
- commit date: 2026-01-23
- overall geometric mean: 1.176x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 385 ms: 1.13x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 220 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.1 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.3 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.20x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.46 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| tomli_loads          | 957 ms                                                   | 816 ms: 1.17x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.3 ms: 1.10x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.2 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.51 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| mako            | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.03 ms: 5.16x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 220 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.04x faster                                                     |
| mdp                              | 1.09 sec                                                 | 538 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.1 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.70x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.9 us: 1.65x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                    |
| float                            | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.07 us: 1.39x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 52.3 ms: 1.34x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.6 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 894 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 48.8 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.25x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.3 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 117 ms: 1.21x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.0 ms: 1.19x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.19x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.2 ms: 1.18x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 816 ms: 1.17x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.8 ms: 1.15x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.9 us: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.4 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.8 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                    |
| sphinx                           | 434 ms                                                   | 385 ms: 1.13x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.4 ms: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.51 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.3 ms: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 619 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                     |
| thrift                           | 322 us                                                   | 302 us: 1.06x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.5 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.0 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 99.2 us: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.46 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 955 ns: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.84 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 905 us: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.5 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 249 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (1): sympy_expand
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.176x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.23x