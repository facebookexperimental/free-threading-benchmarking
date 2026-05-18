# Results vs. 3.12.6

- fork: python
- ref: acefff95eab3db6b7cf8
- machine: darwin-arm64
- commit hash: acefff9
- commit date: 2026-05-17
- overall geometric mean: 1.135x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 971 ms: 1.05x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                   |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 306 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 327 ms: 1.47x faster                                                    |
| async_generators                 | 206 ms                                                   | 147 ms: 1.41x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 333 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 278 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.0 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 45.2 ms: 1.20x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.15x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.5 ms: 1.17x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.9 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 839 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_pure_python

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.19 ms: 4.96x faster                                                   |
| pylint                           | 128 ms                                                   | 56.8 ms: 2.26x faster                                                   |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.10x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 306 ms: 1.62x faster                                                    |
| deepcopy                         | 161 us                                                   | 99.9 us: 1.62x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 327 ms: 1.47x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.7 us: 1.43x faster                                                   |
| async_generators                 | 206 ms                                                   | 147 ms: 1.41x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.22 us: 1.36x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 52.2 ms: 1.34x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 333 ms: 1.34x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.0 ns: 1.27x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.3 ms: 1.25x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.4 ms: 1.23x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.22x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.9 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 278 ms: 1.20x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.2 ms: 1.20x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 36.5 ms: 1.19x faster                                                   |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.5 ms: 1.17x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.15x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.25 us: 1.14x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 839 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.4 ms: 1.13x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.0 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.10x faster                                                  |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.0 ms: 1.10x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.8 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.50 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 971 ms: 1.05x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 638 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                   |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 939 ns: 1.03x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 319 ms: 1.03x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.0 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.2 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 488 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 40.0 ms: 1.03x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                   |
| shortest_path                    | 219 ms                                                   | 228 ms: 1.04x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 866 us: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 211 ms: 1.05x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.7 ms: 1.18x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 260 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_pure_python
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260517-3.16.0a0-acefff9/bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.135x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.21x