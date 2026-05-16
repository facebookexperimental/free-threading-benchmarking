# Results vs. 3.12.6

- fork: python
- ref: e56ae817e5f3df37a603
- machine: darwin-arm64
- commit hash: e56ae81
- commit date: 2026-05-15
- overall geometric mean: 1.108x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| sphinx         | 434 ms                                                   | 439 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 281 ms: 1.77x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 270 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 276 ms: 1.62x faster                                                    |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 171 ms: 1.34x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 128 ms: 1.34x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 133 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 283 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 289 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 119 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.8 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 106 ms: 3.31x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.5 ms: 1.16x faster                                                   |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.1 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 51.3 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.1 ms: 1.23x faster                                                   |
| tomli_loads          | 957 ms                                                   | 845 ms: 1.13x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.2 ms: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| mako            | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.22 ms: 4.92x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 790 us: 2.54x faster                                                    |
| pylint                           | 128 ms                                                   | 52.9 ms: 2.42x faster                                                   |
| mdp                              | 1.09 sec                                                 | 594 ms: 1.84x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 281 ms: 1.77x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 270 ms: 1.70x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 508 us: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 276 ms: 1.62x faster                                                    |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                   |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 171 ms: 1.34x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 128 ms: 1.34x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 133 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 55.3 us: 1.28x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.1 ms: 1.23x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 789 ns: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.10 us: 1.21x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.3 ns: 1.20x faster                                                   |
| go                               | 70.0 ms                                                  | 58.2 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 283 ms: 1.20x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                   |
| float                            | 37.9 ms                                                  | 32.5 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 289 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                    |
| pyflate                          | 216 ms                                                   | 189 ms: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 845 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.32 us: 1.11x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 119 ms: 1.11x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.3 ms: 1.10x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.56 us: 1.10x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.1 ms: 1.09x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                   |
| pycparser                        | 497 ms                                                   | 457 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.4 ms: 1.08x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.5 ms: 1.07x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 51.3 ms: 1.06x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.06x faster                                                   |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                   |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.68 ms: 1.03x faster                                                   |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.94 ms: 1.01x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 45.8 ms: 1.01x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                   |
| sphinx                           | 434 ms                                                   | 439 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 674 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| hexiom                           | 3.04 ms                                                  | 3.11 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 330 us: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.03x slower                                                   |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 28.2 ms: 1.05x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.06x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 184 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.4 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 61.3 ms: 1.19x slower                                                   |
| connected_components             | 201 ms                                                   | 242 ms: 1.21x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 257 us: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 572 us: 1.37x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.44x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 106 ms: 3.31x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): html5lib, dask, json_loads
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260515-3.16.0a0-e56ae81-NOGIL/bm-20260515-macm4pro-arm64-python-e56ae817e5f3df37a603-3.16.0a0-e56ae81.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.34x