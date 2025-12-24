# Results vs. 3.12.6

- fork: python
- ref: cc48bf0fde8025d60a57
- machine: darwin-arm64
- commit hash: cc48bf0
- commit date: 2025-12-23
- overall geometric mean: 1.093x faster
- HPT reliability: 98.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| sphinx         | 434 ms                                                   | 425 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.47x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| tomli_loads          | 957 ms                                                   | 965 ms: 1.01x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 106 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.94 ms: 1.24x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.20 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| mako            | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                                    |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.06x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 807 us: 2.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.83x faster                                                     |
| mdp                              | 1.09 sec                                                 | 606 ms: 1.80x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 511 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.48x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.47x faster                                                     |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.6 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.16 us: 1.21x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 59.2 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 828 ns: 1.17x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.6 ms: 1.10x faster                                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.0 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| sphinx                           | 434 ms                                                   | 425 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.7 ms: 1.00x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 965 ms: 1.01x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.18 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.6 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 680 ms: 1.02x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.02x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.1 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 106 us: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 336 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.6 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.6 ms: 1.08x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.15x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.0 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                     |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.94 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.20 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 550 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 273 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.4 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (2): typing_runtime_protocols, html5lib
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251223-3.15.0a3+-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 98.73% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x