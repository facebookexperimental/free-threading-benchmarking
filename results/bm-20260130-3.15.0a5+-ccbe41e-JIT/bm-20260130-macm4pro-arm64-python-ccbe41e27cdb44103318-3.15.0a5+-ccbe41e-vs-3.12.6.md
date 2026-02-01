# Results vs. 3.12.6

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.269x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| docutils       | 1.02 sec                                                 | 973 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 18.9 ms: 1.22x faster                                                    |
| sphinx         | 434 ms                                                   | 377 ms: 1.15x faster                                                     |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 214 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 218 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 96.6 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 93.8 ms: 1.83x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.32x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.0 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 22.3 ms: 1.70x faster                                                    |
| nbody          | 54.2 ms                                                  | 39.5 ms: 1.37x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.2 ms: 1.36x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.39 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 664 ms: 1.44x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 72.9 us: 1.41x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 36.9 ms: 1.40x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 111 us: 1.26x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 31.0 ms: 1.25x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 21.7 ms: 1.23x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.04x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 8.80 ms: 1.19x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| django_template | 13.6 ms                                                  | 13.8 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.88 ms: 5.35x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.21 ms: 2.43x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 11.0 ms: 2.32x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 214 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 218 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| mdp                              | 1.09 sec                                                 | 590 ms: 1.85x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 96.6 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 93.8 ms: 1.83x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 28.0 ms: 1.83x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 10.3 us: 1.78x faster                                                    |
| deepcopy                         | 161 us                                                   | 91.4 us: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                     |
| float                            | 37.9 ms                                                  | 22.3 ms: 1.70x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 38.4 ms: 1.59x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.21 us: 1.58x faster                                                    |
| go                               | 70.0 ms                                                  | 45.4 ms: 1.54x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.12 ms: 1.54x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 967 ns: 1.51x faster                                                     |
| pyflate                          | 216 ms                                                   | 146 ms: 1.48x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 34.7 ns: 1.47x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 664 ms: 1.44x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 98.4 ms: 1.44x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.8 ms: 1.41x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 72.9 us: 1.41x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.9 ms: 1.40x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 39.2 ms: 1.39x faster                                                    |
| raytrace                         | 145 ms                                                   | 105 ms: 1.39x faster                                                     |
| nbody                            | 54.2 ms                                                  | 39.5 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 40.2 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| chaos                            | 28.9 ms                                                  | 21.8 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.32x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 507 ms: 1.31x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 252 ms: 1.30x faster                                                     |
| k_core                           | 1.12 sec                                                 | 859 ms: 1.30x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 111 us: 1.26x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 31.0 ms: 1.25x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 34.9 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.07 us: 1.24x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 31.4 ms: 1.24x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.26 us: 1.24x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 37.0 ms: 1.23x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 21.7 ms: 1.23x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.82 sec: 1.23x faster                                                   |
| mako                             | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 18.9 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 8.80 ms: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                    |
| fannkuch                         | 176 ms                                                   | 150 ms: 1.17x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 60.9 us: 1.17x faster                                                    |
| pycparser                        | 497 ms                                                   | 428 ms: 1.16x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| sphinx                           | 434 ms                                                   | 377 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.70 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 92.3 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 299 us: 1.08x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 44.5 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.48 ms: 1.07x faster                                                    |
| json                             | 1.93 ms                                                  | 1.81 ms: 1.07x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.07x faster                                                     |
| docutils                         | 1.02 sec                                                 | 973 ms: 1.05x faster                                                     |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                    |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| connected_components             | 201 ms                                                   | 196 ms: 1.02x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.39 ms: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| django_template                  | 13.6 ms                                                  | 13.8 ms: 1.01x slower                                                    |
| sympy_str                        | 104 ms                                                   | 106 ms: 1.01x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 884 us: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.6 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260130-3.15.0a5+-ccbe41e-JIT/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.269x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.26x