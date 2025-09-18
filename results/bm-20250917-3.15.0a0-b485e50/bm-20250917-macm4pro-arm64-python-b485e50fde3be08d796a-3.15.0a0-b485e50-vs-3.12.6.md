# Results vs. 3.12.6

- fork: python
- ref: b485e50fde3be08d796a
- machine: darwin-arm64
- commit hash: b485e50
- commit date: 2025-09-17
- overall geometric mean: 1.109x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.4 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| tomli_loads          | 957 ms                                                   | 903 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 98.8 us: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                   |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 538 ms: 2.03x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.52x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.45 us: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.4 ms: 1.26x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.1 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.6 ns: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.0 ms: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.0 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 62.8 us: 1.13x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.50 us: 1.12x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.29 us: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.7 ms: 1.08x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.9 ms: 1.06x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 903 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 98.8 us: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                   |
| thrift                           | 322 us                                                   | 314 us: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.02x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 656 ms: 1.01x faster                                                    |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                   |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.75 ms: 1.05x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.3 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 919 us: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 326 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.4 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250917-3.15.0a0-b485e50/bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.109x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x