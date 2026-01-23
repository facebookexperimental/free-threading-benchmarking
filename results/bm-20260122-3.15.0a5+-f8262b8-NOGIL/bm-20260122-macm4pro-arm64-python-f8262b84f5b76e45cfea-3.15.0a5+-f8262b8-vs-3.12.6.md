# Results vs. 3.12.6

- fork: python
- ref: f8262b84f5b76e45cfea
- machine: darwin-arm64
- commit hash: f8262b8
- commit date: 2026-01-22
- overall geometric mean: 1.080x faster
- HPT reliability: 96.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.09x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.78x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 154 ms: 1.45x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.1 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| tomli_loads          | 957 ms                                                   | 906 ms: 1.06x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.1 ms: 1.11x slower                                                    |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.17 ms: 4.98x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 818 us: 2.45x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                     |
| mdp                              | 1.09 sec                                                 | 611 ms: 1.79x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.78x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 520 us: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 154 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.45x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.1 ns: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.46 us: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| go                               | 70.0 ms                                                  | 60.9 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 53.9 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.7 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 906 ms: 1.06x faster                                                     |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.2 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.9 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.1 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.08 ms: 1.00x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 71.6 us: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.8 ms: 1.02x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.23 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 338 ms: 1.03x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 693 ms: 1.04x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 342 us: 1.06x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.4 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.07x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| 2to3                             | 114 ms                                                   | 125 ms: 1.09x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 24.1 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 57.9 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.16x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 56.8 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.4 ms: 1.19x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.0 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 275 us: 1.41x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.0 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.1 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (3): dask, asyncio_websockets, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260122-3.15.0a5+-f8262b8-NOGIL/bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 96.44% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x