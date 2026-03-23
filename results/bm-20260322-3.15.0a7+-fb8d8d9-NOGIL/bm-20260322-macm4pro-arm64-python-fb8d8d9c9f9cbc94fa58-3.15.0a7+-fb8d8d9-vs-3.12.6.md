# Results vs. 3.12.6

- fork: python
- ref: fb8d8d9c9f9cbc94fa58
- machine: darwin-arm64
- commit hash: fb8d8d9
- commit date: 2026-03-22
- overall geometric mean: 1.107x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 237 ms: 1.88x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.0 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.7 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.7 ms: 1.16x faster                                                    |
| tomli_loads          | 957 ms                                                   | 832 ms: 1.15x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 106 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.79 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.11 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.03 ms: 5.16x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 800 us: 2.51x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 237 ms: 1.88x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                     |
| mdp                              | 1.09 sec                                                 | 604 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 504 us: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 104 us: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.47x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 788 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.23 us: 1.20x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.8 ns: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.5 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.7 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 832 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.11x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.1 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 457 ms: 1.09x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.6 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 663 ms: 1.00x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.0 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.12 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.9 us: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.8 ms: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 106 us: 1.03x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 53.1 ms: 1.04x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.4 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.79 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.11 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 263 us: 1.35x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 574 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.3 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.7 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.107x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.37x