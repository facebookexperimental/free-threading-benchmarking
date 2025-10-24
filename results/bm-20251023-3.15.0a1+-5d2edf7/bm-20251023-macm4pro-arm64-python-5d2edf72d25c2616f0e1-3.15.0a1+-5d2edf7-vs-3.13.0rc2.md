# Results vs. 3.13.0rc2

- fork: python
- ref: 5d2edf72d25c2616f0e1
- machine: darwin-arm64
- commit hash: 5d2edf7
- commit date: 2025-10-23
- overall geometric mean: 1.018x faster
- HPT reliability: 76.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 229 ms: 2.27x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 232 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.65x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.4 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.6 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 50.8 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 956 ms: 1.05x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.76 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.22 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| mako            | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 229 ms: 2.27x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 232 ms: 2.26x faster                                                     |
| mdp                              | 1.06 sec                                                       | 544 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.65x faster                                                     |
| k_core                           | 1.46 sec                                                       | 909 ms: 1.61x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                     |
| go                               | 72.6 ms                                                        | 57.4 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 52.7 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.3 ms: 1.17x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 913 us: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 956 ms: 1.05x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.94 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.05 sec: 1.04x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| float                            | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.4 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| richards                         | 22.1 ms                                                        | 22.0 ms: 1.00x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.9 ms: 1.00x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 24.8 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.4 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.3 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.2 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.76 ms: 1.02x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 418 us: 1.02x slower                                                     |
| coverage                         | 31.2 ms                                                        | 31.7 ms: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.0 us: 1.02x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.91 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 971 ns: 1.02x slower                                                     |
| thrift                           | 309 us                                                         | 317 us: 1.03x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.8 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.03x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.22 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.3 ns: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.2 ms: 1.08x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.08x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.1 ms: 1.09x slower                                                    |
| fannkuch                         | 179 ms                                                         | 195 ms: 1.09x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.4 ms: 1.10x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 176 ms: 1.10x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.61 us: 1.12x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 50.0 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| nbody                            | 42.5 ms                                                        | 50.8 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.23x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 366 us: 1.82x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.9 ms: 2.85x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.6 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): sphinx, gc_traversal
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251023-3.15.0a1+-5d2edf7/bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1+-5d2edf7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.018x faster

# HPT report

- Reliability score: 76.08% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x