# Results vs. 3.13.0rc2

- fork: python
- ref: ec7fad79d24e79961b86
- machine: darwin-arm64
- commit hash: ec7fad7
- commit date: 2025-07-23
- overall geometric mean: 1.011x faster
- HPT reliability: 72.49%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.3 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 49.5 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.65 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 950 ms: 1.05x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.5 ms: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 5.07 ms: 1.15x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 256 ms: 2.03x faster                                                    |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 251 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 960 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 113 us: 1.29x faster                                                    |
| go                               | 72.6 ms                                                        | 56.6 ms: 1.28x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.26x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.1 ms: 1.25x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.65 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.7 ms: 1.05x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 950 ms: 1.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 946 us: 1.05x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.3 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| float                            | 31.4 ms                                                        | 30.9 ms: 1.02x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.7 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.5 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.6 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.50 ms: 1.00x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.6 ms: 1.00x faster                                                   |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 953 ns: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.5 ms: 1.01x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.1 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 660 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.3 ns: 1.02x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.2 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.8 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.20 ms: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.6 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.57 us: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.07 ms: 1.15x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.5 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.5 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 324 us: 1.62x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.5 ms: 2.79x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): typing_runtime_protocols, pathlib, sphinx, thrift, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 72.49% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x