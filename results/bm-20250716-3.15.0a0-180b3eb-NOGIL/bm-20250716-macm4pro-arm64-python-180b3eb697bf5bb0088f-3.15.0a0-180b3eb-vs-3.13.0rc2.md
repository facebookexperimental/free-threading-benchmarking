# Results vs. 3.13.0rc2

- fork: python
- ref: 180b3eb697bf5bb0088f
- machine: darwin-arm64
- commit hash: 180b3eb
- commit date: 2025-07-16
- overall geometric mean: 1.021x faster
- HPT reliability: 70.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.1 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.7 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.8 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.3 ms: 1.04x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.63 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.47 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 775 us: 2.63x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 484 us: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| mdp                              | 1.06 sec                                                       | 580 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.1 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.7 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.5 ms: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 816 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.5 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| float                            | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.3 ms: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.63 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.03x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.95 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.05 ms: 1.07x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.7 ms: 1.08x slower                                                   |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 348 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.08x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 707 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.3 ns: 1.09x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.47 ms: 1.10x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.5 us: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.92 us: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.17x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.88 us: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.6 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.26x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.3 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.5 ms: 1.33x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.4 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 592 us: 1.44x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.79 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.8 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (4): sphinx, pycparser, tomli_loads, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 70.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x