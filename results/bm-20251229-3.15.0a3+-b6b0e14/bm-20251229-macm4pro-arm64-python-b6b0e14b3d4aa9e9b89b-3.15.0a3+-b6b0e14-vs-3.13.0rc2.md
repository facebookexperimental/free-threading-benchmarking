# Results vs. 3.13.0rc2

- fork: python
- ref: b6b0e14b3d4aa9e9b89b
- machine: darwin-arm64
- commit hash: b6b0e14
- commit date: 2025-12-29
- overall geometric mean: 1.070x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 238 ms: 1.62x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.3 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 45.4 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 932 ms: 1.07x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.8 us: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.73 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.61 ms: 1.04x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 548 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 238 ms: 1.62x faster                                                     |
| k_core                           | 1.46 sec                                                       | 907 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.06 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| deepcopy                         | 145 us                                                         | 102 us: 1.42x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| go                               | 72.6 ms                                                        | 53.7 ms: 1.35x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.0 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 932 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 939 us: 1.06x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.3 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.9 us: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.73 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 634 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 314 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.8 us: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.46 us: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.5 ms: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 973 ns: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.04 us: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.61 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.16 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.07x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.4 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.08x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.0 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (5): genshi_xml, logging_simple, logging_silent, pycparser, json_loads
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-macm4pro-arm64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x