# Results vs. 3.13.0rc2

- fork: python
- ref: a933e9ccee6d3c6753db
- machine: darwin-arm64
- commit hash: a933e9c
- commit date: 2026-03-28
- overall geometric mean: 1.036x faster
- HPT reliability: 78.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 967 ms: 1.08x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 235 ms: 2.22x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.3 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.1 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 58.0 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.05 ms: 1.18x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 850 ms: 1.18x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.9 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                    |
| mako            | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 769 us: 2.65x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 235 ms: 2.22x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 240 ms: 2.19x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 490 us: 2.03x faster                                                     |
| mdp                              | 1.06 sec                                                       | 597 ms: 1.77x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.99 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| go                               | 72.6 ms                                                        | 58.7 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.20x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 789 ns: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.1 ms: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.05 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 850 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| docutils                         | 1.05 sec                                                       | 967 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 450 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.96 ms: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 662 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.32 us: 1.04x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.55 us: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.6 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.95 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.2 ns: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.3 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.9 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.8 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.11x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 72.1 us: 1.11x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.7 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 59.8 ms: 1.14x slower                                                    |
| raytrace                         | 109 ms                                                         | 125 ms: 1.15x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 244 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.26 us: 1.21x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.0 ms: 1.22x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 52.4 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.4 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 256 us: 1.28x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 43.3 ms: 1.29x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.6 ms: 1.31x slower                                                    |
| nbody                            | 42.5 ms                                                        | 58.0 ms: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.1 ms: 3.15x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260328-3.15.0a7+-a933e9c-NOGIL/bm-20260328-macm4pro-arm64-python-a933e9ccee6d3c6753db-3.15.0a7+-a933e9c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 78.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x