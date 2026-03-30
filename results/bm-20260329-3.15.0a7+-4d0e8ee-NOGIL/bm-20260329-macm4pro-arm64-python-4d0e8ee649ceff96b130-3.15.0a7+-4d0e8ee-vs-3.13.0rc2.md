# Results vs. 3.13.0rc2

- fork: python
- ref: 4d0e8ee649ceff96b130
- machine: darwin-arm64
- commit hash: 4d0e8ee
- commit date: 2026-03-29
- overall geometric mean: 1.028x faster
- HPT reliability: 62.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 235 ms: 2.21x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.6 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.68 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.9 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 780 us: 2.62x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 235 ms: 2.21x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 497 us: 2.00x faster                                                     |
| mdp                              | 1.06 sec                                                       | 596 ms: 1.77x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.04 ms: 1.55x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 58.9 ms: 1.23x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 786 ns: 1.21x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.0 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| docutils                         | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 453 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 663 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.99 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.4 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 40.8 ms: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.9 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.68 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.1 us: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.6 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.05 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.27 us: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.3 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 260 us: 1.30x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 44.1 ms: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.33x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 572 us: 1.39x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.6 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): coroutines, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260329-3.15.0a7+-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 62.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x