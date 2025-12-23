# Results vs. 3.13.0rc2

- fork: python
- ref: 5b5ee3c4bf1a28b61063
- machine: darwin-arm64
- commit hash: 5b5ee3c
- commit date: 2025-12-23
- overall geometric mean: 1.070x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.3 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.5 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 960 ms: 1.04x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 99.8 us: 1.00x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.5 ms: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.88 ms: 1.01x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.5 ms: 1.00x slower                                                    |
| mako            | 4.41 ms                                                        | 4.74 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 546 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 904 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.53x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| deepcopy                         | 145 us                                                         | 103 us: 1.41x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| go                               | 72.6 ms                                                        | 53.5 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.3 ms: 1.33x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 48.5 ms: 1.32x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 930 us: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.05x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 960 ms: 1.04x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.03x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.5 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 634 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.0 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.88 ms: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 99.8 us: 1.00x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.5 ms: 1.00x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.25 us: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.5 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 967 ns: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.2 ns: 1.04x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.9 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.25 us: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.74 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.3 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (4): sympy_integrate, json_loads, thrift, pycparser
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251223-3.15.0a3+-5b5ee3c/bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x