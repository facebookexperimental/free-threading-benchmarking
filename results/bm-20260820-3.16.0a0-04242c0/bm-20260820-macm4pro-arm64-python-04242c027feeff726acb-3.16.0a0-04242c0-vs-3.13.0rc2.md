# Results vs. 3.13.0rc2

- fork: python
- ref: 04242c027feeff726acb
- machine: darwin-arm64
- commit hash: 04242c0
- commit date: 2026-08-20
- overall geometric mean: 1.044x faster
- HPT reliability: 98.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 964 ms: 1.09x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 318 ms: 1.65x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 343 ms: 1.52x faster                                                    |
| async_generators                 | 193 ms                                                         | 146 ms: 1.33x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 336 ms: 1.20x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 321 ms: 1.20x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 125 ms: 1.14x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.05x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 269 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 106 ms: 3.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|---------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| tomli_loads         | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 43.6 ms: 1.06x faster                                                   |
| json_loads          | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_process   | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| xml_etree_generate  | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| pickle_pure_python  | 130 us                                                         | 141 us: 1.08x slower                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 69.0 ms: 1.11x slower                                                   |
| Geometric mean      | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.10 ms: 1.05x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.67 ms: 1.06x slower                                                   |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 525 ms: 2.02x faster                                                    |
| pylint                           | 106 ms                                                         | 57.2 ms: 1.84x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 318 ms: 1.65x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 343 ms: 1.52x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.6 us: 1.47x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                   |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                   |
| async_generators                 | 193 ms                                                         | 146 ms: 1.33x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.2 ms: 1.30x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 49.7 us: 1.30x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 336 ms: 1.20x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 321 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                   |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 842 us: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 125 ms: 1.14x faster                                                    |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.11x faster                                                    |
| docutils                         | 1.05 sec                                                       | 964 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.1 ms: 1.06x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.06x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.6 ms: 1.06x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.4 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.96 ms: 1.04x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 42.1 ms: 1.04x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 923 ns: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 639 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.79 us: 1.00x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.56 ms: 1.00x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 423 us: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.1 ns: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.10 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.67 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 69.0 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 52.1 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 269 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 157 ms: 1.53x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 106 ms: 3.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (7): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, sphinx, nbody, unpickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260820-3.16.0a0-04242c0/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 98.83% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x