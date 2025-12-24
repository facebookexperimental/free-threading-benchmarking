# Results vs. 3.13.0rc2

- fork: python
- ref: cc48bf0fde8025d60a57
- machine: darwin-arm64
- commit hash: cc48bf0
- commit date: 2025-12-23
- overall geometric mean: 1.013x faster
- HPT reliability: 60.34%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 425 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.8 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 965 ms: 1.04x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 106 us: 1.07x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.94 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.20 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 807 us: 2.53x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.08x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 511 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 606 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 238 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.34x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.2 ms: 1.23x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.96 ms: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 828 ns: 1.15x faster                                                     |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 965 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.03x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| sphinx                           | 409 ms                                                         | 425 ms: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 680 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.1 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.0 ns: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 106 us: 1.07x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.18 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.09x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 70.9 us: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                     |
| pylint                           | 106 ms                                                         | 120 ms: 1.13x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.6 ms: 1.13x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.94 ms: 1.15x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.0 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.15x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.7 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.18x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.11 ms: 1.19x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.16 us: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.20 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.4 ms: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.44 ms: 1.23x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.6 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.6 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.9 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 550 us: 1.34x slower                                                     |
| many_optionals                   | 200 us                                                         | 273 us: 1.36x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.8 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251223-3.15.0a3+-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3+-cc48bf0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 60.34% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x