# Results vs. 3.13.0rc2

- fork: python
- ref: af49df919dafc3767ae9
- machine: darwin-arm64
- commit hash: af49df9
- commit date: 2026-08-18
- overall geometric mean: 1.044x faster
- HPT reliability: 97.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 964 ms: 1.09x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 317 ms: 1.66x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| async_generators                 | 193 ms                                                         | 146 ms: 1.32x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 336 ms: 1.20x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 106 ms: 3.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| nbody          | 42.5 ms                                                        | 42.2 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.6 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.59 ms: 1.30x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.4 us: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 69.2 ms: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.18 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 526 ms: 2.01x faster                                                    |
| pylint                           | 106 ms                                                         | 57.2 ms: 1.85x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 317 ms: 1.66x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.4 us: 1.47x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 53.4 ms: 1.36x faster                                                   |
| async_generators                 | 193 ms                                                         | 146 ms: 1.32x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.7 us: 1.30x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.59 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.29x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 336 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 847 us: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.15x faster                                                    |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| docutils                         | 1.05 sec                                                       | 964 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.06x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.3 ms: 1.06x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.4 ms: 1.05x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.8 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.3 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.97 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 633 ms: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 926 ns: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.4 us: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                   |
| nbody                            | 42.5 ms                                                        | 42.2 ms: 1.01x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.78 us: 1.00x faster                                                   |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.56 ms: 1.00x slower                                                   |
| connected_components             | 208 ms                                                         | 209 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 422 us: 1.03x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.9 ns: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.9 ms: 1.05x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 497 ms: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.18 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 69.2 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.6 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 52.2 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 106 ms: 3.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, sphinx, logging_simple
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260818-3.16.0a0-af49df9/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 97.78% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x