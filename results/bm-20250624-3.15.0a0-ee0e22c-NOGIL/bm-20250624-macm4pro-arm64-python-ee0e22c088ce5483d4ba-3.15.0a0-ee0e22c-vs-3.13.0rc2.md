# Results vs. 3.13.0rc2

- fork: python
- ref: ee0e22c088ce5483d4ba
- machine: darwin-arm64
- commit hash: ee0e22c
- commit date: 2025-06-24
- overall geometric mean: 1.020x faster
- HPT reliability: 69.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                  |
| sphinx         | 409 ms                                                         | 415 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 54.2 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 98.3 ms: 1.04x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.0 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| mako            | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 790 us: 2.58x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 494 us: 2.01x faster                                                    |
| mdp                              | 1.06 sec                                                       | 569 ms: 1.86x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.5 ms: 1.53x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 60.5 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.4 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 831 ns: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 965 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.57 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 415 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.3 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.19 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.05x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.00 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.01 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 343 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 330 us: 1.07x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 700 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.0 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                   |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.2 ms: 1.11x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.0 us: 1.13x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.1 ms: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.1 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.88 us: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.16x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.97 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.6 ms: 1.18x slower                                                   |
| raytrace                         | 109 ms                                                         | 130 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.20x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.81 us: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.4 ms: 1.26x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                   |
| nbody                            | 42.5 ms                                                        | 54.2 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.0 ms: 1.28x slower                                                   |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.14 us: 1.28x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 55.1 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 599 us: 1.45x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.76 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 219 ns: 5.40x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (2): pycparser, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 69.05% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x