# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.039x faster
- HPT reliability: 99.40%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 403 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 46.9 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 928 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.9 ms: 1.05x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.44 ms: 1.05x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 95.3 us: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.52 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.10 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| mako            | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 248 ms: 2.12x faster                                                    |
| mdp                              | 1.06 sec                                                       | 508 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 950 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                   |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                    |
| go                               | 72.6 ms                                                        | 55.1 ms: 1.32x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                   |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 916 us: 1.08x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 928 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.9 ms: 1.05x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.44 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.9 us: 1.04x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 95.3 us: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                   |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.30 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.6 ms: 1.03x faster                                                   |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.03x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.2 ms: 1.02x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                   |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 403 ms: 1.02x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.52 ms: 1.01x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.86 ms: 1.01x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 47.5 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.5 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                   |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 97.5 ms: 1.02x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.10 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.04x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.4 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.9 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.41 us: 1.09x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 351 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.0 ms: 1.10x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| nbody                            | 42.5 ms                                                        | 46.9 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.90 ms: 1.11x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.5 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.57 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.7 ms: 3.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 196 ns: 4.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (3): sqlite_synth, gc_traversal, genshi_xml
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 99.40% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x