# Results vs. 3.13.0rc2

- fork: python
- ref: 6d5a8c2ec19f1c38b455
- machine: darwin-arm64
- commit hash: 6d5a8c2
- commit date: 2025-05-09
- overall geometric mean: 1.006x faster
- HPT reliability: 70.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 25.7 ms: 1.11x slower                                                   |
| sphinx         | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.8 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.16x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.4 ms: 1.09x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 986 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.8 ms: 1.09x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.24 ms: 1.13x slower                                                   |
| json_loads           | 10.8 us                                                        | 12.5 us: 1.16x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.36 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.82 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 771 us: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 483 us: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| mdp                              | 1.06 sec                                                       | 583 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.8 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.8 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                   |
| deepcopy                         | 145 us                                                         | 125 us: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 816 ns: 1.16x faster                                                    |
| go                               | 72.6 ms                                                        | 62.5 ms: 1.16x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.4 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                   |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 986 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| sphinx                           | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                    |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.00 ms: 1.06x slower                                                   |
| json                             | 1.94 ms                                                        | 2.07 ms: 1.07x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.32 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.36 ms: 1.08x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.8 ms: 1.09x slower                                                   |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 719 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 25.7 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.7 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.24 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.82 ms: 1.15x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.5 us: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 75.3 us: 1.17x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 146 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.3 ms: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.25 ms: 1.26x slower                                                   |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.85 us: 1.27x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.15 us: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.2 ms: 1.29x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.79 us: 1.29x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 600 us: 1.46x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.63 ms: 1.54x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 66.8 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 214 ns: 5.27x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (3): deepcopy_reduce, pathlib, pycparser
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-6d5a8c2-NOGIL/bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 70.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x