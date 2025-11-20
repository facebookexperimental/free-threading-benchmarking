# Results vs. 3.12.6

- fork: python
- ref: ca1e86f9d963dc298d9a
- machine: darwin-arm64
- commit hash: ca1e86f
- commit date: 2025-11-19
- overall geometric mean: 1.128x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 226 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.8 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.2 ms: 1.17x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.9 ms: 1.17x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| tomli_loads          | 957 ms                                                   | 861 ms: 1.11x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.7 us: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.36 ms: 1.11x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.99 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.98 ms: 1.05x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                    |
| mako            | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.02x faster                                                     |
| mdp                              | 1.09 sec                                                 | 542 ms: 2.02x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 226 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 141 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 103 us: 1.57x faster                                                     |
| float                            | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.16 us: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| go                               | 70.0 ms                                                  | 54.1 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.28x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.6 ns: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 117 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.2 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 46.9 ms: 1.17x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.0 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.2 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.27 us: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.50 us: 1.12x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.8 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.9 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 861 ms: 1.11x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.5 us: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.88 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.80 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 467 ms: 1.07x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.7 us: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.98 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 642 ms: 1.03x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.9 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 320 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 175 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.81 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| dask                             | 528 ms                                                   | 542 ms: 1.03x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.9 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.36 ms: 1.11x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.99 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.12x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 941 us: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 363 us: 1.86x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.8 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251119-3.15.0a2+-ca1e86f/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.128x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.23x