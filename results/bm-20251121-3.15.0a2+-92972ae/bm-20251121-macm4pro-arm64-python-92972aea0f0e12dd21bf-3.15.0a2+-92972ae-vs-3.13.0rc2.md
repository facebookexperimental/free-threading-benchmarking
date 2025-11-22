# Results vs. 3.13.0rc2

- fork: python
- ref: 92972aea0f0e12dd21bf
- machine: darwin-arm64
- commit hash: 92972ae
- commit date: 2025-11-21
- overall geometric mean: 1.043x faster
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.32x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.30x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.5 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.4 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.3 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.1 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 851 ms: 1.17x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.6 ms: 1.14x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.1 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                    |
| mako            | 4.41 ms                                                        | 4.70 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.32x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.30x faster                                                     |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.45x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| deepcopy                         | 145 us                                                         | 103 us: 1.41x faster                                                     |
| go                               | 72.6 ms                                                        | 53.7 ms: 1.35x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 98.5 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.5 ms: 1.32x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.31x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 851 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.6 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 929 us: 1.07x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.1 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 42.3 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 637 ms: 1.02x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 47.1 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 463 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 98.1 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.26 us: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 965 ns: 1.02x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| dask                             | 525 ms                                                         | 542 ms: 1.03x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.0 ns: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 110 ms: 1.05x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.0 ms: 1.05x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.14 us: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.70 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 46.3 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                     |
| nbody                            | 42.5 ms                                                        | 46.3 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.4 ms: 1.11x slower                                                    |
| coverage                         | 31.2 ms                                                        | 35.5 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| many_optionals                   | 200 us                                                         | 362 us: 1.81x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.4 ms: 2.81x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.8 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (6): genshi_text, async_tree_eager_cpu_io_mixed, thrift, regex_dna, scimark_sparse_mat_mult, json
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251121-3.15.0a2+-92972ae/bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 99.79% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x