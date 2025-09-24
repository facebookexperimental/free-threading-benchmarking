# Results vs. 3.12.6

- fork: python
- ref: 1a2e00c97acfe9f79722
- machine: darwin-arm64
- commit hash: 1a2e00c
- commit date: 2025-09-23
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 398 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.3 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 46.5 ms: 1.17x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                   |
| tomli_loads          | 957 ms                                                   | 889 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.2 us: 1.06x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.67 ms: 1.08x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 527 ms: 2.07x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.53x faster                                                   |
| deepcopy                         | 161 us                                                   | 106 us: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.94 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.33 us: 1.34x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| go                               | 70.0 ms                                                  | 54.6 ms: 1.28x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.27x faster                                                   |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.0 ms: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.4 ns: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.7 ms: 1.18x faster                                                   |
| nbody                            | 54.2 ms                                                  | 46.5 ms: 1.17x faster                                                   |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.7 us: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.9 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| logging_simple                   | 2.57 us                                                  | 2.24 us: 1.15x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.47 us: 1.14x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.3 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.28 ms: 1.10x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.4 ms: 1.10x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.1 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 398 ms: 1.09x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.4 ms: 1.08x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.67 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.8 ms: 1.08x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 889 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.2 us: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 98.6 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.97 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 54.9 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 931 ns: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 649 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.01x faster                                                   |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 324 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 41.7 ms: 1.05x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 914 us: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 321 us: 1.64x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (3): sympy_expand, connected_components, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250923-3.15.0a0-1a2e00c/bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x