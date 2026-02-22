# Results vs. 3.12.6

- fork: python
- ref: 2be2dd5fc219a5c252d7
- machine: darwin-arm64
- commit hash: 2be2dd5
- commit date: 2026-02-21
- overall geometric mean: 1.088x faster
- HPT reliability: 98.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.08x slower                                                     |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 428 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 154 ms: 1.45x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| tomli_loads          | 957 ms                                                   | 854 ms: 1.12x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.42 ms: 1.30x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.29x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.14 ms: 5.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 829 us: 2.42x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                     |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 525 us: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 154 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 795 ns: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.24 us: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.5 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 854 ms: 1.12x faster                                                     |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 46.1 ns: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.06x faster                                                     |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                     |
| fannkuch                         | 176 ms                                                   | 168 ms: 1.05x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.4 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.5 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 428 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 530 ms: 1.00x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 671 ms: 1.01x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.6 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.21 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.5 us: 1.04x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                     |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 124 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.2 ms: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| shortest_path                    | 219 ms                                                   | 257 ms: 1.17x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 48.1 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 247 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.42 ms: 1.30x slower                                                    |
| many_optionals                   | 195 us                                                   | 272 us: 1.39x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 588 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.8 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): docutils
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260221-3.15.0a6+-2be2dd5-NOGIL/bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 98.93% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.38x