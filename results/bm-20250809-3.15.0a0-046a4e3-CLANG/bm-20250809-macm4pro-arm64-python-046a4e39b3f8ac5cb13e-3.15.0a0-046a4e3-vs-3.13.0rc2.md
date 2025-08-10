# Results vs. 3.13.0rc2

- fork: python
- ref: 046a4e39b3f8ac5cb13e
- machine: darwin-arm64
- commit hash: 046a4e3
- commit date: 2025-08-09
- overall geometric mean: 1.060x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                    |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.13x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.9 ms: 1.11x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.4 ms: 2.92x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 43.7 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.7 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 92.0 us: 1.08x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.55 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.14 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.7 ms: 1.09x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.31 ms: 1.07x faster                                                   |
| mako            | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                   |
| django_template | 12.5 ms                                                        | 14.2 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 238 ms: 2.20x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 244 ms: 2.13x faster                                                    |
| mdp                              | 1.06 sec                                                       | 516 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 243 ms: 1.67x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                    |
| k_core                           | 1.46 sec                                                       | 952 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.2 us: 1.46x faster                                                   |
| go                               | 72.6 ms                                                        | 50.6 ms: 1.43x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.5 ms: 1.27x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 804 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                   |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.15x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.3 ms: 1.15x faster                                                   |
| richards                         | 22.1 ms                                                        | 19.2 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                   |
| async_generators                 | 193 ms                                                         | 172 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 38.9 ms: 1.11x faster                                                   |
| generators                       | 15.7 ms                                                        | 14.2 ms: 1.11x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| regex_compile                    | 47.9 ms                                                        | 43.7 ms: 1.10x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.9 ms: 1.09x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 19.7 ms: 1.09x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 92.0 us: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.1 ms: 1.08x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.31 ms: 1.07x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 38.0 ns: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 60.9 us: 1.06x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                   |
| thrift                           | 309 us                                                         | 292 us: 1.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 942 us: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 619 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.27 ms: 1.04x faster                                                   |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 203 ms: 1.03x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                  |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.20 us: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.55 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 419 us: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.7 ms: 1.03x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.14 ms: 1.03x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.02 us: 1.03x slower                                                   |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.7 ms: 1.05x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.2 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.3 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.2 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.5 ms: 1.15x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 307 us: 1.53x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 16.8 ms: 2.68x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.4 ms: 2.92x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (6): sqlite_synth, telco, sympy_expand, sympy_str, meteor_contest, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250809-3.15.0a0-046a4e3-CLANG/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x