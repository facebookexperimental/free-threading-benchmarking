# Results vs. 3.13.0rc2

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.019x faster
- HPT reliability: 73.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.4 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 55.0 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 969 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.80 ms: 1.14x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.08 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 192 ms: 2.71x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 201 ms: 2.61x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 799 us: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 495 us: 2.01x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.87x faster                                                    |
| mdp                              | 1.06 sec                                                       | 574 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.4 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| async_tree_none                  | 142 ms                                                         | 99.0 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| go                               | 72.6 ms                                                        | 60.3 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 816 ns: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 969 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.8 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                   |
| json                             | 1.94 ms                                                        | 2.03 ms: 1.04x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.02 ms: 1.06x slower                                                   |
| thrift                           | 309 us                                                         | 328 us: 1.06x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 342 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.04 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 698 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.09x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.1 ns: 1.11x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.8 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.3 us: 1.13x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.80 ms: 1.14x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.9 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.93 us: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.88 us: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.08 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.65 ms: 1.28x slower                                                   |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.0 ms: 1.29x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.2 ms: 1.31x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 593 us: 1.44x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.88 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (5): pathlib, pycparser, async_tree_eager_cpu_io_mixed, json_dumps, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f-NOGIL/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 73.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x