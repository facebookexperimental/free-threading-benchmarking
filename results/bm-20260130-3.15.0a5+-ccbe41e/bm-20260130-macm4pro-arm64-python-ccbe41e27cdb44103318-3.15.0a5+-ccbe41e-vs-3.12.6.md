# Results vs. 3.12.6

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.180x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 991 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 434 ms                                                   | 382 ms: 1.13x faster                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.8 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.20x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.3 ms: 1.23x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.45 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| tomli_loads          | 957 ms                                                   | 816 ms: 1.17x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 95.4 us: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.02x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                    |
| mako            | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.94 ms: 5.28x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                     |
| mdp                              | 1.09 sec                                                 | 538 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 95.8 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.2 us: 1.68x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.03 us: 1.40x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| go                               | 70.0 ms                                                  | 51.6 ms: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 27.9 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 48.3 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 896 ms: 1.25x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 44.3 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.21x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.38 us: 1.18x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.9 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 816 ms: 1.17x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 21.9 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                    |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.6 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.3 us: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| sphinx                           | 434 ms                                                   | 382 ms: 1.13x faster                                                     |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.13x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.9 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.28 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 452 ms: 1.10x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 302 ms: 1.08x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 95.4 us: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 616 ms: 1.08x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.8 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                                     |
| sympy_str                        | 104 ms                                                   | 98.8 ms: 1.05x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.04x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 991 ms: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 944 ns: 1.02x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.45 ms: 1.02x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.98 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 879 us: 1.06x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.2 ms: 1.16x slower                                                    |
| many_optionals                   | 195 us                                                   | 244 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                             |

Benchmark hidden because not significant (1): sympy_expand
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260130-3.15.0a5+-ccbe41e/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.180x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.23x