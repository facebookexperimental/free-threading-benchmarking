# Results vs. 3.13.0rc2

- fork: python
- ref: e5f68fd29b3bd867207f
- machine: darwin-arm64
- commit hash: e5f68fd
- commit date: 2025-04-10
- overall geometric mean: 1.037x faster
- HPT reliability: 50.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 84.7 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.2 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 228 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 237 ms: 1.24x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 221 ms: 1.06x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 53.0 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.2 ms: 1.27x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 56.0 ms: 1.11x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 950 ms: 1.05x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.04 ms: 1.08x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.46 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.52 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.9 ms: 1.10x slower                                                    |
| mako            | 4.41 ms                                                        | 5.39 ms: 1.22x slower                                                    |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.29x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 747 us: 2.73x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 442 us: 2.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 195 ms: 2.08x faster                                                     |
| mdp                              | 1.06 sec                                                       | 559 ms: 1.89x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 84.7 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| k_core                           | 1.46 sec                                                       | 977 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.2 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 228 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.2 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 237 ms: 1.24x faster                                                     |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 805 ns: 1.18x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.9 ms: 1.17x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.5 us: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 56.0 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| docutils                         | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 950 ms: 1.05x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.23 us: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.04x slower                                                     |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                     |
| connected_components             | 208 ms                                                         | 217 ms: 1.04x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.91 ms: 1.05x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.25 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 221 ms: 1.06x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.05 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.9 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.04 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.09x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 351 ms: 1.09x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.46 ms: 1.10x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.9 ms: 1.10x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.3 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.10x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 719 ms: 1.11x slower                                                     |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.2 ms: 1.11x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 48.7 ms: 1.11x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 138 ms: 1.11x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.5 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.3 us: 1.12x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.50 us: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 108 ms: 1.13x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.65 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.4 ms: 1.13x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 46.1 ns: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 59.8 ms: 1.14x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.9 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 185 ms: 1.16x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.09 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 40.0 ms: 1.19x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.20 us: 1.20x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.39 ms: 1.22x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.2 ms: 1.24x slower                                                    |
| nbody                            | 42.5 ms                                                        | 53.0 ms: 1.25x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.52 ms: 1.26x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.29x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.59 ms: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 570 us: 1.39x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250410-3.14.0a7+-e5f68fd-NOGIL/bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7+-e5f68fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 50.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x