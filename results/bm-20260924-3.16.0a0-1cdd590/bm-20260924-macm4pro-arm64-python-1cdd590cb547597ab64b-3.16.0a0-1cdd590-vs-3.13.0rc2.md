# Results vs. 3.13.0rc2

- fork: python
- ref: 1cdd590cb547597ab64b
- machine: darwin-arm64
- commit hash: 1cdd590
- commit date: 2026-09-24
- overall geometric mean: 1.047x faster
- HPT reliability: 97.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 950 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.4 ms: 1.08x faster                                                   |
| sphinx         | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 345 ms: 1.52x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.23x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.35 ms: 1.15x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 343 ms: 1.13x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 295 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 251 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.9 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.60x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 43.0 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 795 ms: 1.26x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.3 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.8 us: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.06x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 66.8 ms: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.28 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.75 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 510 ms: 2.08x faster                                                    |
| pylint                           | 106 ms                                                         | 56.1 ms: 1.88x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 345 ms: 1.52x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.12 ms: 1.52x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.0 us: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 983 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                   |
| go                               | 72.6 ms                                                        | 52.1 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 49.8 us: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 795 ms: 1.26x faster                                                    |
| pyflate                          | 222 ms                                                         | 180 ms: 1.23x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.23x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.21x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 837 us: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.35 ms: 1.15x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 343 ms: 1.13x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.11x faster                                                   |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 950 ms: 1.10x faster                                                    |
| fannkuch                         | 179 ms                                                         | 162 ms: 1.10x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.3 ms: 1.09x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.4 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.9 ms: 1.07x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.66 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 34.9 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 304 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.96 ms: 1.04x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 625 ms: 1.04x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.2 ms: 1.04x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 96.8 us: 1.03x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 295 ms: 1.02x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.67 us: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 932 ns: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.4 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.43 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 311 us: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.0 ms: 1.01x slower                                                   |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 211 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 489 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.0 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.06x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.8 ms: 1.07x slower                                                   |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.28 ms: 1.07x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.10x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 251 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.75 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.5 ms: 1.18x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                   |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 64.9 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.60x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (4): logging_silent, json_loads, async_tree_memoization, xml_etree_generate
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.047x faster

# HPT report

- Reliability score: 97.80% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x