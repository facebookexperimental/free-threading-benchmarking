# Results vs. 3.13.0rc2

- fork: python
- ref: e167e06f8c6b24f7b54e
- machine: darwin-arm64
- commit hash: e167e06
- commit date: 2026-03-15
- overall geometric mean: 1.168x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 990 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.2 ms: 1.15x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 218 ms: 2.41x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 93.9 ms: 1.52x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.40x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.6 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 36.5 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.6 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.6 ms: 1.33x faster                                                    |
| nbody          | 42.5 ms                                                        | 40.2 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.5 ms: 1.18x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 636 ms: 1.57x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 85.4 us: 1.16x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 31.3 ms: 1.14x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 127 us: 1.03x faster                                                     |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.8 ms: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.16x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.03 ms: 1.10x faster                                                    |
| django_template | 12.5 ms                                                        | 13.7 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 218 ms: 2.41x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.46 ms: 2.33x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.2 ms: 2.21x faster                                                    |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 219 ms: 1.85x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.56 ms: 1.76x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                     |
| k_core                           | 1.46 sec                                                       | 858 ms: 1.70x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 38.5 ms: 1.66x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 10.00 us: 1.65x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 636 ms: 1.57x faster                                                     |
| go                               | 72.6 ms                                                        | 46.4 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 94.9 us: 1.53x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 93.9 ms: 1.52x faster                                                    |
| scimark_lu                       | 42.8 ms                                                        | 28.5 ms: 1.50x faster                                                    |
| pyflate                          | 222 ms                                                         | 151 ms: 1.47x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.40x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.6 ms: 1.39x faster                                                    |
| float                            | 31.4 ms                                                        | 23.6 ms: 1.33x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 998 ns: 1.30x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.3 ms: 1.28x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 509 ms: 1.28x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 253 ms: 1.27x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 97.3 ms: 1.27x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.17 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                     |
| fannkuch                         | 179 ms                                                         | 149 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.78 sec: 1.19x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 40.5 ms: 1.18x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 36.5 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.62 ms: 1.17x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.44 ms: 1.17x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 32.0 ms: 1.16x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 85.4 us: 1.16x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 5.87 us: 1.16x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 35.0 ns: 1.16x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 37.9 ms: 1.15x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.2 ms: 1.15x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 31.3 ms: 1.14x faster                                                    |
| mako                             | 4.41 ms                                                        | 4.03 ms: 1.10x faster                                                    |
| chaos                            | 24.3 ms                                                        | 22.2 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 910 us: 1.09x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                     |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 990 ms: 1.06x faster                                                     |
| nbody                            | 42.5 ms                                                        | 40.2 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 31.9 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.13 us: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| sphinx                           | 409 ms                                                         | 391 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 450 ms: 1.04x faster                                                     |
| meteor_contest                   | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.34 us: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pickle_pure_python               | 130 us                                                         | 127 us: 1.03x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.7 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| raytrace                         | 109 ms                                                         | 111 ms: 1.02x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 63.8 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.8 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                    |
| django_template                  | 12.5 ms                                                        | 13.7 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| many_optionals                   | 200 us                                                         | 237 us: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 45.0 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.6 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                             |

Benchmark hidden because not significant (2): sqlite_synth, thrift
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-e167e06-JIT/bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.168x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.21x