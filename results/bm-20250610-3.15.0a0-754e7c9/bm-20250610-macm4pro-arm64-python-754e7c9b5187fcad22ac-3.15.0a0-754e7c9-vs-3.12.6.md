# Results vs. 3.12.6

- fork: python
- ref: 754e7c9b5187fcad22ac
- machine: darwin-arm64
- commit hash: 754e7c9
- commit date: 2025-06-10
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.28x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.2 ms: 1.16x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.12x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.9 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.08x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 96.7 us: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 909 ms: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.42 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.56 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.14 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.80 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.00x slower                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.64 ms: 2.16x faster                                                   |
| mdp                              | 1.09 sec                                                 | 509 ms: 2.14x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 256 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.50x faster                                                   |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.38 us: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| go                               | 70.0 ms                                                  | 55.5 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.20x faster                                                   |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 46.2 ms: 1.18x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.2 ms: 1.16x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.2 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.1 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.5 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.9 ms: 1.12x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.9 ms: 1.10x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.1 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.37 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.08x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.80 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 302 us: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.7 us: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.1 ms: 1.06x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 909 ms: 1.05x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.2 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.52 us: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 488 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 956 ns: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 47.6 ms: 1.00x faster                                                   |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.00x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| connected_components             | 201 ms                                                   | 204 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.42 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 348 ms: 1.06x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 710 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.56 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.14 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 948 us: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.9 ms: 2.74x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): json_loads, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250610-3.15.0a0-754e7c9/bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x