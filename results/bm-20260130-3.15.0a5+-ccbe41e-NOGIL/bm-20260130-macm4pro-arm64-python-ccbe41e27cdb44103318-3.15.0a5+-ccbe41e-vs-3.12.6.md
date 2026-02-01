# Results vs. 3.12.6

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.116x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 239 ms: 1.87x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.4 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| nbody          | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.4 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 8.97 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| tomli_loads          | 957 ms                                                   | 866 ms: 1.11x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 106 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.42 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.07x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.08 ms: 5.09x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 766 us: 2.62x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 242 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 239 ms: 1.87x faster                                                     |
| mdp                              | 1.09 sec                                                 | 598 ms: 1.83x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 496 us: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.49x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.11 us: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 810 ns: 1.19x faster                                                     |
| go                               | 70.0 ms                                                  | 58.8 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.8 ns: 1.16x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.2 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 866 ms: 1.11x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 451 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.58 ms: 1.10x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.4 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.0 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.38 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.62 us: 1.07x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 8.97 ms: 1.07x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.6 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| docutils                         | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.9 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.90 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 70.5 us: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 329 ms: 1.00x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.9 ms: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.6 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 673 ms: 1.01x slower                                                     |
| thrift                           | 322 us                                                   | 326 us: 1.01x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.10 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 106 us: 1.02x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 59.5 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.03x slower                                                     |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| nbody                            | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.8 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 183 ms: 1.10x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 57.3 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.0 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.42 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 562 us: 1.34x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.4 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.4 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (3): richards, scimark_monte_carlo, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260130-3.15.0a5+-ccbe41e-NOGIL/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.36x