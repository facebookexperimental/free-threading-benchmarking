# Results vs. 3.12.6

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: darwin-arm64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.088x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 25.8 ms: 1.12x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 49.6 ms: 1.10x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.58 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.03x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.4 ms: 1.16x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.0 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| tomli_loads          | 957 ms                                                   | 970 ms: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.68 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 4.86 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.80 ms: 2.12x faster                                                   |
| mdp                              | 1.09 sec                                                 | 535 ms: 2.04x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.82 us: 1.26x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| float                            | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 57.9 ms: 1.21x faster                                                   |
| raytrace                         | 145 ms                                                   | 120 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 52.2 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 962 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.4 ms: 1.16x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| spectral_norm                    | 54.4 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.9 ms: 1.12x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.6 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.0 ms: 1.07x faster                                                   |
| pyflate                          | 216 ms                                                   | 201 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.0 ms: 1.07x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.96 ms: 1.06x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 67.1 us: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.58 ms: 1.05x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.63 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.0 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 954 ns: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.9 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.2 ms: 1.01x faster                                                   |
| connected_components             | 201 ms                                                   | 200 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.00x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 331 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| pycparser                        | 497 ms                                                   | 503 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 970 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.86 ms: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.86 us: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.63 us: 1.02x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 51.5 ms: 1.08x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.68 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 25.8 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                   |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 249 us: 1.27x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.73x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): pprint_pformat
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x