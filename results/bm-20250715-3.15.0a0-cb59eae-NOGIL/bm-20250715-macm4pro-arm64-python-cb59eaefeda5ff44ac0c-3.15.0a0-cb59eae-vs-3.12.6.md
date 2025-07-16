# Results vs. 3.12.6

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: darwin-arm64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.112x faster
- HPT reliability: 99.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 988 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.33x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.8 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.2 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| tomli_loads          | 957 ms                                                   | 966 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.58 ms: 1.08x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| mako            | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                   |
| django_template | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 766 us: 2.62x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.33x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.69 ms: 2.14x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 85.8 ms: 2.01x faster                                                   |
| mdp                              | 1.09 sec                                                 | 570 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.73x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 480 us: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.37x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.5 us: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.91 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 810 ns: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| go                               | 70.0 ms                                                  | 59.6 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.8 ns: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.7 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 988 ms: 1.03x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.2 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.51 us: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.99 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.92 ms: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 966 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.4 us: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 330 us: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 340 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.4 ms: 1.04x slower                                                   |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 692 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.1 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.2 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.06x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.58 ms: 1.08x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 55.3 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.1 ms: 1.08x slower                                                   |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.4 ms: 1.12x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.0 ms: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.20 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 243 us: 1.24x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 590 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (5): html5lib, pidigits, logging_format, chaos, nbody
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 99.67% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x