# Results vs. 3.13.0rc2

- fork: python
- ref: 92972aea0f0e12dd21bf
- machine: darwin-arm64
- commit hash: 92972ae
- commit date: 2025-11-21
- overall geometric mean: 1.018x faster
- HPT reliability: 52.17%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 200 ms: 2.63x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.1 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.9 ms: 1.45x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.6 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.8 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 871 ms: 1.15x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.85 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.15 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.0 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| mako            | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 191 ms: 2.72x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 773 us: 2.64x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 200 ms: 2.63x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 479 us: 2.08x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 208 ms: 1.86x faster                                                     |
| mdp                              | 1.06 sec                                                       | 608 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 85.1 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.9 ms: 1.45x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                     |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.4 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 871 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.32 ms: 1.15x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 830 ns: 1.14x faster                                                     |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.7 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 684 ms: 1.05x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.1 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.2 ns: 1.06x slower                                                    |
| thrift                           | 309 us                                                         | 329 us: 1.06x slower                                                     |
| dask                             | 525 ms                                                         | 560 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.0 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.11 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.6 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.8 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.59 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.3 us: 1.10x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.85 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 43.0 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.08 us: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.15 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.1 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.6 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.3 ms: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.29 ms: 1.29x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.8 ms: 1.31x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.38x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 61.1 ms: 1.43x slower                                                    |
| many_optionals                   | 200 us                                                         | 378 us: 1.89x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.6 ms: 2.65x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.6 ms: 2.97x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251121-3.15.0a2+-92972ae-NOGIL/bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.018x faster

# HPT report

- Reliability score: 52.17% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x