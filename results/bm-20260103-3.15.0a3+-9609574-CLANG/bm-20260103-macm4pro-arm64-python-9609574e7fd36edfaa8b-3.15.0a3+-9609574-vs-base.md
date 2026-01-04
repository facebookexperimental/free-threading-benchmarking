# Results vs. base

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.007x faster
- HPT reliability: 99.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                                                                              | 112 ms: 1.01x faster                                                                                                      |
| html5lib       | 21.6 ms                                                                                                             | 21.2 ms: 1.02x faster                                                                                                     |
| Geometric mean | (ref)                                                                                                               | 1.01x faster                                                                                                              |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| async_tree_eager                 | 40.7 ms                                                                                                             | 39.7 ms: 1.03x faster                                                                                                     |
| async_tree_eager_io              | 228 ms                                                                                                              | 223 ms: 1.02x faster                                                                                                      |
| async_tree_none                  | 102 ms                                                                                                              | 100 ms: 1.02x faster                                                                                                      |
| async_tree_eager_memoization     | 106 ms                                                                                                              | 105 ms: 1.01x faster                                                                                                      |
| async_tree_eager_tg              | 79.8 ms                                                                                                             | 80.3 ms: 1.01x slower                                                                                                     |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                                                              | 243 ms: 1.01x slower                                                                                                      |
| coroutines                       | 10.1 ms                                                                                                             | 10.4 ms: 1.03x slower                                                                                                     |
| Geometric mean                   | (ref)                                                                                                               | 1.01x faster                                                                                                              |

Benchmark hidden because not significant (11): async_tree_memoization, async_tree_eager_io_tg, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_generators, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 162 ms                                                                                                              | 163 ms: 1.01x slower                                                                                                      |
| nbody          | 45.7 ms                                                                                                             | 46.1 ms: 1.01x slower                                                                                                     |
| float          | 27.1 ms                                                                                                             | 28.1 ms: 1.04x slower                                                                                                     |
| Geometric mean | (ref)                                                                                                               | 1.02x slower                                                                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 45.1 ms                                                                                                             | 43.5 ms: 1.04x faster                                                                                                     |
| regex_dna      | 97.6 ms                                                                                                             | 98.2 ms: 1.01x slower                                                                                                     |
| regex_v8       | 9.72 ms                                                                                                             | 10.0 ms: 1.03x slower                                                                                                     |
| Geometric mean | (ref)                                                                                                               | 1.00x slower                                                                                                              |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|----------------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| xml_etree_generate   | 34.5 ms                                                                                                             | 32.6 ms: 1.06x faster                                                                                                     |
| xml_etree_iterparse  | 40.0 ms                                                                                                             | 38.0 ms: 1.05x faster                                                                                                     |
| xml_etree_parse      | 63.2 ms                                                                                                             | 60.2 ms: 1.05x faster                                                                                                     |
| xml_etree_process    | 24.5 ms                                                                                                             | 23.6 ms: 1.04x faster                                                                                                     |
| tomli_loads          | 915 ms                                                                                                              | 878 ms: 1.04x faster                                                                                                      |
| unpickle_pure_python | 96.8 us                                                                                                             | 93.5 us: 1.04x faster                                                                                                     |
| json_dumps           | 3.89 ms                                                                                                             | 3.78 ms: 1.03x faster                                                                                                     |
| unpickle_list        | 2.10 us                                                                                                             | 2.06 us: 1.02x faster                                                                                                     |
| pickle_pure_python   | 139 us                                                                                                              | 137 us: 1.01x faster                                                                                                      |
| json_loads           | 10.7 us                                                                                                             | 10.6 us: 1.01x faster                                                                                                     |
| pickle_dict          | 12.9 us                                                                                                             | 12.9 us: 1.00x faster                                                                                                     |
| pickle_list          | 2.12 us                                                                                                             | 2.13 us: 1.01x slower                                                                                                     |
| pickle               | 5.96 us                                                                                                             | 6.05 us: 1.01x slower                                                                                                     |
| unpickle             | 6.25 us                                                                                                             | 6.38 us: 1.02x slower                                                                                                     |
| Geometric mean       | (ref)                                                                                                               | 1.02x faster                                                                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.24 ms                                                                                                             | 6.29 ms: 1.01x slower                                                                                                     |
| python_startup         | 8.67 ms                                                                                                             | 8.75 ms: 1.01x slower                                                                                                     |
| Geometric mean         | (ref)                                                                                                               | 1.01x slower                                                                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|-----------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 21.1 ms                                                                                                             | 19.8 ms: 1.06x faster                                                                                                     |
| django_template | 14.7 ms                                                                                                             | 14.0 ms: 1.05x faster                                                                                                     |
| genshi_text     | 9.68 ms                                                                                                             | 9.23 ms: 1.05x faster                                                                                                     |
| mako            | 4.65 ms                                                                                                             | 4.72 ms: 1.02x slower                                                                                                     |
| Geometric mean  | (ref)                                                                                                               | 1.04x faster                                                                                                              |

All benchmarks:
===============

