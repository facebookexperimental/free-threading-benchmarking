# Results vs. 3.13.0rc2

- fork: python
- ref: dffac6163e693cf80ed4
- machine: darwin-arm64
- commit hash: dffac61
- commit date: 2026-08-14
- overall geometric mean: 1.040x faster
- HPT reliability: 95.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 967 ms: 1.08x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 339 ms: 1.54x faster                                                    |
| async_generators                 | 193 ms                                                         | 146 ms: 1.33x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 123 ms: 1.15x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 180 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 296 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.63x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                   |
| nbody          | 42.5 ms                                                        | 41.9 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 852 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 68.4 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.27 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.42 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 528 ms: 2.00x faster                                                    |
| pylint                           | 106 ms                                                         | 57.5 ms: 1.84x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 339 ms: 1.54x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.20 ms: 1.49x faster                                                   |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 102 us: 1.42x faster                                                    |
| go                               | 72.6 ms                                                        | 54.1 ms: 1.34x faster                                                   |
| async_generators                 | 193 ms                                                         | 146 ms: 1.33x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 48.8 ms: 1.31x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 49.7 us: 1.30x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 186 ms: 1.20x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 852 ms: 1.17x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 847 us: 1.17x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 123 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.15x faster                                                   |
| fannkuch                         | 179 ms                                                         | 164 ms: 1.09x faster                                                    |
| docutils                         | 1.05 sec                                                       | 967 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| float                            | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.0 ms: 1.07x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.7 ms: 1.06x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.6 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.6 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.96 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.2 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 180 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 927 ns: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 296 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| nbody                            | 42.5 ms                                                        | 41.9 ms: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 318 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.76 us: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.57 ms: 1.01x slower                                                   |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 655 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.1 ns: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 498 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.27 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.42 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 68.4 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 51.1 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                   |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.3 ms: 1.23x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.63x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (5): async_tree_none_tg, logging_simple, json_loads, logging_format, sphinx
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260814-3.16.0a0-dffac61/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 95.37% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x