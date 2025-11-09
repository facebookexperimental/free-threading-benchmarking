# Results vs. 3.13.0rc2

- fork: python
- ref: 0ac890bea79d3e0162c8
- machine: darwin-arm64
- commit hash: 0ac890b
- commit date: 2025-11-08
- overall geometric mean: 1.075x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.02x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 221 ms: 1.75x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.7 ms: 1.46x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.7 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.17x faster                                                     |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.2 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.8 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.5 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 11.1 ms: 1.04x slower                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.72 ms: 1.07x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 775 ms: 1.29x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 89.1 us: 1.12x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 22.9 ms: 1.11x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.14 ms: 1.03x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.33 ms: 1.07x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.1 ms: 1.06x faster                                                    |
| mako            | 4.41 ms                                                        | 4.66 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| mdp                              | 1.06 sec                                                       | 519 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 221 ms: 1.75x faster                                                     |
| k_core                           | 1.46 sec                                                       | 893 ms: 1.64x faster                                                     |
| deepcopy                         | 145 us                                                         | 96.9 us: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.0 us: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 97.7 ms: 1.46x faster                                                    |
| go                               | 72.6 ms                                                        | 50.3 ms: 1.44x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 96.7 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 775 ms: 1.29x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| richards                         | 22.1 ms                                                        | 18.9 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.6 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 89.1 us: 1.12x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 22.9 ms: 1.11x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.57 ms: 1.11x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.5 ms: 1.10x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.2 ms: 1.10x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 923 us: 1.08x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.33 ms: 1.07x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.1 ms: 1.06x faster                                                    |
| thrift                           | 309 us                                                         | 294 us: 1.05x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.13 us: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.34 us: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 621 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 452 ms: 1.04x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.25 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 399 us: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.9 us: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| 2to3                             | 112 ms                                                         | 109 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 6.87 us: 1.01x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.3 ms: 1.01x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 162 ms: 1.02x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 96.9 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.6 ms: 1.02x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.9 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.14 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.03x slower                                                     |
| regex_v8                         | 10.7 ms                                                        | 11.1 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.2 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.66 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.72 ms: 1.07x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.2 ms: 1.09x slower                                                    |
| nbody                            | 42.5 ms                                                        | 46.8 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                     |
| many_optionals                   | 200 us                                                         | 344 us: 1.72x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.75x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.2 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (4): connected_components, dask, logging_silent, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251108-3.15.0a1+-0ac890b-CLANG/bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x