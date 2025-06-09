# Results vs. 3.13.0rc2

- fork: python
- ref: 2677dd017a033eaaad3b
- machine: darwin-arm64
- commit hash: 2677dd0
- commit date: 2025-06-08
- overall geometric mean: 1.025x faster
- HPT reliability: 50.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 983 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.2 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.9 ms: 1.13x faster                                                   |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 53.5 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.5 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.4 ms: 1.23x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 55.6 ms: 1.12x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 968 ms: 1.03x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.60 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.35 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.2 ms: 1.09x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                   |
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 485 us: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 555 ms: 1.90x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.8 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.4 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                    |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.20x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.9 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 821 ns: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.9 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 55.6 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| async_generators                 | 193 ms                                                         | 176 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 983 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.05x faster                                                   |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 968 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.60 ms: 1.01x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.83 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.22 ms: 1.05x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.01 ms: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 330 us: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.35 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.2 ms: 1.09x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 40.7 ms: 1.09x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.5 ms: 1.10x slower                                                   |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 72.5 us: 1.12x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.9 ms: 1.13x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 59.1 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.2 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.83 ms: 1.15x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.82 us: 1.15x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 184 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.16x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 375 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.1 ms: 1.17x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 765 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 41.9 ms: 1.25x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.80 us: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                    |
| nbody                            | 42.5 ms                                                        | 53.5 ms: 1.26x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.10 us: 1.27x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 598 us: 1.45x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 64.7 ms: 1.51x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.66 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 216 ns: 5.32x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (2): json, sphinx
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250608-3.15.0a0-2677dd0-NOGIL/bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 50.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x