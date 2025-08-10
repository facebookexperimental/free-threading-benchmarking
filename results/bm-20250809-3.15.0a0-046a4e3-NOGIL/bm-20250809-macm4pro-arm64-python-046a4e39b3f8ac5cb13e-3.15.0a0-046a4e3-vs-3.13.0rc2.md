# Results vs. 3.13.0rc2

- fork: python
- ref: 046a4e39b3f8ac5cb13e
- machine: darwin-arm64
- commit hash: 046a4e3
- commit date: 2025-08-09
- overall geometric mean: 1.007x faster
- HPT reliability: 72.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 983 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                   |
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 770 us: 2.65x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 482 us: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 595 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.7 ms: 1.22x faster                                                   |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.95 ms: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| go                               | 72.6 ms                                                        | 62.1 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.6 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.7 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 983 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.5 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.28 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 348 ms: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.09x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 708 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                   |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.6 us: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.3 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.85 us: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.9 ms: 1.17x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.5 ms: 1.19x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.3 ms: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.34 us: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.27 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.9 ms: 1.34x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.5 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 584 us: 1.42x slower                                                    |
| many_optionals                   | 200 us                                                         | 330 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.2 ms: 2.91x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (2): deepcopy_reduce, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250809-3.15.0a0-046a4e3-NOGIL/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 72.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x