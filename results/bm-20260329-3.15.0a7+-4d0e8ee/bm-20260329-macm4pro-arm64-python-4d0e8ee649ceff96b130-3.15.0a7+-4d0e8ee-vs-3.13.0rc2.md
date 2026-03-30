# Results vs. 3.13.0rc2

- fork: python
- ref: 4d0e8ee649ceff96b130
- machine: darwin-arm64
- commit hash: 4d0e8ee
- commit date: 2026-03-29
- overall geometric mean: 1.076x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.4 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 232 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.5 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.54 ms: 1.12x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.2 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 813 ms: 1.23x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 99.1 us: 1.00x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.64 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.33x faster                                                     |
| mdp                              | 1.06 sec                                                       | 530 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 232 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 896 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.8 us: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.2 ms: 1.27x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 813 ms: 1.23x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| float                            | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.54 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.3 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 114 ms: 1.08x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.4 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.1 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.9 ms: 1.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 952 us: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.2 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.64 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.3 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 637 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 935 ns: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 99.1 us: 1.00x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.5 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                    |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.81 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 44.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.13 us: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                     |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.5 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.42 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.5 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (2): regex_dna, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260329-3.15.0a7+-4d0e8ee/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x