| Benchmark                        | results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json | results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------:|
| generators                       | 18.3 ms                                                                                                             | 15.0 ms: 1.22x faster                                                                                                     |
| genshi_xml                       | 21.1 ms                                                                                                             | 19.8 ms: 1.06x faster                                                                                                     |
| hexiom                           | 2.75 ms                                                                                                             | 2.60 ms: 1.06x faster                                                                                                     |
| xml_etree_generate               | 34.5 ms                                                                                                             | 32.6 ms: 1.06x faster                                                                                                     |
| django_template                  | 14.7 ms                                                                                                             | 14.0 ms: 1.05x faster                                                                                                     |
| xml_etree_iterparse              | 40.0 ms                                                                                                             | 38.0 ms: 1.05x faster                                                                                                     |
| xml_etree_parse                  | 63.2 ms                                                                                                             | 60.2 ms: 1.05x faster                                                                                                     |
| genshi_text                      | 9.68 ms                                                                                                             | 9.23 ms: 1.05x faster                                                                                                     |
| xml_etree_process                | 24.5 ms                                                                                                             | 23.6 ms: 1.04x faster                                                                                                     |
| tomli_loads                      | 915 ms                                                                                                              | 878 ms: 1.04x faster                                                                                                      |
| regex_compile                    | 45.1 ms                                                                                                             | 43.5 ms: 1.04x faster                                                                                                     |
| sqlglot_v2_normalize             | 45.5 ms                                                                                                             | 43.9 ms: 1.04x faster                                                                                                     |
| unpickle_pure_python             | 96.8 us                                                                                                             | 93.5 us: 1.04x faster                                                                                                     |
| json_dumps                       | 3.89 ms                                                                                                             | 3.78 ms: 1.03x faster                                                                                                     |
| async_tree_eager                 | 40.7 ms                                                                                                             | 39.7 ms: 1.03x faster                                                                                                     |
| sqlglot_v2_optimize              | 22.1 ms                                                                                                             | 21.5 ms: 1.03x faster                                                                                                     |
| bench_thread_pool                | 428 us                                                                                                              | 416 us: 1.03x faster                                                                                                      |
| mdp                              | 541 ms                                                                                                              | 528 ms: 1.03x faster                                                                                                      |
| async_tree_eager_io              | 228 ms                                                                                                              | 223 ms: 1.02x faster                                                                                                      |
| subparsers                       | 4.03 ms                                                                                                             | 3.94 ms: 1.02x faster                                                                                                     |
| logging_silent                   | 40.5 ns                                                                                                             | 39.6 ns: 1.02x faster                                                                                                     |
| unpickle_list                    | 2.10 us                                                                                                             | 2.06 us: 1.02x faster                                                                                                     |
| sympy_expand                     | 168 ms                                                                                                              | 164 ms: 1.02x faster                                                                                                      |
| sympy_sum                        | 54.5 ms                                                                                                             | 53.4 ms: 1.02x faster                                                                                                     |
| async_tree_none                  | 102 ms                                                                                                              | 100 ms: 1.02x faster                                                                                                      |
| html5lib                         | 21.6 ms                                                                                                             | 21.2 ms: 1.02x faster                                                                                                     |
| sqlglot_v2_transpile             | 621 us                                                                                                              | 610 us: 1.02x faster                                                                                                      |
| sqlglot_v2_parse                 | 510 us                                                                                                              | 501 us: 1.02x faster                                                                                                      |
| sympy_integrate                  | 7.34 ms                                                                                                             | 7.22 ms: 1.02x faster                                                                                                     |
| pickle_pure_python               | 139 us                                                                                                              | 137 us: 1.01x faster                                                                                                      |
| nqueens                          | 39.9 ms                                                                                                             | 39.4 ms: 1.01x faster                                                                                                     |
| thrift                           | 304 us                                                                                                              | 300 us: 1.01x faster                                                                                                      |
| go                               | 52.2 ms                                                                                                             | 51.5 ms: 1.01x faster                                                                                                     |
| json_loads                       | 10.7 us                                                                                                             | 10.6 us: 1.01x faster                                                                                                     |
| deepcopy_reduce                  | 1.07 us                                                                                                             | 1.06 us: 1.01x faster                                                                                                     |
| coverage                         | 31.9 ms                                                                                                             | 31.6 ms: 1.01x faster                                                                                                     |
| comprehensions                   | 7.04 us                                                                                                             | 6.97 us: 1.01x faster                                                                                                     |
| deepcopy                         | 101 us                                                                                                              | 99.6 us: 1.01x faster                                                                                                     |
| raytrace                         | 114 ms                                                                                                              | 113 ms: 1.01x faster                                                                                                      |
| sympy_str                        | 98.8 ms                                                                                                             | 97.9 ms: 1.01x faster                                                                                                     |
| async_tree_eager_memoization     | 106 ms                                                                                                              | 105 ms: 1.01x faster                                                                                                      |
| dulwich_log                      | 18.8 ms                                                                                                             | 18.7 ms: 1.01x faster                                                                                                     |
| 2to3                             | 112 ms                                                                                                              | 112 ms: 1.01x faster                                                                                                      |
| logging_simple                   | 2.23 us                                                                                                             | 2.22 us: 1.01x faster                                                                                                     |
| telco                            | 2.81 ms                                                                                                             | 2.79 ms: 1.01x faster                                                                                                     |
| pickle_dict                      | 12.9 us                                                                                                             | 12.9 us: 1.00x faster                                                                                                     |
| logging_format                   | 2.46 us                                                                                                             | 2.45 us: 1.00x faster                                                                                                     |
| deltablue                        | 1.45 ms                                                                                                             | 1.45 ms: 1.00x faster                                                                                                     |
| k_core                           | 900 ms                                                                                                              | 898 ms: 1.00x faster                                                                                                      |
| richards                         | 19.8 ms                                                                                                             | 19.8 ms: 1.00x faster                                                                                                     |
| pidigits                         | 162 ms                                                                                                              | 163 ms: 1.01x slower                                                                                                      |
| gc_traversal                     | 2.05 ms                                                                                                             | 2.07 ms: 1.01x slower                                                                                                     |
| async_tree_eager_tg              | 79.8 ms                                                                                                             | 80.3 ms: 1.01x slower                                                                                                     |
| regex_dna                        | 97.6 ms                                                                                                             | 98.2 ms: 1.01x slower                                                                                                     |
| pickle_list                      | 2.12 us                                                                                                             | 2.13 us: 1.01x slower                                                                                                     |
| scimark_lu                       | 44.0 ms                                                                                                             | 44.3 ms: 1.01x slower                                                                                                     |
| nbody                            | 45.7 ms                                                                                                             | 46.1 ms: 1.01x slower                                                                                                     |
| python_startup_no_site           | 6.24 ms                                                                                                             | 6.29 ms: 1.01x slower                                                                                                     |
| python_startup                   | 8.67 ms                                                                                                             | 8.75 ms: 1.01x slower                                                                                                     |
| pathlib                          | 10.7 ms                                                                                                             | 10.8 ms: 1.01x slower                                                                                                     |
| spectral_norm                    | 43.8 ms                                                                                                             | 44.5 ms: 1.01x slower                                                                                                     |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                                                              | 243 ms: 1.01x slower                                                                                                      |
| pickle                           | 5.96 us                                                                                                             | 6.05 us: 1.01x slower                                                                                                     |
| mako                             | 4.65 ms                                                                                                             | 4.72 ms: 1.02x slower                                                                                                     |
| create_gc_cycles                 | 917 us                                                                                                              | 932 us: 1.02x slower                                                                                                      |
| bench_mp_pool                    | 44.5 ms                                                                                                             | 45.3 ms: 1.02x slower                                                                                                     |
| chaos                            | 25.0 ms                                                                                                             | 25.5 ms: 1.02x slower                                                                                                     |
| shortest_path                    | 221 ms                                                                                                              | 226 ms: 1.02x slower                                                                                                      |
| unpickle                         | 6.25 us                                                                                                             | 6.38 us: 1.02x slower                                                                                                     |
| connected_components             | 205 ms                                                                                                              | 210 ms: 1.02x slower                                                                                                      |
| coroutines                       | 10.1 ms                                                                                                             | 10.4 ms: 1.03x slower                                                                                                     |
| pprint_safe_repr                 | 301 ms                                                                                                              | 310 ms: 1.03x slower                                                                                                      |
| scimark_fft                      | 120 ms                                                                                                              | 124 ms: 1.03x slower                                                                                                      |
| scimark_sparse_mat_mult          | 1.80 ms                                                                                                             | 1.86 ms: 1.03x slower                                                                                                     |
| regex_v8                         | 9.72 ms                                                                                                             | 10.0 ms: 1.03x slower                                                                                                     |
| pprint_pformat                   | 611 ms                                                                                                              | 632 ms: 1.03x slower                                                                                                      |
| crypto_pyaes                     | 36.7 ms                                                                                                             | 37.9 ms: 1.03x slower                                                                                                     |
| float                            | 27.1 ms                                                                                                             | 28.1 ms: 1.04x slower                                                                                                     |
| scimark_monte_carlo              | 27.7 ms                                                                                                             | 29.2 ms: 1.05x slower                                                                                                     |
| fannkuch                         | 170 ms                                                                                                              | 181 ms: 1.06x slower                                                                                                      |
| unpack_sequence                  | 28.0 ns                                                                                                             | 42.1 ns: 1.50x slower                                                                                                     |
| Geometric mean                   | (ref)                                                                                                               | 1.00x faster                                                                                                              |

Benchmark hidden because not significant (26): async_tree_memoization, async_tree_eager_io_tg, async_tree_io_tg, async_tree_none_tg, richards_super, pylint, async_tree_io, sphinx, typing_runtime_protocols, async_tree_memoization_tg, json, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed, async_tree_cpu_io_mixed_tg, sqlite_synth, many_optionals, pyflate, scimark_sor, docutils, bpe_tokeniser, deepcopy_memo, async_generators, meteor_contest, async_tree_eager_memoization_tg, regex_effbot, pycparser
Ignored benchmarks (4) of results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, dask

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 99.15% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x