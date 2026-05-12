# Results vs. 3.12.6

- fork: python
- ref: 7a4c6dfb8839eb05fb87
- machine: darwin-arm64
- commit hash: 7a4c6df
- commit date: 2026-05-11
- overall geometric mean: 1.160x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 947 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.8 ms: 1.06x faster                                                   |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 300 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.51x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 305 ms: 1.51x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 324 ms: 1.48x faster                                                    |
| async_generators                 | 206 ms                                                   | 145 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 123 ms: 1.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 326 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.36x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.36x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 174 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 276 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 256 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 149 ms: 1.32x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 100 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.9 ms: 1.23x faster                                                   |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                   |
| tomli_loads          | 957 ms                                                   | 814 ms: 1.18x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.7 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.06x faster                                                   |
| pylint                           | 128 ms                                                   | 55.4 ms: 2.31x faster                                                   |
| mdp                              | 1.09 sec                                                 | 501 ms: 2.18x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 300 ms: 1.65x faster                                                    |
| deepcopy                         | 161 us                                                   | 98.0 us: 1.65x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.51x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 305 ms: 1.51x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 324 ms: 1.48x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.0 us: 1.48x faster                                                   |
| async_generators                 | 206 ms                                                   | 145 ms: 1.43x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.99 us: 1.41x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 123 ms: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.37x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 326 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.36x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 170 ms: 1.36x faster                                                    |
| go                               | 70.0 ms                                                  | 51.9 ms: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 174 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.28x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.4 ms: 1.26x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 34.9 ms: 1.24x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.6 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.0 ns: 1.24x faster                                                   |
| nbody                            | 54.2 ms                                                  | 43.9 ms: 1.23x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 45.1 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 276 ms: 1.21x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.20x faster                                                   |
| pyflate                          | 216 ms                                                   | 180 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.5 ms: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 814 ms: 1.18x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.17x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.9 ms: 1.16x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.70 ms: 1.13x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 45.9 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                  |
| sympy_integrate                  | 8.02 ms                                                  | 7.25 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.10x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| docutils                         | 1.02 sec                                                 | 947 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 53.6 ms: 1.07x faster                                                   |
| sympy_str                        | 104 ms                                                   | 97.2 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.8 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.91 ms: 1.05x faster                                                   |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                   |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 924 ns: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 635 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.7 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                    |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.6 ms: 1.01x faster                                                   |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                   |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 858 us: 1.03x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 256 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.4 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 149 ms: 1.32x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 100 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                            |

Benchmark hidden because not significant (2): regex_v8, mako
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.160x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.21x