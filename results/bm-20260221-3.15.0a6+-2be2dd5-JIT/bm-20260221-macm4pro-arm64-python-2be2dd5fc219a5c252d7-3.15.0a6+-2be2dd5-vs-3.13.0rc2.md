# Results vs. 3.13.0rc2

- fork: python
- ref: 2be2dd5fc219a5c252d7
- machine: darwin-arm64
- commit hash: 2be2dd5
- commit date: 2026-02-21
- overall geometric mean: 1.155x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| html5lib       | 23.1 ms                                                        | 20.2 ms: 1.15x faster                                                    |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.36x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.2 ms: 1.45x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 37.3 ms: 1.16x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.8 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.4 ms: 1.34x faster                                                    |
| nbody          | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.8 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 656 ms: 1.52x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 86.3 us: 1.15x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 31.1 ms: 1.15x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 128 us: 1.02x faster                                                     |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.10 ms: 1.05x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.57 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.00 ms: 1.10x faster                                                    |
| django_template | 12.5 ms                                                        | 13.7 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.36x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.42 ms: 2.34x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 11.2 ms: 2.21x faster                                                    |
| mdp                              | 1.06 sec                                                       | 544 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.68 ms: 1.70x faster                                                    |
| k_core                           | 1.46 sec                                                       | 866 ms: 1.69x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 39.2 ms: 1.63x faster                                                    |
| go                               | 72.6 ms                                                        | 47.1 ms: 1.54x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 656 ms: 1.52x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 10.8 us: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 95.3 us: 1.52x faster                                                    |
| scimark_lu                       | 42.8 ms                                                        | 28.4 ms: 1.50x faster                                                    |
| pyflate                          | 222 ms                                                         | 151 ms: 1.47x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.2 ms: 1.45x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                    |
| float                            | 31.4 ms                                                        | 23.4 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.2 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 98.4 ms: 1.26x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.17 ms: 1.24x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 524 ms: 1.24x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 263 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.8 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.59 ms: 1.18x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 34.4 ns: 1.18x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.42 ms: 1.18x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 40.8 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| comprehensions                   | 6.80 us                                                        | 5.87 us: 1.16x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 37.3 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.84 sec: 1.15x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 86.3 us: 1.15x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 31.1 ms: 1.15x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.2 ms: 1.15x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 38.7 ms: 1.13x faster                                                    |
| chaos                            | 24.3 ms                                                        | 22.0 ms: 1.11x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 33.7 ms: 1.10x faster                                                    |
| mako                             | 4.41 ms                                                        | 4.00 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.81 ms: 1.09x faster                                                    |
| pycparser                        | 470 ms                                                         | 438 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.4 ms: 1.07x faster                                                    |
| nbody                            | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                    |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 32.1 ms: 1.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 949 us: 1.05x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.14 us: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.35 us: 1.04x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 46.1 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| pickle_pure_python               | 130 us                                                         | 128 us: 1.02x faster                                                     |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.4 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.10 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.4 ms: 1.07x slower                                                    |
| django_template                  | 12.5 ms                                                        | 13.7 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.57 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.3 ms: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.23x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.8 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmark hidden because not significant (3): dask, docutils, sqlite_synth
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260221-3.15.0a6+-2be2dd5-JIT/bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.155x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.22x