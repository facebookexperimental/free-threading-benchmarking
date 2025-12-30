# Results vs. 3.12.6

- fork: python
- ref: b6b0e14b3d4aa9e9b89b
- machine: darwin-arm64
- commit hash: b6b0e14
- commit date: 2025-12-29
- overall geometric mean: 1.082x faster
- HPT reliability: 94.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.99x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.94x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.38 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.06 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.01 sec: 1.06x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.14 ms: 5.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 822 us: 2.44x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.99x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 609 ms: 1.79x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 522 us: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.46x faster                                                     |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.31 us: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 831 ns: 1.16x faster                                                     |
| go                               | 70.0 ms                                                  | 60.3 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.4 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 999 ms: 1.12x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                     |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.06 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.38 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.76 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| sphinx                           | 434 ms                                                   | 430 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 71.5 us: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 334 ms: 1.02x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.17 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 684 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.14 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| json                             | 1.93 ms                                                  | 2.02 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 338 us: 1.05x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 1.01 sec: 1.06x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.6 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.7 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.4 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 57.1 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 247 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 547 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 273 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.94x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): fannkuch, nqueens
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 94.12% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x