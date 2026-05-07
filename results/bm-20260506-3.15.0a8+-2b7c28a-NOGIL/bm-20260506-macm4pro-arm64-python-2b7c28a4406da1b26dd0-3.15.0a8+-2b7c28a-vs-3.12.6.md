# Results vs. 3.12.6

- fork: python
- ref: 2b7c28a4406da1b26dd0
- machine: darwin-arm64
- commit hash: 2b7c28a
- commit date: 2026-05-06
- overall geometric mean: 1.130x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 237 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.09x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.90x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| async_generators                 | 206 ms                                                   | 149 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.1 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.3 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.7 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| tomli_loads          | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.18 ms: 4.97x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 783 us: 2.56x faster                                                     |
| pylint                           | 128 ms                                                   | 50.8 ms: 2.52x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 237 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.09x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.90x faster                                                     |
| mdp                              | 1.09 sec                                                 | 589 ms: 1.85x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 509 us: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 149 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| float                            | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.10 us: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 802 ns: 1.21x faster                                                     |
| go                               | 70.0 ms                                                  | 58.6 ms: 1.20x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.8 ns: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.90 sec: 1.18x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 454 ms: 1.10x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.5 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.7 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.1 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.02x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 687 ms: 1.03x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 333 us: 1.03x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.9 us: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.12x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 53.6 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 44.1 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 61.5 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| many_optionals                   | 195 us                                                   | 255 us: 1.31x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 566 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.3 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (1): sympy_integrate
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260506-3.15.0a8+-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8+-2b7c28a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.130x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.37x