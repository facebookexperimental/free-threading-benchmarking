# Results vs. 3.13.0rc2

- fork: python
- ref: a1c630834649d54ffbca
- machine: darwin-arm64
- commit hash: a1c6308
- commit date: 2025-12-26
- overall geometric mean: 1.082x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.2 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.4 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.2 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 920 ms: 1.09x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.1 us: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.63 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.74 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 538 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| k_core                           | 1.46 sec                                                       | 899 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.04 ms: 1.55x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.43x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| go                               | 72.6 ms                                                        | 52.6 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.6 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.70 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.09x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.4 ms: 1.09x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 920 ms: 1.09x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 930 us: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.06x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 612 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.2 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 304 ms: 1.06x faster                                                     |
| sphinx                           | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.63 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.4 us: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.34 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.1 us: 1.02x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.2 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 964 ns: 1.02x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.05 us: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.4 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.74 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.8 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.2 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (3): shortest_path, logging_silent, regex_dna
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251226-3.15.0a3+-a1c6308/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3+-a1c6308.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x