# Results vs. 3.12.6

- fork: python
- ref: e5f68fd29b3bd867207f
- machine: darwin-arm64
- commit hash: e5f68fd
- commit date: 2025-04-10
- overall geometric mean: 1.117x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.4 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.9 ms: 1.16x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.1 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.5 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 885 ms: 1.08x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.2 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.11 ms: 1.20x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.5 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.70 ms: 2.39x faster                                                    |
| mdp                              | 1.09 sec                                                 | 520 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.10 us: 1.33x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.46 us: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.1 ns: 1.27x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.26x faster                                                    |
| go                               | 70.0 ms                                                  | 56.4 ms: 1.24x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.4 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.2 ms: 1.19x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.6 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| k_core                           | 1.12 sec                                                 | 940 ms: 1.19x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 46.9 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.5 ms: 1.16x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.5 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 63.5 us: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.8 ms: 1.12x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.5 ms: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 885 ms: 1.08x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 47.5 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.4 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.5 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 932 ns: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.2 us: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 24.9 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.5 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.02x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 655 ms: 1.02x faster                                                     |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 99.1 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 40.4 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.33 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 439 us: 1.05x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 877 us: 1.06x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.95 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 233 us: 1.19x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.11 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.5 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.4 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (3): mako, gc_traversal, pidigits
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250410-3.14.0a7+-e5f68fd/bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.117x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x