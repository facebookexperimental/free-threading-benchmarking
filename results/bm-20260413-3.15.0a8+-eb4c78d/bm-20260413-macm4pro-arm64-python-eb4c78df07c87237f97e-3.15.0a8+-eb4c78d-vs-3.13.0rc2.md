# Results vs. 3.13.0rc2

- fork: python
- ref: eb4c78df07c87237f97e
- machine: darwin-arm64
- commit hash: eb4c78d
- commit date: 2026-04-13
- overall geometric mean: 1.067x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 399 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.77x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 820 ms: 1.22x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.9 us: 1.02x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.3 ms: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.3 ms: 1.05x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.74 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.3 ms: 1.00x faster                                                    |
| mako            | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 534 ms: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.77x faster                                                     |
| k_core                           | 1.46 sec                                                       | 897 ms: 1.63x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.4 us: 1.46x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 53.0 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 820 ms: 1.22x faster                                                     |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.19x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.6 ms: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.3 ms: 1.06x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.3 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.04x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.1 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 966 us: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 399 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.74 ms: 1.02x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.4 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 97.9 us: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.3 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 642 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.3 ms: 1.00x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.1 ns: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.81 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.10 us: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.6 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.3 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.4 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.89 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.0 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.52 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.8 ms: 1.24x slower                                                    |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (3): logging_format, json_loads, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260413-3.15.0a8+-eb4c78d/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.067x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.20x