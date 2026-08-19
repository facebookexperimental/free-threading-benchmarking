# Results vs. 3.12.6

- fork: python
- ref: af49df919dafc3767ae9
- machine: darwin-arm64
- commit hash: af49df9
- commit date: 2026-08-18
- overall geometric mean: 1.013x faster
- HPT reliability: 69.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 136 ms: 1.19x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 464 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 312 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 306 ms: 1.46x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 317 ms: 1.45x faster                                                    |
| async_generators                 | 206 ms                                                   | 163 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 148 ms: 1.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 146 ms: 1.18x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 191 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 302 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 308 ms: 1.08x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.9 ms: 1.05x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 239 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 52.0 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| nbody          | 54.2 ms                                                  | 64.2 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 68.6 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.8 ms: 1.23x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.13x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| tomli_loads          | 957 ms                                                   | 922 ms: 1.04x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 39.2 ms: 1.01x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 117 us: 1.14x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 165 us: 1.18x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.6 ms: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.00x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.2 ms: 1.27x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.28 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.27x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.90 ms: 1.24x slower                                                   |
| django_template | 13.6 ms                                                  | 17.9 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.27x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.62 ms: 4.49x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 784 us: 2.56x faster                                                    |
| pylint                           | 128 ms                                                   | 54.5 ms: 2.35x faster                                                   |
| mdp                              | 1.09 sec                                                 | 627 ms: 1.74x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 493 us: 1.68x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 312 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 306 ms: 1.46x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 317 ms: 1.45x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| async_generators                 | 206 ms                                                   | 163 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.8 ms: 1.23x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.9 us: 1.23x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 148 ms: 1.20x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 809 ns: 1.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 146 ms: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 60.9 us: 1.17x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 191 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 302 ms: 1.12x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.78 us: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.10x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 308 ms: 1.08x faster                                                    |
| float                            | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 20.1 ms: 1.06x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 12.9 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| go                               | 70.0 ms                                                  | 66.8 ms: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 922 ms: 1.04x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 49.6 ns: 1.03x faster                                                   |
| pyflate                          | 216 ms                                                   | 212 ms: 1.02x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 53.9 ms: 1.01x faster                                                   |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 39.2 ms: 1.01x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.3 ms: 1.02x slower                                                   |
| scimark_sor                      | 61.0 ms                                                  | 62.1 ms: 1.02x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 509 ms: 1.02x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 239 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.55 ms: 1.07x slower                                                   |
| sphinx                           | 434 ms                                                   | 464 ms: 1.07x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 62.8 ms: 1.09x slower                                                   |
| fannkuch                         | 176 ms                                                   | 193 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.5 ms: 1.10x slower                                                   |
| raytrace                         | 145 ms                                                   | 160 ms: 1.10x slower                                                    |
| sympy_str                        | 104 ms                                                   | 116 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 364 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| chaos                            | 28.9 ms                                                  | 32.2 ms: 1.11x slower                                                   |
| thrift                           | 322 us                                                   | 359 us: 1.12x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 750 ms: 1.13x slower                                                    |
| generators                       | 21.9 ms                                                  | 24.8 ms: 1.13x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 52.0 ms: 1.14x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 117 us: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.8 ms: 1.15x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 194 ms: 1.16x slower                                                    |
| shortest_path                    | 219 ms                                                   | 256 ms: 1.17x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.56 ms: 1.17x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 165 us: 1.18x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.6 ms: 1.18x slower                                                   |
| nbody                            | 54.2 ms                                                  | 64.2 ms: 1.18x slower                                                   |
| richards                         | 22.4 ms                                                  | 26.8 ms: 1.19x slower                                                   |
| 2to3                             | 114 ms                                                   | 136 ms: 1.19x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 30.4 ms: 1.20x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.14 ms: 1.20x slower                                                   |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.90 ms: 1.24x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 68.6 ms: 1.26x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.2 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.28 ms: 1.28x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 2.21 ms: 1.28x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.9 ms: 1.31x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 578 us: 1.38x slower                                                    |
| many_optionals                   | 195 us                                                   | 271 us: 1.39x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 74.7 ms: 1.46x slower                                                   |
| coverage                         | 26.9 ms                                                  | 41.3 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 69.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x