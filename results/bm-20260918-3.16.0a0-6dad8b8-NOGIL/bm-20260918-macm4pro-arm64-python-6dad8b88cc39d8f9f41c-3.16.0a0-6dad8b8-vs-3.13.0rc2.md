# Results vs. 3.13.0rc2

- fork: python
- ref: 6dad8b88cc39d8f9f41c
- machine: darwin-arm64
- commit hash: 6dad8b8
- commit date: 2026-09-18
- overall geometric mean: 1.071x slower
- HPT reliability: 99.79%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 138 ms: 1.23x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 307 ms: 1.70x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 317 ms: 1.66x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 312 ms: 1.30x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 322 ms: 1.20x faster                                                    |
| async_generators                 | 193 ms                                                         | 168 ms: 1.15x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 315 ms: 1.07x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 204 ms: 1.10x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 164 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 264 ms: 1.17x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 13.2 ms: 1.23x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 151 ms: 1.24x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 282 ms: 1.36x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 168 ms: 1.63x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 71.3 ms: 1.65x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x slower                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| float          | 31.4 ms                                                        | 35.2 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 62.0 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 69.7 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 952 ms: 1.05x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 40.3 ms: 1.12x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 118 us: 1.19x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.5 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 167 us: 1.28x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.2 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.45 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.39x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 777 us: 2.63x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 486 us: 2.04x faster                                                    |
| pylint                           | 106 ms                                                         | 54.3 ms: 1.94x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 307 ms: 1.70x faster                                                    |
| mdp                              | 1.06 sec                                                       | 637 ms: 1.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 317 ms: 1.66x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.62 ms: 1.36x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 312 ms: 1.30x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 322 ms: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 168 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                   |
| go                               | 72.6 ms                                                        | 66.8 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 952 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| pyflate                          | 222 ms                                                         | 214 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.2 us: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 62.1 ms: 1.03x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 16.0 us: 1.03x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| pycparser                        | 470 ms                                                         | 502 ms: 1.07x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 315 ms: 1.07x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 204 ms: 1.10x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.12x slower                                                    |
| float                            | 31.4 ms                                                        | 35.2 ms: 1.12x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 40.3 ms: 1.12x slower                                                   |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                    |
| sphinx                           | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.57 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.2 ms: 1.15x slower                                                   |
| async_tree_none                  | 142 ms                                                         | 164 ms: 1.15x slower                                                    |
| thrift                           | 309 us                                                         | 361 us: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 264 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.4 ms: 1.17x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.2 ms: 1.19x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.65 us: 1.19x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 382 ms: 1.19x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 118 us: 1.19x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.93 us: 1.20x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.4 ms: 1.20x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 36.2 ms: 1.21x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 116 ms: 1.21x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 789 ms: 1.21x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.7 ms: 1.22x slower                                                   |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 45.6 ms: 1.22x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.2 ms: 1.23x slower                                                   |
| 2to3                             | 112 ms                                                         | 138 ms: 1.23x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 197 ms: 1.24x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 151 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.5 ms: 1.24x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.7 ms: 1.24x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.45 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.59 ms: 1.26x slower                                                   |
| chaos                            | 24.3 ms                                                        | 30.9 ms: 1.27x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 167 us: 1.28x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 52.5 ns: 1.29x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.90 us: 1.31x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.1 ms: 1.32x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 282 ms: 1.36x slower                                                    |
| raytrace                         | 109 ms                                                         | 149 ms: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 564 us: 1.37x slower                                                    |
| many_optionals                   | 200 us                                                         | 275 us: 1.37x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.03 ms: 1.40x slower                                                   |
| django_template                  | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 69.7 ms: 1.46x slower                                                   |
| nbody                            | 42.5 ms                                                        | 62.0 ms: 1.46x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 65.2 ms: 1.52x slower                                                   |
| generators                       | 15.7 ms                                                        | 25.3 ms: 1.61x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 168 ms: 1.63x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 71.3 ms: 1.65x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (3): async_tree_memoization_tg, dulwich_log, async_tree_cpu_io_mixed_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-macm4pro-arm64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.071x slower

# HPT report

- Reliability score: 99.79% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.31x