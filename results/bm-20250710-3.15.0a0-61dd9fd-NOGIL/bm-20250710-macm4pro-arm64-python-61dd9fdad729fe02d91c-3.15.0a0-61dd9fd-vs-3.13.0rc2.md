# Results vs. 3.13.0rc2

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: darwin-arm64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.022x faster
- HPT reliability: 66.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| nbody          | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.9 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 977 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 784 us: 2.60x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 492 us: 2.02x faster                                                    |
| mdp                              | 1.06 sec                                                       | 572 ms: 1.85x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.7 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.1 ms: 1.24x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| go                               | 72.6 ms                                                        | 59.9 ms: 1.21x faster                                                   |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.2 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 977 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.9 ms: 1.03x slower                                                   |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.01 ms: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.00 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 343 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 697 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 332 us: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.08x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 44.1 ns: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.3 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.4 us: 1.13x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.59 us: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.95 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.17x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.99 us: 1.17x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.88 us: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.5 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.24 ms: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.8 ms: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 54.8 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 578 us: 1.40x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.84 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (6): pycparser, json_dumps, pathlib, sphinx, pidigits, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 66.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x