# Results vs. 3.12.6

- fork: python
- ref: 18d4e2ecd4e7414ef228
- machine: darwin-arm64
- commit hash: 18d4e2e
- commit date: 2025-10-03
- overall geometric mean: 1.074x faster
- HPT reliability: 93.17%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.39x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.38x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 213 ms: 2.15x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.9 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.4 ms: 2.47x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.5 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.8 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.50 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.1 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.64 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.01 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.6 ms: 1.13x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| mako            | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 779 us: 2.58x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.39x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.38x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 213 ms: 2.15x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.9 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.74x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 486 us: 1.71x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.3 us: 1.37x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.1 ms: 1.17x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 832 ns: 1.16x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.61 us: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 45.6 ns: 1.12x faster                                                   |
| go                               | 70.0 ms                                                  | 62.7 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.02 sec: 1.11x faster                                                  |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.3 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 134 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 202 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 19.4 ms: 1.07x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.8 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 136 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.8 ms: 1.01x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.54 us: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| regex_v8                         | 9.59 ms                                                  | 9.50 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.82 us: 1.01x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.09 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.3 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.9 ms: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                   |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 74.8 us: 1.05x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.5 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                   |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                   |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 357 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 725 ms: 1.09x slower                                                    |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.7 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.3 ms: 1.11x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.6 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.12 ms: 1.20x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.64 ms: 1.20x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 57.4 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.01 ms: 1.23x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 553 us: 1.32x slower                                                    |
| coverage                         | 26.9 ms                                                  | 41.2 ms: 1.53x slower                                                   |
| many_optionals                   | 195 us                                                   | 348 us: 1.78x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.4 ms: 2.47x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251003-3.15.0a0-18d4e2e-NOGIL/bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 93.17% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x