# Results vs. 3.12.6

- fork: python
- ref: dc28c3a358221b1e0ae5
- machine: darwin-arm64
- commit hash: dc28c3a
- commit date: 2026-10-23
- overall geometric mean: 1.202x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| docutils       | 1.02 sec                                                 | 903 ms: 1.13x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.1 ms: 1.14x faster                                                       |
| sphinx         | 434 ms                                                   | 387 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 100 ms: 2.06x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.91x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.74x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 273 ms: 1.63x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                       |
| nbody          | 54.2 ms                                                  | 41.5 ms: 1.31x faster                                                       |
| pidigits       | 161 ms                                                   | 159 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                    | 1.22x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.8 ms: 1.12x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.02 ms: 1.06x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.8 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.50 ms: 1.22x faster                                                       |
| tomli_loads          | 957 ms                                                   | 799 ms: 1.20x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 92.9 us: 1.11x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.11x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.2 us: 1.06x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.21 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.39 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                       |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.91 ms: 5.31x faster                                                       |
| pylint                           | 128 ms                                                   | 51.4 ms: 2.49x faster                                                       |
| mdp                              | 1.09 sec                                                 | 498 ms: 2.19x faster                                                        |
| async_generators                 | 206 ms                                                   | 100 ms: 2.06x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.91x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.74x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| deepcopy                         | 161 us                                                   | 94.7 us: 1.71x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 273 ms: 1.63x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.57 us: 1.50x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 49.5 us: 1.43x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 609 us: 1.36x faster                                                        |
| float                            | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                       |
| go                               | 70.0 ms                                                  | 52.0 ms: 1.35x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.4 ms: 1.31x faster                                                       |
| nbody                            | 54.2 ms                                                  | 41.5 ms: 1.31x faster                                                       |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 111 ms: 1.28x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.8 ms: 1.25x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.50 ms: 1.22x faster                                                       |
| generators                       | 21.9 ms                                                  | 18.2 ms: 1.21x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                       |
| pyflate                          | 216 ms                                                   | 180 ms: 1.20x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 799 ms: 1.20x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.20x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.20x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.1 ms: 1.19x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                      |
| chaos                            | 28.9 ms                                                  | 24.5 ms: 1.18x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 43.1 ns: 1.18x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.73 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 967 ms: 1.16x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.66 ms: 1.14x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 20.1 ms: 1.14x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                       |
| docutils                         | 1.02 sec                                                 | 903 ms: 1.13x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 88.8 ms: 1.12x faster                                                       |
| sphinx                           | 434 ms                                                   | 387 ms: 1.12x faster                                                        |
| fannkuch                         | 176 ms                                                   | 158 ms: 1.11x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 92.9 us: 1.11x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.11x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.29 ms: 1.10x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.7 ms: 1.10x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 63.1 ms: 1.08x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.2 ms: 1.07x faster                                                       |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                        |
| json                             | 1.93 ms                                                  | 1.80 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| sympy_str                        | 104 ms                                                   | 98.0 ms: 1.06x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.02 ms: 1.06x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.2 us: 1.06x faster                                                       |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 630 ms: 1.06x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 919 ns: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                       |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| pidigits                         | 161 ms                                                   | 159 ms: 1.02x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.8 ms: 1.02x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 413 us: 1.01x faster                                                        |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.21 ms: 1.02x slower                                                       |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 42.4 ms: 1.07x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.39 ms: 1.12x slower                                                       |
| many_optionals                   | 195 us                                                   | 221 us: 1.13x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (3): sympy_expand, meteor_contest, pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261023-3.16.0a1+dev-dc28c3a/bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.202x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.15x