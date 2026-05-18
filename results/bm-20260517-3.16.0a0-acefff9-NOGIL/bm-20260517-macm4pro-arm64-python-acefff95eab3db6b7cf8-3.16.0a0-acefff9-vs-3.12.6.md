# Results vs. 3.12.6

- fork: python
- ref: acefff95eab3db6b7cf8
- machine: darwin-arm64
- commit hash: acefff9
- commit date: 2026-05-17
- overall geometric mean: 1.105x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| sphinx         | 434 ms                                                   | 440 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 279 ms: 1.78x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 273 ms: 1.76x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 269 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                    |
| async_generators                 | 206 ms                                                   | 151 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 171 ms: 1.35x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 132 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 282 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 288 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 119 ms: 1.11x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.3 ms: 1.00x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.8 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| tomli_loads          | 957 ms                                                   | 857 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.5 ms: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.20 ms: 4.94x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 802 us: 2.51x faster                                                    |
| pylint                           | 128 ms                                                   | 53.3 ms: 2.40x faster                                                   |
| mdp                              | 1.09 sec                                                 | 588 ms: 1.86x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 279 ms: 1.78x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 273 ms: 1.76x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 269 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 508 us: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                    |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 151 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 171 ms: 1.35x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 132 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 55.5 us: 1.28x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 790 ns: 1.22x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.07 us: 1.22x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.4 ns: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 282 ms: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 58.5 ms: 1.20x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 288 ms: 1.16x faster                                                    |
| float                            | 37.9 ms                                                  | 32.8 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                   |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.12x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 857 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 119 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.34 us: 1.10x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                                   |
| pycparser                        | 497 ms                                                   | 459 ms: 1.08x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.5 ms: 1.08x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.4 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 50.9 ms: 1.07x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.7 ms: 1.06x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.67 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.3 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 529 ms: 1.00x slower                                                    |
| sphinx                           | 434 ms                                                   | 440 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.9 ms: 1.02x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 682 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 28.5 ms: 1.06x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 185 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.7 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                   |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.7 ms: 1.15x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 61.0 ms: 1.19x slower                                                   |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 255 us: 1.30x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 573 us: 1.37x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                    |
| coverage                         | 26.9 ms                                                  | 38.2 ms: 1.42x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): json_loads, sympy_integrate, html5lib
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.105x faster

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.34x