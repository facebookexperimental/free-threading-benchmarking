# Results vs. 3.12.6

- fork: python
- ref: cb3b4b98d8d141c9de04
- machine: darwin-arm64
- commit hash: cb3b4b9
- commit date: 2026-05-20
- overall geometric mean: 1.122x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 973 ms: 1.05x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                   |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 312 ms: 1.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                    |
| async_generators                 | 206 ms                                                   | 147 ms: 1.41x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 337 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 278 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                   |
| nbody          | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                   |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.2 ms: 1.16x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.3 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.73 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|---------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse | 51.6 ms                                                  | 43.4 ms: 1.19x faster                                                   |
| tomli_loads         | 957 ms                                                   | 831 ms: 1.15x faster                                                    |
| json_dumps          | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| xml_etree_generate  | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| json_loads          | 10.9 us                                                  | 10.5 us: 1.03x faster                                                   |
| xml_etree_parse     | 67.9 ms                                                  | 66.8 ms: 1.02x faster                                                   |
| xml_etree_process   | 26.7 ms                                                  | 26.3 ms: 1.02x faster                                                   |
| pickle_pure_python  | 139 us                                                   | 145 us: 1.04x slower                                                    |
| Geometric mean      | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.18 ms: 4.96x faster                                                   |
| pylint                           | 128 ms                                                   | 57.0 ms: 2.25x faster                                                   |
| mdp                              | 1.09 sec                                                 | 519 ms: 2.10x faster                                                    |
| deepcopy                         | 161 us                                                   | 99.9 us: 1.62x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 312 ms: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.8 us: 1.42x faster                                                   |
| async_generators                 | 206 ms                                                   | 147 ms: 1.41x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.30 us: 1.35x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 337 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                   |
| go                               | 70.0 ms                                                  | 54.1 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                    |
| float                            | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.0 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.3 ms: 1.21x faster                                                   |
| nbody                            | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 278 ms: 1.20x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.5 ns: 1.20x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.4 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.2 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 831 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.15x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.3 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.50 us: 1.12x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.31 us: 1.11x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.8 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.3 ms: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.09x faster                                                  |
| hexiom                           | 3.04 ms                                                  | 2.81 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.59 ms: 1.06x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 94.3 ms: 1.06x faster                                                   |
| docutils                         | 1.02 sec                                                 | 973 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 314 ms: 1.05x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.4 ms: 1.04x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 639 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.03x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                   |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 489 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.8 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 951 ns: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.3 ms: 1.02x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.5 ms: 1.02x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.73 ms: 1.02x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                    |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 40.4 ms: 1.04x slower                                                   |
| connected_components             | 201 ms                                                   | 211 ms: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 876 us: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.7 ms: 1.18x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 245 us: 1.26x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 58.5 ms: 1.35x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (3): thrift, unpickle_pure_python, pidigits
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, asyncio_websockets, chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260520-3.16.0a0-cb3b4b9/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.122x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.21x