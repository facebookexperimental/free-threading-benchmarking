# Results vs. 3.13.0rc2

- fork: python
- ref: b38e073f1be8fe40af99
- machine: darwin-arm64
- commit hash: b38e073
- commit date: 2026-08-31
- overall geometric mean: 1.044x faster
- HPT reliability: 96.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 956 ms: 1.09x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 338 ms: 1.54x faster                                                    |
| async_generators                 | 193 ms                                                         | 146 ms: 1.32x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 123 ms: 1.16x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.79 ms: 1.10x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 179 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 296 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.63x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| nbody          | 42.5 ms                                                        | 42.8 ms: 1.01x slower                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.37 ms: 1.18x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.59 ms: 1.30x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 811 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.6 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 72.9 ms: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.34 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.78 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 518 ms: 2.04x faster                                                    |
| pylint                           | 106 ms                                                         | 57.1 ms: 1.85x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 338 ms: 1.54x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                   |
| deepcopy                         | 145 us                                                         | 97.5 us: 1.49x faster                                                   |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 52.8 ms: 1.37x faster                                                   |
| async_generators                 | 193 ms                                                         | 146 ms: 1.32x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.4 us: 1.31x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.59 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 811 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 183 ms: 1.22x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 832 us: 1.19x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.37 ms: 1.18x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 123 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                   |
| fannkuch                         | 179 ms                                                         | 161 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.79 ms: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 956 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.5 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.0 ms: 1.07x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.0 ms: 1.06x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.06x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 41.9 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.97 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 179 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 296 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 930 ns: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 643 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.6 us: 1.01x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.78 us: 1.00x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.46 us: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.57 ms: 1.01x slower                                                   |
| nbody                            | 42.5 ms                                                        | 42.8 ms: 1.01x slower                                                   |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 228 ms: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 422 us: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 317 us: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.5 ns: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.34 ms: 1.08x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.78 ms: 1.14x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 72.9 ms: 1.17x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.9 ms: 1.21x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 52.9 ms: 1.24x slower                                                   |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.63x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (3): async_tree_none_tg, sphinx, json_loads
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260831-3.16.0a0-b38e073/bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 96.80% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x