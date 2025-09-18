# Results vs. 3.13.0rc2

- fork: python
- ref: b485e50fde3be08d796a
- machine: darwin-arm64
- commit hash: b485e50
- commit date: 2025-09-17
- overall geometric mean: 1.029x faster
- HPT reliability: 98.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.4 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.2 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 903 ms: 1.11x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.8 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| mako            | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 249 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 538 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 106 us: 1.36x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                   |
| go                               | 72.6 ms                                                        | 55.4 ms: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.28x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                   |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.75 ms: 1.11x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 903 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                   |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| connected_components             | 208 ms                                                         | 199 ms: 1.04x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.9 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.8 us: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.82 ms: 1.02x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.1 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.8 us: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.00x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.5 ms: 1.01x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 656 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 325 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 314 us: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.0 ms: 1.02x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.50 us: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.29 us: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.45 us: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.2 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.7 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.3 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.7 ms: 1.13x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 326 us: 1.63x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.0 ms: 2.88x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.4 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (4): json, logging_silent, regex_compile, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250917-3.15.0a0-b485e50/bm-20250917-macm4pro-arm64-python-b485e50fde3be08d796a-3.15.0a0-b485e50.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 98.67% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x