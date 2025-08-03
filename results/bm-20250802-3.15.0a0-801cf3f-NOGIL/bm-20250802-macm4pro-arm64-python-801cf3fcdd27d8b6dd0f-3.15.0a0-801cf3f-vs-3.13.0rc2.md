# Results vs. 3.13.0rc2

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: darwin-arm64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.013x faster
- HPT reliability: 58.67%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.0 ms: 1.11x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 59.3 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.0 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 966 ms: 1.03x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.58 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.56 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                   |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.66x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 479 us: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 599 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 983 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                   |
| go                               | 72.6 ms                                                        | 60.0 ms: 1.21x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 813 ns: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.6 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 966 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.58 ms: 1.02x faster                                                   |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.23 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.99 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 345 ms: 1.07x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 701 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 333 us: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.0 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.3 ns: 1.09x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.56 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.0 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.3 us: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.4 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.0 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.26 us: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.56 ms: 1.26x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.4 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.28 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 58.0 ms: 1.36x slower                                                   |
| nbody                            | 42.5 ms                                                        | 59.3 ms: 1.39x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 597 us: 1.45x slower                                                    |
| many_optionals                   | 200 us                                                         | 330 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.1 ms: 2.89x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): sphinx, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250802-3.15.0a0-801cf3f-NOGIL/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 58.67% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x