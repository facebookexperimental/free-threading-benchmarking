# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.054x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 106 ms: 1.05x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| sphinx         | 409 ms                                                         | 395 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 245 ms: 1.65x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 106 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.59 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.2 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.6 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.2 ms: 1.06x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 103 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 818 ms: 1.22x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 93.4 us: 1.07x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.7 ms: 1.06x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.9 ms: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.03x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 4.89 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.56 ms: 1.01x faster                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 245 ms: 1.65x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                     |
| deepcopy                         | 145 us                                                         | 99.1 us: 1.46x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                    |
| go                               | 72.6 ms                                                        | 53.5 ms: 1.36x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 106 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 818 ms: 1.22x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 16.8 ms: 1.18x faster                                                    |
| async_generators                 | 193 ms                                                         | 164 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                     |
| generators                       | 15.7 ms                                                        | 13.9 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 881 us: 1.13x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.59 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.64 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 93.4 us: 1.07x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.2 ms: 1.06x faster                                                    |
| thrift                           | 309 us                                                         | 292 us: 1.06x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.7 ms: 1.06x faster                                                    |
| 2to3                             | 112 ms                                                         | 106 ms: 1.05x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 42.4 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.0 us: 1.04x faster                                                    |
| float                            | 31.4 ms                                                        | 30.2 ms: 1.04x faster                                                    |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 626 ms: 1.04x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 39.1 ns: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                     |
| sphinx                           | 409 ms                                                         | 395 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.34 ms: 1.03x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 931 ns: 1.02x faster                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 37.2 ms: 1.02x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.01 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.9 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.56 ms: 1.01x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 94.8 ms: 1.01x faster                                                    |
| sympy_expand                     | 159 ms                                                         | 159 ms: 1.01x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 124 ms: 1.01x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 52.8 ms: 1.01x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.7 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.03x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 45.3 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.04x slower                                                    |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.1 ms: 1.05x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.89 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.23 us: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.0 ms: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 103 ms: 1.08x slower                                                     |
| nbody                            | 42.5 ms                                                        | 46.6 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 227 us: 1.13x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.41 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.2 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (9): scimark_monte_carlo, sqlalchemy_imperative, dask, asyncio_websockets, pycparser, mdp, bench_thread_pool, telco, json
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.054x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.07x