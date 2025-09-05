# Results vs. 3.12.6

- fork: python
- ref: fc0305a2d8bef7cffaa4
- machine: darwin-arm64
- commit hash: fc0305a
- commit date: 2025-09-04
- overall geometric mean: 1.077x faster
- HPT reliability: 93.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                    |
| docutils       | 1.02 sec                                                 | 993 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.04 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 981 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.56 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.6 ms: 1.13x slower                                                   |
| mako            | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 769 us: 2.61x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| mdp                              | 1.09 sec                                                 | 617 ms: 1.77x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.76x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 477 us: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.34x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 833 ns: 1.16x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.51 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.2 ns: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1000 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| go                               | 70.0 ms                                                  | 62.7 ms: 1.12x faster                                                   |
| async_generators                 | 206 ms                                                   | 185 ms: 1.11x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.8 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.0 ms: 1.09x faster                                                   |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 203 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.0 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.04 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 993 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.54 us: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.00x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.3 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 981 ms: 1.02x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 146 ms: 1.03x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.7 ms: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.2 us: 1.05x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.06x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                    |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 354 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 721 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                    |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.2 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.1 ms: 1.11x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.33 ms: 1.12x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.6 ms: 1.13x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.7 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.56 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.77 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 591 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 337 us: 1.73x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (3): async_tree_eager_memoization_tg, dask, logging_format
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 93.74% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x