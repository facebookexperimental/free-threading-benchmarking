# Results vs. 3.12.6

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: darwin-arm64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.089x faster
- HPT reliability: 94.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 209 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 214 ms: 2.15x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 88.2 ms: 1.95x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.68x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 231 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.05x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 51.4 ms: 1.13x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.5 ms: 1.28x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.5 ms: 1.41x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| tomli_loads          | 957 ms                                                   | 978 ms: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.40 ms: 1.17x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.49 ms: 1.31x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.67 ms: 1.19x slower                                                    |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 745 us: 2.70x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 209 ms: 2.38x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.92 ms: 2.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 214 ms: 2.15x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 88.2 ms: 1.95x faster                                                    |
| mdp                              | 1.09 sec                                                 | 569 ms: 1.92x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 448 us: 1.85x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.68x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 231 ms: 1.46x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.5 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| deepcopy                         | 161 us                                                   | 124 us: 1.30x faster                                                     |
| float                            | 37.9 ms                                                  | 29.5 ms: 1.28x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.8 us: 1.24x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 814 ns: 1.19x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 978 ms: 1.14x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.65 us: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.29 us: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| go                               | 70.0 ms                                                  | 63.6 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 56.0 ms: 1.09x faster                                                    |
| raytrace                         | 145 ms                                                   | 134 ms: 1.08x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 47.6 ns: 1.07x faster                                                    |
| pyflate                          | 216 ms                                                   | 202 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.4 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.59 us: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.3 us: 1.02x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.86 us: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 978 ms: 1.02x slower                                                     |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 147 ms: 1.04x slower                                                     |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.05x slower                                                     |
| shortest_path                    | 219 ms                                                   | 230 ms: 1.05x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 40.9 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.7 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.3 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 55.2 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.24 ms: 1.08x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.74 ms: 1.11x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.2 ms: 1.11x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.9 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 365 ms: 1.11x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 745 ms: 1.12x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 51.4 ms: 1.13x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| fannkuch                         | 176 ms                                                   | 201 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.2 ms: 1.16x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.98 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.40 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.67 ms: 1.19x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 243 us: 1.24x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.27 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.49 ms: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 588 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.8 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 94.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x