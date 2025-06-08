# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.034x faster
- HPT reliability: 94.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| float          | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                   |
| nbody          | 42.5 ms                                                        | 48.8 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 846 ms: 1.18x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.2 ms: 1.09x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 93.4 us: 1.07x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.7 ms: 1.06x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.38 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                   |
| mako            | 4.41 ms                                                        | 4.35 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                    |
| k_core                           | 1.46 sec                                                       | 986 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                    |
| go                               | 72.6 ms                                                        | 57.4 ms: 1.26x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.7 ms: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 846 ms: 1.18x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.57 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.2 ms: 1.09x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 910 us: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| unpickle_pure_python             | 99.5 us                                                        | 93.4 us: 1.07x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 33.7 ms: 1.06x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.38 ms: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.94 ms: 1.04x faster                                                   |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                   |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.5 us: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                   |
| float                            | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.02x faster                                                   |
| mako                             | 4.41 ms                                                        | 4.35 ms: 1.01x faster                                                   |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| python_startup                   | 8.63 ms                                                        | 8.54 ms: 1.01x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 938 ns: 1.01x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.8 ms: 1.01x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.82 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.48 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 24.6 ms: 1.00x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.12 ms: 1.03x slower                                                   |
| connected_components             | 208 ms                                                         | 215 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.2 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.2 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 499 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.32 us: 1.08x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.7 ms: 1.10x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.1 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.3 ms: 1.14x slower                                                   |
| nbody                            | 42.5 ms                                                        | 48.8 ms: 1.15x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.7 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.82 us: 1.15x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.09 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.43 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.98x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 195 ns: 4.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (2): gc_traversal, regex_compile
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 94.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x