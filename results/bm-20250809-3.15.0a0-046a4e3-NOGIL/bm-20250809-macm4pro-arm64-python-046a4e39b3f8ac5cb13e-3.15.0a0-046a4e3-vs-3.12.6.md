# Results vs. 3.12.6

- fork: python
- ref: 046a4e39b3f8ac5cb13e
- machine: darwin-arm64
- commit hash: 046a4e3
- commit date: 2025-08-09
- overall geometric mean: 1.085x faster
- HPT reliability: 97.01%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.2 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| tomli_loads          | 957 ms                                                   | 983 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 770 us: 2.61x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 595 ms: 1.83x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 482 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                   |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.34 us: 1.18x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.2 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.29 us: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| go                               | 70.0 ms                                                  | 62.1 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                  |
| scimark_sor                      | 61.0 ms                                                  | 55.6 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.95 ms: 1.08x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 476 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 142 ms: 1.00x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.09 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.85 us: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.5 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 983 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.6 us: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.05x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.2 ms: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 348 ms: 1.06x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 708 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.27 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.5 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.3 ms: 1.16x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.55 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.28 ms: 1.26x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 584 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 330 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (3): logging_simple, pidigits, xml_etree_process
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250809-3.15.0a0-046a4e3-NOGIL/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 97.01% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x