# Results vs. 3.12.6

- fork: python
- ref: ef1fce0a69a19360643f
- machine: darwin-arm64
- commit hash: ef1fce0
- commit date: 2026-10-29
- overall geometric mean: 1.203x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.00x faster                                                        |
| docutils       | 1.02 sec                                                 | 898 ms: 1.14x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.3 ms: 1.14x faster                                                       |
| sphinx         | 434 ms                                                   | 385 ms: 1.13x faster                                                        |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 98.3 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 263 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 268 ms: 1.71x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.60x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.78 ms: 1.39x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.87x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.0 ms: 1.41x faster                                                       |
| nbody          | 54.2 ms                                                  | 43.8 ms: 1.24x faster                                                       |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                    | 1.21x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.0 ms: 1.12x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.00 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                       |
| tomli_loads          | 957 ms                                                   | 792 ms: 1.21x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 92.8 us: 1.11x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.06x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 64.8 ms: 1.05x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.19 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.45 ms: 1.07x faster                                                       |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.08x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.95 ms: 5.26x faster                                                       |
| pylint                           | 128 ms                                                   | 50.2 ms: 2.55x faster                                                       |
| mdp                              | 1.09 sec                                                 | 497 ms: 2.20x faster                                                        |
| async_generators                 | 206 ms                                                   | 98.3 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 263 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 268 ms: 1.71x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.0 us: 1.70x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.60x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 46.0 us: 1.54x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.59 us: 1.49x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.43x faster                                                       |
| float                            | 37.9 ms                                                  | 27.0 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.78 ms: 1.39x faster                                                       |
| go                               | 70.0 ms                                                  | 51.2 ms: 1.37x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 619 us: 1.34x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.3 ms: 1.32x faster                                                       |
| generators                       | 21.9 ms                                                  | 17.0 ms: 1.29x faster                                                       |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 48.3 ms: 1.26x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 34.7 ms: 1.25x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                        |
| nbody                            | 54.2 ms                                                  | 43.8 ms: 1.24x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 115 ms: 1.24x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 792 ms: 1.21x faster                                                        |
| pyflate                          | 216 ms                                                   | 179 ms: 1.21x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.8 ms: 1.20x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.20x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.35 us: 1.19x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                        |
| chaos                            | 28.9 ms                                                  | 24.5 ms: 1.18x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.17x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                      |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.61 ms: 1.16x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.74 ms: 1.15x faster                                                       |
| k_core                           | 1.12 sec                                                 | 972 ms: 1.15x faster                                                        |
| docutils                         | 1.02 sec                                                 | 898 ms: 1.14x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.3 ms: 1.14x faster                                                       |
| sphinx                           | 434 ms                                                   | 385 ms: 1.13x faster                                                        |
| richards                         | 22.4 ms                                                  | 19.9 ms: 1.12x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 89.0 ms: 1.12x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.21 ms: 1.11x faster                                                       |
| fannkuch                         | 176 ms                                                   | 158 ms: 1.11x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 92.8 us: 1.11x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.6 ms: 1.10x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.45 ms: 1.07x faster                                                       |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                        |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 307 ms: 1.07x faster                                                        |
| sympy_str                        | 104 ms                                                   | 97.6 ms: 1.07x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 907 ns: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.00 ms: 1.07x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.5 ms: 1.06x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 54.1 ms: 1.06x faster                                                       |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.06x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 629 ms: 1.06x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 64.8 ms: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 410 us: 1.02x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| 2to3                             | 114 ms                                                   | 113 ms: 1.00x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 48.1 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.19 ms: 1.02x slower                                                       |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                        |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.08x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.9 ms: 1.08x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                       |
| many_optionals                   | 195 us                                                   | 226 us: 1.16x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.87x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (2): pickle_pure_python, sympy_expand
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261029-3.16.0a1+dev-ef1fce0/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1+dev-ef1fce0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.203x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.15x