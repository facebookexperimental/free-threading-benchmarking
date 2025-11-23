# Results vs. default_base_vs_NOGIL

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: darwin-arm64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.025x slower
- HPT reliability: 99.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 113 ms                                                                   | 121 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                                 | 987 ms: 1.04x faster                                                     |
| html5lib       | 22.0 ms                                                                  | 22.8 ms: 1.04x slower                                                    |
| sphinx         | 393 ms                                                                   | 406 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 225 ms                                                                   | 190 ms: 1.18x faster                                                     |
| async_tree_none_tg               | 97.7 ms                                                                  | 84.9 ms: 1.15x faster                                                    |
| async_tree_eager_io              | 227 ms                                                                   | 199 ms: 1.14x faster                                                     |
| async_tree_memoization_tg        | 138 ms                                                                   | 122 ms: 1.13x faster                                                     |
| async_tree_io_tg                 | 222 ms                                                                   | 196 ms: 1.13x faster                                                     |
| async_tree_eager_memoization_tg  | 125 ms                                                                   | 111 ms: 1.13x faster                                                     |
| async_tree_io                    | 228 ms                                                                   | 207 ms: 1.10x faster                                                     |
| async_tree_memoization           | 140 ms                                                                   | 128 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 254 ms                                                                   | 237 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 241 ms                                                                   | 228 ms: 1.06x faster                                                     |
| async_tree_eager_tg              | 80.5 ms                                                                  | 76.6 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 254 ms                                                                   | 244 ms: 1.04x faster                                                     |
| async_tree_none                  | 99.5 ms                                                                  | 97.9 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 109 ms                                                                   | 107 ms: 1.02x faster                                                     |
| async_generators                 | 176 ms                                                                   | 182 ms: 1.03x slower                                                     |
| coroutines                       | 10.2 ms                                                                  | 10.8 ms: 1.06x slower                                                    |
| async_tree_eager                 | 41.7 ms                                                                  | 46.7 ms: 1.12x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 162 ms                                                                   | 161 ms: 1.00x faster                                                     |
| float          | 27.0 ms                                                                  | 27.4 ms: 1.02x slower                                                    |
| nbody          | 45.8 ms                                                                  | 55.5 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 9.75 ms                                                                  | 9.21 ms: 1.06x faster                                                    |
| regex_effbot   | 1.42 ms                                                                  | 1.44 ms: 1.01x slower                                                    |
| regex_dna      | 93.3 ms                                                                  | 94.8 ms: 1.02x slower                                                    |
| regex_compile  | 46.2 ms                                                                  | 50.7 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 60.2 ms                                                                  | 56.3 ms: 1.07x faster                                                    |
| xml_etree_iterparse  | 38.2 ms                                                                  | 36.7 ms: 1.04x faster                                                    |
| pickle_pure_python   | 142 us                                                                   | 145 us: 1.02x slower                                                     |
| json_dumps           | 3.86 ms                                                                  | 3.94 ms: 1.02x slower                                                    |
| tomli_loads          | 848 ms                                                                   | 871 ms: 1.03x slower                                                     |
| xml_etree_generate   | 34.6 ms                                                                  | 36.1 ms: 1.04x slower                                                    |
| xml_etree_process    | 24.5 ms                                                                  | 26.2 ms: 1.07x slower                                                    |
| unpickle_pure_python | 95.5 us                                                                  | 109 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.82 ms                                                                  | 9.71 ms: 1.10x slower                                                    |
| python_startup_no_site | 6.25 ms                                                                  | 7.05 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 14.9 ms                                                                  | 15.8 ms: 1.06x slower                                                    |
| genshi_xml      | 21.5 ms                                                                  | 23.0 ms: 1.07x slower                                                    |
| genshi_text     | 9.93 ms                                                                  | 11.2 ms: 1.13x slower                                                    |
| mako            | 4.87 ms                                                                  | 5.52 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.05 ms                                                                  | 779 us: 2.63x faster                                                     |
| create_gc_cycles                 | 913 us                                                                   | 496 us: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 225 ms                                                                   | 190 ms: 1.18x faster                                                     |
| sqlite_synth                     | 965 ns                                                                   | 825 ns: 1.17x faster                                                     |
| async_tree_none_tg               | 97.7 ms                                                                  | 84.9 ms: 1.15x faster                                                    |
| async_tree_eager_io              | 227 ms                                                                   | 199 ms: 1.14x faster                                                     |
| async_tree_memoization_tg        | 138 ms                                                                   | 122 ms: 1.13x faster                                                     |
| async_tree_io_tg                 | 222 ms                                                                   | 196 ms: 1.13x faster                                                     |
| async_tree_eager_memoization_tg  | 125 ms                                                                   | 111 ms: 1.13x faster                                                     |
| async_tree_io                    | 228 ms                                                                   | 207 ms: 1.10x faster                                                     |
| async_tree_memoization           | 140 ms                                                                   | 128 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 254 ms                                                                   | 237 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 60.2 ms                                                                  | 56.3 ms: 1.07x faster                                                    |
| regex_v8                         | 9.75 ms                                                                  | 9.21 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 241 ms                                                                   | 228 ms: 1.06x faster                                                     |
| async_tree_eager_tg              | 80.5 ms                                                                  | 76.6 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 38.2 ms                                                                  | 36.7 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 254 ms                                                                   | 244 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                                 | 987 ms: 1.04x faster                                                     |
| fannkuch                         | 173 ms                                                                   | 169 ms: 1.02x faster                                                     |
| async_tree_none                  | 99.5 ms                                                                  | 97.9 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 109 ms                                                                   | 107 ms: 1.02x faster                                                     |
| pidigits                         | 162 ms                                                                   | 161 ms: 1.00x faster                                                     |
| bpe_tokeniser                    | 1.96 sec                                                                 | 1.98 sec: 1.01x slower                                                   |
| regex_effbot                     | 1.42 ms                                                                  | 1.44 ms: 1.01x slower                                                    |
| float                            | 27.0 ms                                                                  | 27.4 ms: 1.02x slower                                                    |
| pylint                           | 109 ms                                                                   | 111 ms: 1.02x slower                                                     |
| regex_dna                        | 93.3 ms                                                                  | 94.8 ms: 1.02x slower                                                    |
| pickle_pure_python               | 142 us                                                                   | 145 us: 1.02x slower                                                     |
| json_dumps                       | 3.86 ms                                                                  | 3.94 ms: 1.02x slower                                                    |
| tomli_loads                      | 848 ms                                                                   | 871 ms: 1.03x slower                                                     |
| generators                       | 18.9 ms                                                                  | 19.4 ms: 1.03x slower                                                    |
| async_generators                 | 176 ms                                                                   | 182 ms: 1.03x slower                                                     |
| sphinx                           | 393 ms                                                                   | 406 ms: 1.03x slower                                                     |
| sqlglot_v2_normalize             | 46.4 ms                                                                  | 47.9 ms: 1.03x slower                                                    |
| telco                            | 2.87 ms                                                                  | 2.97 ms: 1.04x slower                                                    |
| html5lib                         | 22.0 ms                                                                  | 22.8 ms: 1.04x slower                                                    |
| pyflate                          | 184 ms                                                                   | 191 ms: 1.04x slower                                                     |
| dask                             | 541 ms                                                                   | 562 ms: 1.04x slower                                                     |
| xml_etree_generate               | 34.6 ms                                                                  | 36.1 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 43.7 ms                                                                  | 45.8 ms: 1.05x slower                                                    |
| sqlglot_v2_optimize              | 22.5 ms                                                                  | 23.6 ms: 1.05x slower                                                    |
| deepcopy                         | 102 us                                                                   | 108 us: 1.05x slower                                                     |
| pprint_safe_repr                 | 315 ms                                                                   | 334 ms: 1.06x slower                                                     |
| coroutines                       | 10.2 ms                                                                  | 10.8 ms: 1.06x slower                                                    |
| django_template                  | 14.9 ms                                                                  | 15.8 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.5 ms                                                                  | 23.0 ms: 1.07x slower                                                    |
| 2to3                             | 113 ms                                                                   | 121 ms: 1.07x slower                                                     |
| xml_etree_process                | 24.5 ms                                                                  | 26.2 ms: 1.07x slower                                                    |
| sqlglot_v2_transpile             | 633 us                                                                   | 679 us: 1.07x slower                                                     |
| pprint_pformat                   | 637 ms                                                                   | 684 ms: 1.07x slower                                                     |
| subparsers                       | 17.5 ms                                                                  | 18.9 ms: 1.08x slower                                                    |
| many_optionals                   | 354 us                                                                   | 383 us: 1.08x slower                                                     |
| thrift                           | 306 us                                                                   | 331 us: 1.08x slower                                                     |
| logging_silent                   | 41.3 ns                                                                  | 44.7 ns: 1.08x slower                                                    |
| sympy_integrate                  | 7.39 ms                                                                  | 8.02 ms: 1.09x slower                                                    |
| deltablue                        | 1.45 ms                                                                  | 1.58 ms: 1.09x slower                                                    |
| logging_simple                   | 2.23 us                                                                  | 2.43 us: 1.09x slower                                                    |
| deepcopy_reduce                  | 1.09 us                                                                  | 1.19 us: 1.09x slower                                                    |
| logging_format                   | 2.45 us                                                                  | 2.68 us: 1.09x slower                                                    |
| sympy_str                        | 101 ms                                                                   | 110 ms: 1.09x slower                                                     |
| sqlglot_v2_parse                 | 514 us                                                                   | 562 us: 1.09x slower                                                     |
| sympy_sum                        | 54.9 ms                                                                  | 60.3 ms: 1.10x slower                                                    |
| regex_compile                    | 46.2 ms                                                                  | 50.7 ms: 1.10x slower                                                    |
| python_startup                   | 8.82 ms                                                                  | 9.71 ms: 1.10x slower                                                    |
| sympy_expand                     | 170 ms                                                                   | 188 ms: 1.10x slower                                                     |
| hexiom                           | 2.79 ms                                                                  | 3.07 ms: 1.10x slower                                                    |
| go                               | 53.2 ms                                                                  | 58.7 ms: 1.10x slower                                                    |
| nqueens                          | 39.1 ms                                                                  | 43.2 ms: 1.10x slower                                                    |
| meteor_contest                   | 49.8 ms                                                                  | 55.0 ms: 1.11x slower                                                    |
| raytrace                         | 114 ms                                                                   | 127 ms: 1.12x slower                                                     |
| deepcopy_memo                    | 11.4 us                                                                  | 12.7 us: 1.12x slower                                                    |
| chaos                            | 24.7 ms                                                                  | 27.6 ms: 1.12x slower                                                    |
| scimark_sor                      | 49.1 ms                                                                  | 54.8 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 63.8 us                                                                  | 71.4 us: 1.12x slower                                                    |
| async_tree_eager                 | 41.7 ms                                                                  | 46.7 ms: 1.12x slower                                                    |
| richards                         | 20.2 ms                                                                  | 22.6 ms: 1.12x slower                                                    |
| coverage                         | 35.2 ms                                                                  | 39.5 ms: 1.12x slower                                                    |
| mdp                              | 536 ms                                                                   | 602 ms: 1.12x slower                                                     |
| genshi_text                      | 9.93 ms                                                                  | 11.2 ms: 1.13x slower                                                    |
| python_startup_no_site           | 6.25 ms                                                                  | 7.05 ms: 1.13x slower                                                    |
| mako                             | 4.87 ms                                                                  | 5.52 ms: 1.13x slower                                                    |
| comprehensions                   | 7.13 us                                                                  | 8.09 us: 1.13x slower                                                    |
| scimark_fft                      | 114 ms                                                                   | 130 ms: 1.14x slower                                                     |
| unpickle_pure_python             | 95.5 us                                                                  | 109 us: 1.14x slower                                                     |
| crypto_pyaes                     | 36.7 ms                                                                  | 42.1 ms: 1.15x slower                                                    |
| richards_super                   | 22.7 ms                                                                  | 26.1 ms: 1.15x slower                                                    |
| spectral_norm                    | 42.8 ms                                                                  | 50.6 ms: 1.18x slower                                                    |
| scimark_monte_carlo              | 28.0 ms                                                                  | 33.2 ms: 1.19x slower                                                    |
| scimark_lu                       | 45.7 ms                                                                  | 54.4 ms: 1.19x slower                                                    |
| nbody                            | 45.8 ms                                                                  | 55.5 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.77 ms                                                                  | 2.22 ms: 1.25x slower                                                    |
| bench_thread_pool                | 427 us                                                                   | 561 us: 1.31x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.03x slower                                                             |

Benchmark hidden because not significant (7): asyncio_websockets, pathlib, json_loads, async_tree_eager_cpu_io_mixed, dulwich_log, json, pycparser
Ignored benchmarks (8) of results/bm-20251122-3.15.0a2+-227b9d3/bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.025x slower

# HPT report

- Reliability score: 99.83% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x