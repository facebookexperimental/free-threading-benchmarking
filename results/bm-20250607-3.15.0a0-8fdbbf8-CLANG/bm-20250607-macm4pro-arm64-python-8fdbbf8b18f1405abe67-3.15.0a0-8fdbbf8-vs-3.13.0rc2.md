# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 107 ms: 1.04x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.14x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 242 ms: 1.60x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 106 ms: 1.35x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.2 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.55 ms: 1.04x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 796 ms: 1.26x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 91.1 us: 1.09x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.33 ms: 1.07x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.47 ms: 1.02x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.08 ms: 1.02x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.1 ms: 1.12x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.01 ms: 1.11x faster                                                   |
| mako            | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.02x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.14x faster                                                    |
| mdp                              | 1.06 sec                                                       | 501 ms: 2.11x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 242 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.8 us: 1.48x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.48x faster                                                   |
| go                               | 72.6 ms                                                        | 50.3 ms: 1.44x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 106 ms: 1.35x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.9 ms: 1.26x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 796 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 16.8 ms: 1.18x faster                                                   |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.15x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.50 ms: 1.14x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.7 ms: 1.12x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.1 ms: 1.12x faster                                                   |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.1 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| regex_compile                    | 47.9 ms                                                        | 43.2 ms: 1.11x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.01 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 58.5 us: 1.10x faster                                                   |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.10x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 39.3 ms: 1.10x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 91.1 us: 1.09x faster                                                   |
| thrift                           | 309 us                                                         | 283 us: 1.09x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.4 ms: 1.09x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.33 ms: 1.07x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.7 ms: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 929 us: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.15 ms: 1.05x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                   |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                   |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.55 ms: 1.04x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| 2to3                             | 112 ms                                                         | 107 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                   |
| sympy_str                        | 95.5 ms                                                        | 93.1 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| sympy_expand                     | 159 ms                                                         | 156 ms: 1.02x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.47 ms: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.01x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 416 us: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 660 ms: 1.02x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.08 ms: 1.02x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                   |
| pylint                           | 106 ms                                                         | 109 ms: 1.03x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.01 us: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.53 us: 1.04x slower                                                   |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.8 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 48.8 ms: 1.12x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.2 ms: 1.14x slower                                                   |
| many_optionals                   | 200 us                                                         | 232 us: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.14 ms: 1.46x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.2 ms: 2.91x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 193 ns: 4.75x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (5): pycparser, json_loads, sqlite_synth, deltablue, sympy_sum
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x