# Results vs. base

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: darwin-arm64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.002x faster
- HPT reliability: 99.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 113 ms                                                                   | 113 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                    | 10.2 ms                                                                  | 10.0 ms: 1.02x faster                                                    |
| async_tree_eager              | 41.7 ms                                                                  | 41.3 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed | 223 ms                                                                   | 222 ms: 1.00x faster                                                     |
| asyncio_websockets            | 188 ms                                                                   | 187 ms: 1.00x faster                                                     |
| async_generators              | 176 ms                                                                   | 178 ms: 1.01x slower                                                     |
| Geometric mean                | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (14): async_tree_eager_io_tg, async_tree_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg, async_tree_eager_io, async_tree_eager_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_eager_memoization, async_tree_none, async_tree_io_tg, async_tree_eager_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 27.0 ms                                                                  | 26.4 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 9.75 ms                                                                  | 9.64 ms: 1.01x faster                                                    |
| regex_dna      | 93.3 ms                                                                  | 95.6 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 142 us                                                                   | 139 us: 1.02x faster                                                     |
| tomli_loads          | 848 ms                                                                   | 840 ms: 1.01x faster                                                     |
| json_dumps           | 3.86 ms                                                                  | 3.89 ms: 1.01x slower                                                    |
| unpickle_pure_python | 95.5 us                                                                  | 97.5 us: 1.02x slower                                                    |
| xml_etree_iterparse  | 38.2 ms                                                                  | 39.1 ms: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (4): json_loads, xml_etree_generate, xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 6.25 ms                                                                  | 6.25 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.87 ms                                                                  | 4.69 ms: 1.04x faster                                                    |
| genshi_xml      | 21.5 ms                                                                  | 21.2 ms: 1.01x faster                                                    |
| django_template | 14.9 ms                                                                  | 14.7 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                     | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako                          | 4.87 ms                                                                  | 4.69 ms: 1.04x faster                                                    |
| coverage                      | 35.2 ms                                                                  | 34.2 ms: 1.03x faster                                                    |
| float                         | 27.0 ms                                                                  | 26.4 ms: 1.02x faster                                                    |
| scimark_lu                    | 45.7 ms                                                                  | 44.7 ms: 1.02x faster                                                    |
| pickle_pure_python            | 142 us                                                                   | 139 us: 1.02x faster                                                     |
| deepcopy_memo                 | 11.4 us                                                                  | 11.2 us: 1.02x faster                                                    |
| coroutines                    | 10.2 ms                                                                  | 10.0 ms: 1.02x faster                                                    |
| genshi_xml                    | 21.5 ms                                                                  | 21.2 ms: 1.01x faster                                                    |
| generators                    | 18.9 ms                                                                  | 18.6 ms: 1.01x faster                                                    |
| django_template               | 14.9 ms                                                                  | 14.7 ms: 1.01x faster                                                    |
| deepcopy                      | 102 us                                                                   | 101 us: 1.01x faster                                                     |
| regex_v8                      | 9.75 ms                                                                  | 9.64 ms: 1.01x faster                                                    |
| nqueens                       | 39.1 ms                                                                  | 38.8 ms: 1.01x faster                                                    |
| async_tree_eager              | 41.7 ms                                                                  | 41.3 ms: 1.01x faster                                                    |
| tomli_loads                   | 848 ms                                                                   | 840 ms: 1.01x faster                                                     |
| deepcopy_reduce               | 1.09 us                                                                  | 1.08 us: 1.01x faster                                                    |
| typing_runtime_protocols      | 63.8 us                                                                  | 63.3 us: 1.01x faster                                                    |
| chaos                         | 24.7 ms                                                                  | 24.5 ms: 1.01x faster                                                    |
| raytrace                      | 114 ms                                                                   | 113 ms: 1.01x faster                                                     |
| pprint_safe_repr              | 315 ms                                                                   | 313 ms: 1.01x faster                                                     |
| go                            | 53.2 ms                                                                  | 52.8 ms: 1.01x faster                                                    |
| sqlite_synth                  | 965 ns                                                                   | 959 ns: 1.01x faster                                                     |
| sqlglot_v2_transpile          | 633 us                                                                   | 629 us: 1.01x faster                                                     |
| create_gc_cycles              | 913 us                                                                   | 909 us: 1.00x faster                                                     |
| spectral_norm                 | 42.8 ms                                                                  | 42.6 ms: 1.00x faster                                                    |
| richards                      | 20.2 ms                                                                  | 20.1 ms: 1.00x faster                                                    |
| pprint_pformat                | 637 ms                                                                   | 634 ms: 1.00x faster                                                     |
| dulwich_log                   | 18.8 ms                                                                  | 18.7 ms: 1.00x faster                                                    |
| sqlglot_v2_normalize          | 46.4 ms                                                                  | 46.2 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed | 223 ms                                                                   | 222 ms: 1.00x faster                                                     |
| asyncio_websockets            | 188 ms                                                                   | 187 ms: 1.00x faster                                                     |
| richards_super                | 22.7 ms                                                                  | 22.6 ms: 1.00x faster                                                    |
| scimark_monte_carlo           | 28.0 ms                                                                  | 28.0 ms: 1.00x faster                                                    |
| hexiom                        | 2.79 ms                                                                  | 2.78 ms: 1.00x faster                                                    |
| mdp                           | 536 ms                                                                   | 535 ms: 1.00x faster                                                     |
| 2to3                          | 113 ms                                                                   | 113 ms: 1.00x faster                                                     |
| python_startup_no_site        | 6.25 ms                                                                  | 6.25 ms: 1.00x slower                                                    |
| bpe_tokeniser                 | 1.96 sec                                                                 | 1.97 sec: 1.00x slower                                                   |
| subparsers                    | 17.5 ms                                                                  | 17.6 ms: 1.00x slower                                                    |
| thrift                        | 306 us                                                                   | 307 us: 1.00x slower                                                     |
| sympy_sum                     | 54.9 ms                                                                  | 55.2 ms: 1.00x slower                                                    |
| comprehensions                | 7.13 us                                                                  | 7.17 us: 1.01x slower                                                    |
| async_generators              | 176 ms                                                                   | 178 ms: 1.01x slower                                                     |
| json_dumps                    | 3.86 ms                                                                  | 3.89 ms: 1.01x slower                                                    |
| scimark_fft                   | 114 ms                                                                   | 116 ms: 1.01x slower                                                     |
| unpickle_pure_python          | 95.5 us                                                                  | 97.5 us: 1.02x slower                                                    |
| xml_etree_iterparse           | 38.2 ms                                                                  | 39.1 ms: 1.02x slower                                                    |
| regex_dna                     | 93.3 ms                                                                  | 95.6 ms: 1.02x slower                                                    |
| Geometric mean                | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (52): async_tree_eager_io_tg, async_tree_cpu_io_mixed_tg, json_loads, docutils, sqlglot_v2_parse, scimark_sparse_mat_mult, gc_traversal, async_tree_eager_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg, sqlglot_v2_optimize, nbody, genshi_text, pathlib, async_tree_eager_io, pycparser, fannkuch, pylint, logging_silent, async_tree_eager_memoization_tg, json, logging_simple, sympy_str, sphinx, async_tree_memoization, async_tree_none_tg, html5lib, async_tree_eager_memoization, dask, crypto_pyaes, pidigits, python_startup, regex_compile, bench_thread_pool, xml_etree_generate, meteor_contest, bench_mp_pool, xml_etree_parse, many_optionals, xml_etree_process, regex_effbot, sympy_expand, async_tree_none, sympy_integrate, deltablue, logging_format, scimark_sor, telco, async_tree_io_tg, pyflate, async_tree_eager_tg
Ignored benchmarks (8) of results/bm-20251122-3.15.0a2+-227b9d3/bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 99.59% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x