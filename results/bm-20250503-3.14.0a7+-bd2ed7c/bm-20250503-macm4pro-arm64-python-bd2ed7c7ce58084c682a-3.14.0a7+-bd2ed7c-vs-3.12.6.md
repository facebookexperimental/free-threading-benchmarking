# Results vs. 3.12.6

- fork: python
- ref: bd2ed7c7ce58084c682a
- machine: darwin-arm64
- commit hash: bd2ed7c
- commit date: 2025-05-03
- overall geometric mean: 1.114x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 25.7 ms: 1.12x slower                                                    |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 246 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.81x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.6 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                    |
| nbody          | 54.2 ms                                                  | 49.1 ms: 1.10x faster                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.89 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.0 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.7 us: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 949 ms: 1.01x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.11 ms: 1.20x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.05 ms: 1.06x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.18 ms: 2.26x faster                                                    |
| mdp                              | 1.09 sec                                                 | 519 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 246 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.81x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.45x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.59 us: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.30x faster                                                    |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                     |
| go                               | 70.0 ms                                                  | 56.4 ms: 1.24x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 51.5 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 952 ms: 1.17x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 47.0 ms: 1.16x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.9 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| nbody                            | 54.2 ms                                                  | 49.1 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.0 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.5 ms: 1.09x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.0 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.37 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.4 us: 1.08x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                     |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.2 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.7 us: 1.05x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.97 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| 2to3                             | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.04x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.6 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.4 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 943 ns: 1.03x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 650 ms: 1.02x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 1.99 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 949 ms: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 40.0 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.89 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.40 ms: 1.04x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 876 us: 1.06x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.05 ms: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 25.7 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.11 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 238 us: 1.22x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.6 ms: 2.69x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (2): json, pidigits
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250503-3.14.0a7+-bd2ed7c/bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x