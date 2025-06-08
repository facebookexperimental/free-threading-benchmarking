# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.020x faster
- HPT reliability: 54.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 990 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 55.9 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 52.7 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 975 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.35 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.82 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 772 us: 2.64x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 487 us: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 562 ms: 1.88x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| deepcopy                         | 145 us                                                         | 120 us: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.2 ms: 1.19x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 990 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 975 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.89 ms: 1.05x slower                                                   |
| thrift                           | 309 us                                                         | 326 us: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.27 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.05 ms: 1.07x slower                                                   |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.35 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.7 ms: 1.10x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.11x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.12x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.5 ms: 1.14x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.82 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.9 ms: 1.16x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.95 us: 1.17x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 378 ms: 1.17x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 768 ms: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.8 ms: 1.18x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.19x slower                                                   |
| raytrace                         | 109 ms                                                         | 129 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.78 us: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.10 us: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.9 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 592 us: 1.44x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 64.6 ms: 1.51x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.67 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 215 ns: 5.29x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (6): json_dumps, pycparser, json, regex_dna, html5lib, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8-NOGIL/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 54.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x