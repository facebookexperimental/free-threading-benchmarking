# Results vs. 3.13.0rc2

- fork: python
- ref: c461aa99e2fabbaf5859
- machine: darwin-arm64
- commit hash: c461aa9
- commit date: 2026-01-15
- overall geometric mean: 1.072x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.2 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                     |
| nbody          | 42.5 ms                                                        | 45.7 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.86 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.5 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 854 ms: 1.17x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 96.2 us: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.20 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.61 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 910 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.06 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.5 us: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.45x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 854 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.5 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.86 ms: 1.09x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.5 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 621 ms: 1.05x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 61.8 us: 1.05x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 955 us: 1.04x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 96.2 us: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 304 us: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.5 ms: 1.00x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.1 ns: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.7 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 966 ns: 1.02x slower                                                     |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.04 us: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.06x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.20 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.7 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.61 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.2 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.2 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (4): pycparser, sympy_integrate, connected_components, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260115-3.15.0a5+-c461aa9/bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x