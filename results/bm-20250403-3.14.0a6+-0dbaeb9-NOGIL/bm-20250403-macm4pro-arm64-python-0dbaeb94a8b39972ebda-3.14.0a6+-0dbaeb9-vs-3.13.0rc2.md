# Results vs. 3.13.0rc2

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: darwin-arm64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.010x faster
- HPT reliability: 71.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                    |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 209 ms: 2.52x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 214 ms: 1.81x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 88.2 ms: 1.50x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 51.4 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.5 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.5 ms: 1.26x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 978 ms: 1.02x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.40 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.49 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                    |
| mako            | 4.41 ms                                                        | 5.67 ms: 1.28x slower                                                    |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 745 us: 2.74x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 198 ms: 2.63x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 209 ms: 2.52x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 448 us: 2.22x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                     |
| mdp                              | 1.06 sec                                                       | 569 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 214 ms: 1.81x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 88.2 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 978 ms: 1.50x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.30x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.5 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| deepcopy                         | 145 us                                                         | 124 us: 1.17x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 814 ns: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 56.0 ms: 1.14x faster                                                    |
| go                               | 72.6 ms                                                        | 63.6 ms: 1.14x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.8 us: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.3 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.5 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 978 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                     |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                    |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.06x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.27 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 222 ms: 1.07x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.40 ms: 1.09x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                     |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.3 us: 1.12x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 49.7 ms: 1.12x slower                                                    |
| fannkuch                         | 179 ms                                                         | 201 ms: 1.12x slower                                                     |
| richards                         | 22.1 ms                                                        | 24.9 ms: 1.13x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 365 ms: 1.14x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 42.4 ms: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.14x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 28.2 ms: 1.14x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 745 ms: 1.15x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.74 ms: 1.15x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.3 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.2 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.59 us: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.0 ms: 1.17x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.86 us: 1.17x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 47.6 ns: 1.17x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 147 ms: 1.19x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 51.4 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 40.9 ms: 1.22x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                    |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                     |
| coverage                         | 31.2 ms                                                        | 38.8 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.49 ms: 1.26x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.24 ms: 1.26x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.65 us: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.67 ms: 1.28x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.2 ms: 1.29x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.92 ms: 1.42x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 588 us: 1.43x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.7 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (2): deepcopy_reduce, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 71.62% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x