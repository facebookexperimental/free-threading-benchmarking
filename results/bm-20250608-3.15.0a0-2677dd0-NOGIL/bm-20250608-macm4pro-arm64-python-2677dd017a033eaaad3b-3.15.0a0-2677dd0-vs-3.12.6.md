# Results vs. 3.12.6

- fork: python
- ref: 2677dd017a033eaaad3b
- machine: darwin-arm64
- commit hash: 2677dd0
- commit date: 2025-06-08
- overall geometric mean: 1.106x faster
- HPT reliability: 99.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 983 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.8 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.2 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                   |
| nbody          | 54.2 ms                                                  | 53.5 ms: 1.01x faster                                                   |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.5 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.4 ms: 1.38x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 55.6 ms: 1.22x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 968 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.60 ms: 1.08x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.35 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.83 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                   |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.62x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.66 ms: 2.15x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.8 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 555 ms: 1.97x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 485 us: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.4 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                   |
| deepcopy                         | 161 us                                                   | 120 us: 1.35x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.82 us: 1.26x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 55.6 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 821 ns: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| go                               | 70.0 ms                                                  | 60.7 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| raytrace                         | 145 ms                                                   | 129 ms: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.9 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.7 ms: 1.07x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.1 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 983 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.83 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| nbody                            | 54.2 ms                                                  | 53.5 ms: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.01 ms: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 968 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.5 us: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 330 us: 1.03x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.1 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.2 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.60 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.80 us: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.9 ms: 1.10x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 52.4 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 184 ms: 1.10x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.10 us: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 375 ms: 1.14x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 765 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.35 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.83 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.22 ms: 1.24x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 64.7 ms: 1.26x slower                                                   |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 598 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 216 ns: 4.25x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): html5lib, json
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250608-3.15.0a0-2677dd0-NOGIL/bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.106x faster

# HPT report

- Reliability score: 99.64% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x