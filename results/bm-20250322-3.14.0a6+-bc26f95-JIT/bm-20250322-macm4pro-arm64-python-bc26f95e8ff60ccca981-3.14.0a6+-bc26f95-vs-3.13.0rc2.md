# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.035x slower
- HPT reliability: 95.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                   |
| html5lib       | 23.1 ms                                                        | 24.4 ms: 1.06x slower                                                    |
| sphinx         | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 273 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 272 ms: 1.91x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 277 ms: 1.39x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 114 ms: 1.16x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| async_generators                 | 193 ms                                                         | 197 ms: 1.02x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.35x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.2 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| float          | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 881 ms: 1.13x faster                                                     |
| unpickle_pure_python | 99.5 us                                                        | 96.1 us: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 47.9 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.24 ms: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.18x slower                                                    |
| django_template | 12.5 ms                                                        | 17.3 ms: 1.38x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 273 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 272 ms: 1.91x faster                                                     |
| k_core                           | 1.46 sec                                                       | 974 ms: 1.50x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 274 ms: 1.48x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 277 ms: 1.39x faster                                                     |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 114 ms: 1.16x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 881 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| go                               | 72.6 ms                                                        | 68.1 ms: 1.07x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| pyflate                          | 222 ms                                                         | 211 ms: 1.05x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 23.6 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 623 ms: 1.04x faster                                                     |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 96.1 us: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.03x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.09 sec: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 63.0 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                     |
| fannkuch                         | 179 ms                                                         | 179 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                    |
| async_generators                 | 193 ms                                                         | 197 ms: 1.02x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 969 ns: 1.02x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 38.7 ms: 1.02x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.02x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 47.9 ms: 1.04x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.19 ms: 1.04x slower                                                    |
| float                            | 31.4 ms                                                        | 32.7 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.04x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.10 sec: 1.04x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                   |
| thrift                           | 309 us                                                         | 324 us: 1.05x slower                                                     |
| sphinx                           | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 46.8 ms: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.4 ms: 1.06x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.8 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 439 us: 1.07x slower                                                     |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.4 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.0 us: 1.10x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.50 ms: 1.10x slower                                                    |
| pycparser                        | 470 ms                                                         | 525 ms: 1.12x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.99 ms: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.44 ms: 1.12x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.24 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.7 ms: 1.13x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 181 ms: 1.14x slower                                                     |
| pylint                           | 106 ms                                                         | 121 ms: 1.15x slower                                                     |
| nbody                            | 42.5 ms                                                        | 49.3 ms: 1.16x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.88 us: 1.18x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.63 us: 1.18x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.6 ms: 1.18x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.36 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.11 us: 1.19x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.6 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 49.8 ns: 1.23x slower                                                    |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                     |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| chaos                            | 24.3 ms                                                        | 30.5 ms: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.1 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.35x slower                                                     |
| django_template                  | 12.5 ms                                                        | 17.3 ms: 1.38x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.14 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.2 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.035x slower

# HPT report

- Reliability score: 95.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x