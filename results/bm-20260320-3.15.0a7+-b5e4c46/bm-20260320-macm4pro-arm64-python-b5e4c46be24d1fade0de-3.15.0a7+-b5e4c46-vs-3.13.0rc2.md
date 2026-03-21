# Results vs. 3.13.0rc2

- fork: python
- ref: b5e4c46be24d1fade0de
- machine: darwin-arm64
- commit hash: b5e4c46
- commit date: 2026-03-20
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 399 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.5 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.7 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.0 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 826 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.9 us: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.66 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.3 ms: 1.00x faster                                                    |
| mako            | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.69x faster                                                     |
| k_core                           | 1.46 sec                                                       | 898 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.4 us: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| go                               | 72.6 ms                                                        | 53.2 ms: 1.36x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.5 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 826 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 922 us: 1.08x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.6 ms: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 41.8 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.66 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 399 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 641 ms: 1.01x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 36.8 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 64.0 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 40.3 ns: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.9 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.3 ms: 1.00x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.79 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.02x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.0 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.21 us: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.6 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.2 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.7 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.7 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (4): json_loads, sqlite_synth, pycparser, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260320-3.15.0a7+-b5e4c46/bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x