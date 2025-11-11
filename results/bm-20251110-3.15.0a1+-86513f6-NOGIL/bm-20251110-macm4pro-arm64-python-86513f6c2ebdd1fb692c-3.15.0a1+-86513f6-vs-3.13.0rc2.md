# Results vs. 3.13.0rc2

- fork: python
- ref: 86513f6c2ebdd1fb692c
- machine: darwin-arm64
- commit hash: 86513f6
- commit date: 2025-11-10
- overall geometric mean: 1.015x slower
- HPT reliability: 87.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 199 ms: 2.62x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.53x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 203 ms: 1.99x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 214 ms: 1.80x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.48x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 89.8 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.1 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.4 ms: 1.03x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.8 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.40 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.13 ms: 1.13x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.7 ms: 1.05x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 984 ms: 1.02x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.5 ms: 1.09x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.20x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.79 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.10 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.9 ms: 1.17x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| mako            | 4.41 ms                                                        | 5.94 ms: 1.35x slower                                                    |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.27x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 767 us: 2.66x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 199 ms: 2.62x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 208 ms: 2.53x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 476 us: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 203 ms: 1.99x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 214 ms: 1.80x faster                                                     |
| mdp                              | 1.06 sec                                                       | 616 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.48x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 89.8 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.4 us: 1.23x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| go                               | 72.6 ms                                                        | 62.9 ms: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.9 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.40 ms: 1.14x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.13 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 853 ns: 1.11x faster                                                     |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.03 sec: 1.05x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.7 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.4 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 984 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| pycparser                        | 470 ms                                                         | 482 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.5 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| richards                         | 22.1 ms                                                        | 24.5 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| thrift                           | 309 us                                                         | 346 us: 1.12x slower                                                     |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.9 ms: 1.13x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.79 ms: 1.13x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 46.2 ns: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 368 ms: 1.14x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 747 ms: 1.15x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.5 ms: 1.15x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.59 us: 1.16x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.16x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 75.3 us: 1.17x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.9 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.89 us: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.0 ms: 1.19x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 114 ms: 1.19x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 57.0 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.10 ms: 1.19x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.20x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.8 ms: 1.20x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 195 ms: 1.22x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.7 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.23x slower                                                    |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.58 us: 1.26x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.25 ms: 1.26x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 533 us: 1.30x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 43.6 ms: 1.30x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.94 ms: 1.35x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 58.1 ms: 1.36x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.8 ms: 1.36x slower                                                    |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| many_optionals                   | 200 us                                                         | 389 us: 1.94x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.1 ms: 2.77x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 19.5 ms: 3.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): deepcopy_reduce
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251110-3.15.0a1+-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1+-86513f6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x slower

# HPT report

- Reliability score: 87.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x