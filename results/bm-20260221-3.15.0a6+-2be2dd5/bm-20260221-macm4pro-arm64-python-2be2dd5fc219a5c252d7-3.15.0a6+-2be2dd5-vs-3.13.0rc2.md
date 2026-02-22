# Results vs. 3.13.0rc2

- fork: python
- ref: 2be2dd5fc219a5c252d7
- machine: darwin-arm64
- commit hash: 2be2dd5
- commit date: 2026-02-21
- overall geometric mean: 1.069x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.8 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.8 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                     |
| nbody          | 42.5 ms                                                        | 44.7 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 848 ms: 1.18x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.2 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.22 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.65 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.61 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.3 ms: 1.00x faster                                                    |
| mako            | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 545 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 908 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.06 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.5 us: 1.46x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| go                               | 72.6 ms                                                        | 52.7 ms: 1.38x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 98.8 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 848 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 189 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                    |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.5 ms: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.9 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.61 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 962 us: 1.03x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 46.4 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 639 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.2 us: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.3 ms: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.00x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.00x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.61 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.8 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.95 us: 1.02x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.8 ms: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.7 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.15 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.22 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.6 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.65 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.2 ms: 1.13x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.5 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 256 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.8 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (6): logging_silent, sqlite_synth, docutils, pycparser, connected_components, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260221-3.15.0a6+-2be2dd5/bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6+-2be2dd5.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.19x