# Results vs. 3.13.0rc2

- fork: python
- ref: a17c57eee5b5cc813907
- machine: darwin-arm64
- commit hash: a17c57e
- commit date: 2025-10-31
- overall geometric mean: 1.024x faster
- HPT reliability: 79.19%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 226 ms: 2.30x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 104 ms: 1.37x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 43.8 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 910 ms: 1.10x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 60.4 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 226 ms: 2.30x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.26x faster                                                     |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| k_core                           | 1.46 sec                                                       | 901 ms: 1.62x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 104 ms: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.31x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                     |
| go                               | 72.6 ms                                                        | 57.9 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 910 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 917 us: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.70 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.4 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.4 ms: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.0 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.87 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 416 us: 1.01x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.2 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 43.8 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                     |
| pycparser                        | 470 ms                                                         | 480 ms: 1.02x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.03x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.9 us: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.04x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 673 ms: 1.04x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 982 ns: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.8 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.5 ns: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.56 us: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.1 ms: 1.08x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.5 ms: 1.10x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 47.8 ms: 1.12x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.64 us: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| nbody                            | 42.5 ms                                                        | 49.8 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 370 us: 1.85x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.4 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (9): sphinx, dask, sympy_integrate, json, html5lib, shortest_path, async_tree_eager_cpu_io_mixed, connected_components, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251031-3.15.0a1+-a17c57e/bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1+-a17c57e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 79.19% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x