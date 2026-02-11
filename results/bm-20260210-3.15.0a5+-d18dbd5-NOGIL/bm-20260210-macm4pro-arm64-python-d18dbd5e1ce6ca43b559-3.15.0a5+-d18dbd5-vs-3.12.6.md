# Results vs. 3.12.6

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: darwin-arm64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.110x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                     |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.1 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.9 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| tomli_loads          | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 106 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.74 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.07 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.7 ms: 1.02x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.09 ms: 5.08x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 806 us: 2.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 596 ms: 1.83x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 509 us: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                     |
| deepcopy                         | 161 us                                                   | 103 us: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| float                            | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 791 ns: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.13 us: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 59.2 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.7 ns: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 123 ms: 1.15x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.3 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.9 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 456 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.1 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.1 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 657 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.06 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.0 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.5 ms: 1.00x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.09 ms: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.8 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.10 ms: 1.02x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.7 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 106 us: 1.03x slower                                                     |
| nbody                            | 54.2 ms                                                  | 56.1 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.7 ms: 1.06x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 57.8 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.7 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.74 ms: 1.22x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.07 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 261 us: 1.34x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 562 us: 1.34x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.2 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (5): xml_etree_process, async_tree_eager, dask, pidigits, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260210-3.15.0a5+-d18dbd5-NOGIL/bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.36x