# Results vs. 3.12.6

- fork: python
- ref: 0efd679a6ce3b57ec3c5
- machine: darwin-arm64
- commit hash: 0efd679
- commit date: 2026-04-28
- overall geometric mean: 1.174x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.06x faster                                                    |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.0 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                    |
| tomli_loads          | 957 ms                                                   | 823 ms: 1.16x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 96.7 us: 1.06x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.9 ms: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.85 ms: 1.03x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.57 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.53 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.9 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.99 ms: 5.20x faster                                                    |
| pylint                           | 128 ms                                                   | 50.7 ms: 2.53x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| mdp                              | 1.09 sec                                                 | 536 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.0 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.70x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.5 us: 1.66x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 143 ms: 1.56x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.00 us: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| go                               | 70.0 ms                                                  | 52.5 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 42.9 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.8 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 898 ms: 1.25x faster                                                     |
| nbody                            | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.6 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 823 ms: 1.16x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 46.2 ms: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.53 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.7 ms: 1.08x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 622 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 307 ms: 1.07x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.7 us: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.9 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 65.9 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 942 ns: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 317 us: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.5 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                    |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.01x slower                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.79 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.02x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 5.85 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.57 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.49 ms: 1.24x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.5 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260428-3.15.0a8+-0efd679/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.174x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x