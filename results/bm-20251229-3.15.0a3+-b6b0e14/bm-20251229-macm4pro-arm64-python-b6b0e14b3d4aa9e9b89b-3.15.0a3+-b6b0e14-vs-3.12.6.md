# Results vs. 3.12.6

- fork: python
- ref: b6b0e14b3d4aa9e9b89b
- machine: darwin-arm64
- commit hash: b6b0e14
- commit date: 2025-12-29
- overall geometric mean: 1.154x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 396 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.3 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.4 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.9 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.8 us: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 932 ms: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.73 ms: 1.08x faster                                                    |
| mako            | 4.77 ms                                                  | 4.61 ms: 1.04x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.06 ms: 5.11x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| mdp                              | 1.09 sec                                                 | 548 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy                         | 161 us                                                   | 102 us: 1.58x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.04 us: 1.40x faster                                                    |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| go                               | 70.0 ms                                                  | 53.7 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.27x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.6 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 907 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.5 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.4 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.18x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                     |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.23 us: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.0 ms: 1.14x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.46 us: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.9 us: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.9 ms: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.3 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 396 ms: 1.09x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.73 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                     |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 97.8 us: 1.05x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 634 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 314 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.61 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.6 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 932 ms: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.2 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.16 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.09x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 939 us: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 255 us: 1.31x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (3): json, json_loads, sqlite_synth
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.154x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.21x