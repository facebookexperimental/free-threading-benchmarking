# Results vs. 3.13.0rc2

- fork: python
- ref: 797c2c33e181badc053f
- machine: darwin-arm64
- commit hash: 797c2c3
- commit date: 2025-08-12
- overall geometric mean: 1.011x faster
- HPT reliability: 55.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.2 ms: 3.05x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.65 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 957 ms: 1.04x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.3 ms: 1.00x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.85 ms: 1.03x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.12x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 250 ms: 1.62x faster                                                    |
| k_core                           | 1.46 sec                                                       | 960 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 256 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.30x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                   |
| go                               | 72.6 ms                                                        | 56.7 ms: 1.28x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.12x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.65 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 957 ms: 1.04x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.3 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 968 us: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.3 ms: 1.02x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.3 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                   |
| float                            | 31.4 ms                                                        | 31.0 ms: 1.01x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.9 us: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.3 ms: 1.00x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 953 ns: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.60 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 170 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.85 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 671 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.1 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 501 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.41 us: 1.08x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.08x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 57.2 ms: 1.09x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.61 us: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.0 ms: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 323 us: 1.61x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.4 ms: 2.78x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.2 ms: 3.05x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): async_tree_eager_cpu_io_mixed, telco, json, thrift, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250812-3.15.0a0-797c2c3/bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 55.02% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x