# Results vs. 3.13.0rc2

- fork: python
- ref: 2be2dd5fc219a5c252d7
- machine: darwin-arm64
- commit hash: 2be2dd5
- commit date: 2026-02-21
- overall geometric mean: 1.009x faster
- HPT reliability: 68.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.2 ms: 1.00x slower                                                    |
| sphinx         | 409 ms                                                         | 428 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 154 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.0 ms: 1.03x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 854 ms: 1.17x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.42 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 829 us: 2.46x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 255 ms: 2.06x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 525 us: 1.89x faster                                                     |
| mdp                              | 1.06 sec                                                       | 610 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.14 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 59.5 ms: 1.22x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 154 ms: 1.20x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 795 ns: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 854 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                     |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.2 ms: 1.00x slower                                                    |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.0 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.03x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 671 ms: 1.03x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                    |
| sphinx                           | 409 ms                                                         | 428 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.7 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.4 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.21 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 337 us: 1.09x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.6 ms: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.68 us: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 46.1 ns: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.5 us: 1.14x slower                                                    |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 42.5 ms: 1.14x slower                                                    |
| shortest_path                    | 225 ms                                                         | 257 ms: 1.14x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.4 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.8 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.42 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 48.1 ms: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 58.2 ms: 1.36x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.4 ms: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 588 us: 1.43x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260221-3.15.0a6+-2be2dd5-NOGIL/bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 68.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x