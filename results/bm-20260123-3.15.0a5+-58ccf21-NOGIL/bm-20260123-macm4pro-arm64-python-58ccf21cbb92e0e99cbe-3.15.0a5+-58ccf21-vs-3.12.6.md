# Results vs. 3.12.6

- fork: python
- ref: 58ccf21cbb92e0e99cbe
- machine: darwin-arm64
- commit hash: 58ccf21
- commit date: 2026-01-23
- overall geometric mean: 1.108x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 992 ms: 1.03x faster                                                     |
| sphinx         | 434 ms                                                   | 415 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.0 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.34x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                                    |
| tomli_loads          | 957 ms                                                   | 874 ms: 1.09x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.66 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.02 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.0 ms: 1.06x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.42 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.02 ms: 5.16x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 785 us: 2.56x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 598 ms: 1.82x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 513 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.16 us: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                     |
| go                               | 70.0 ms                                                  | 59.4 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.15x faster                                                   |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.13x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 45.1 ns: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.11x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 874 ms: 1.09x faster                                                     |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.1 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 459 ms: 1.08x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.65 us: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| sphinx                           | 434 ms                                                   | 415 ms: 1.05x faster                                                     |
| chaos                            | 28.9 ms                                                  | 27.7 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.0 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 992 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.04 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.01x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.1 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 677 ms: 1.02x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.10 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.0 ms: 1.06x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.2 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.4 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.42 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.66 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.02 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 562 us: 1.34x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.0 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (4): html5lib, dask, scimark_monte_carlo, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.36x