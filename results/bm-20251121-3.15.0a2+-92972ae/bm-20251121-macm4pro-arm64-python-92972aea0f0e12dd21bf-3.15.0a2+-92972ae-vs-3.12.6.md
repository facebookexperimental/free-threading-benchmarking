# Results vs. 3.12.6

- fork: python
- ref: 92972aea0f0e12dd21bf
- machine: darwin-arm64
- commit hash: 92972ae
- commit date: 2025-11-21
- overall geometric mean: 1.131x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.5 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.4 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.3 ms: 1.17x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| tomli_loads          | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.6 ms: 1.07x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.1 us: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.87 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.93 ms: 1.06x faster                                                    |
| mako            | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| mdp                              | 1.09 sec                                                 | 539 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.5 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 103 us: 1.57x faster                                                     |
| float                            | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.14 us: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.98 ms: 1.36x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| go                               | 70.0 ms                                                  | 53.7 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.3 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 48.5 ms: 1.26x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.3 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.8 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.0 ms: 1.16x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.1 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.26 us: 1.14x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.47 us: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 851 ms: 1.13x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.0 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.1 us: 1.11x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 46.3 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 463 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.6 ms: 1.07x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.93 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 312 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.1 us: 1.05x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 637 ms: 1.04x faster                                                     |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.6 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.70 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                    |
| dask                             | 528 ms                                                   | 542 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.3 ms: 1.05x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.87 ms: 1.11x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 929 us: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| coverage                         | 26.9 ms                                                  | 35.5 ms: 1.32x slower                                                    |
| many_optionals                   | 195 us                                                   | 362 us: 1.85x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.4 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (2): fannkuch, sqlite_synth
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251121-3.15.0a2+-92972ae/bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2+-92972ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.131x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.23x