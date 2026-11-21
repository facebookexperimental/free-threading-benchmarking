# Results vs. 3.12.6

- fork: python
- ref: ab5b8f87a70b62a22c1e
- machine: darwin-arm64
- commit hash: ab5b8f8
- commit date: 2026-11-20
- overall geometric mean: 1.202x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 896 ms: 1.14x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                       |
| sphinx         | 434 ms                                                   | 381 ms: 1.14x faster                                                        |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 98.5 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 279 ms: 1.72x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 280 ms: 1.59x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.59 ms: 1.42x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.25x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.5 ms: 2.91x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                       |
| nbody          | 54.2 ms                                                  | 41.2 ms: 1.32x faster                                                       |
| pidigits       | 161 ms                                                   | 146 ms: 1.10x faster                                                        |
| Geometric mean | (ref)                                                    | 1.26x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.08 ms: 1.06x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                       |
| tomli_loads          | 957 ms                                                   | 820 ms: 1.17x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.2 ms: 1.10x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 94.5 us: 1.09x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 66.1 ms: 1.03x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.04 ms: 1.00x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.33 ms: 1.10x faster                                                       |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.93 ms: 5.28x faster                                                       |
| pylint                           | 128 ms                                                   | 50.3 ms: 2.55x faster                                                       |
| mdp                              | 1.09 sec                                                 | 504 ms: 2.16x faster                                                        |
| async_generators                 | 206 ms                                                   | 98.5 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 279 ms: 1.72x faster                                                        |
| deepcopy                         | 161 us                                                   | 94.9 us: 1.70x faster                                                       |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 280 ms: 1.59x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.2 us: 1.57x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.78 us: 1.45x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.59 ms: 1.42x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.41x faster                                                       |
| float                            | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| go                               | 70.0 ms                                                  | 51.5 ms: 1.36x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.0 ms: 1.32x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 628 us: 1.32x faster                                                        |
| nbody                            | 54.2 ms                                                  | 41.2 ms: 1.32x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 110 ms: 1.29x faster                                                        |
| generators                       | 21.9 ms                                                  | 17.1 ms: 1.28x faster                                                       |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 47.7 ms: 1.28x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 40.1 ns: 1.27x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.6 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.25x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 41.3 ms: 1.24x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.2 ms: 1.23x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.22x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.86 sec: 1.20x faster                                                      |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.20x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.75 ms: 1.19x faster                                                       |
| pyflate                          | 216 ms                                                   | 182 ms: 1.18x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 820 ms: 1.17x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.16x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                       |
| k_core                           | 1.12 sec                                                 | 974 ms: 1.15x faster                                                        |
| docutils                         | 1.02 sec                                                 | 896 ms: 1.14x faster                                                        |
| sphinx                           | 434 ms                                                   | 381 ms: 1.14x faster                                                        |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.81 ms: 1.11x faster                                                       |
| fannkuch                         | 176 ms                                                   | 158 ms: 1.11x faster                                                        |
| xml_etree_process                | 26.7 ms                                                  | 24.2 ms: 1.10x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.33 ms: 1.10x faster                                                       |
| pidigits                         | 161 ms                                                   | 146 ms: 1.10x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.28 ms: 1.10x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 91.2 ms: 1.09x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 94.5 us: 1.09x faster                                                       |
| pycparser                        | 497 ms                                                   | 463 ms: 1.07x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.4 ms: 1.07x faster                                                       |
| sympy_str                        | 104 ms                                                   | 98.2 ms: 1.06x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 54.4 ms: 1.06x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.08 ms: 1.06x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 918 ns: 1.05x faster                                                        |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 315 ms: 1.04x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 642 ms: 1.03x faster                                                        |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 66.1 ms: 1.03x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 8.04 ms: 1.00x slower                                                       |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                        |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 49.2 ms: 1.03x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                       |
| many_optionals                   | 195 us                                                   | 229 us: 1.17x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.5 ms: 2.91x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (3): 2to3, sympy_expand, pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261120-3.16.0a2+dev-ab5b8f8/bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.202x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.15x