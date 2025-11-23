# Results vs. base

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: darwin-arm64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.003x faster
- HPT reliability: 58.54%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 121 ms                                                                   | 121 ms: 1.00x faster                                                     |
| sphinx         | 413 ms                                                                   | 406 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets            | 189 ms                                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager              | 46.8 ms                                                                  | 46.7 ms: 1.00x faster                                                    |
| async_tree_io                 | 206 ms                                                                   | 207 ms: 1.00x slower                                                     |
| async_tree_io_tg              | 196 ms                                                                   | 196 ms: 1.00x slower                                                     |
| async_tree_none               | 97.5 ms                                                                  | 97.9 ms: 1.00x slower                                                    |
| async_tree_eager_io           | 199 ms                                                                   | 199 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed | 223 ms                                                                   | 224 ms: 1.00x slower                                                     |
| async_tree_cpu_io_mixed       | 243 ms                                                                   | 244 ms: 1.00x slower                                                     |
| async_generators              | 180 ms                                                                   | 182 ms: 1.01x slower                                                     |
| coroutines                    | 10.6 ms                                                                  | 10.8 ms: 1.02x slower                                                    |
| Geometric mean                | (ref)                                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (9): async_tree_memoization_tg, async_tree_eager_io_tg, async_tree_none_tg, async_tree_eager_memoization, async_tree_memoization, async_tree_eager_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 27.6 ms                                                                  | 27.4 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 9.29 ms                                                                  | 9.21 ms: 1.01x faster                                                    |
| regex_compile  | 50.9 ms                                                                  | 50.7 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 60.9 ms                                                                  | 56.3 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 39.0 ms                                                                  | 36.7 ms: 1.06x faster                                                    |
| xml_etree_generate   | 36.4 ms                                                                  | 36.1 ms: 1.01x faster                                                    |
| json_dumps           | 3.97 ms                                                                  | 3.94 ms: 1.01x faster                                                    |
| xml_etree_process    | 26.3 ms                                                                  | 26.2 ms: 1.00x faster                                                    |
| unpickle_pure_python | 107 us                                                                   | 109 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (3): tomli_loads, pickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 5.55 ms                                                                  | 5.52 ms: 1.00x faster                                                    |
| genshi_xml      | 22.9 ms                                                                  | 23.0 ms: 1.00x slower                                                    |
| django_template | 15.7 ms                                                                  | 15.8 ms: 1.01x slower                                                    |
| genshi_text     | 11.1 ms                                                                  | 11.2 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                     | bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse               | 60.9 ms                                                                  | 56.3 ms: 1.08x faster                                                    |
| xml_etree_iterparse           | 39.0 ms                                                                  | 36.7 ms: 1.06x faster                                                    |
| pylint                        | 117 ms                                                                   | 111 ms: 1.05x faster                                                     |
| sphinx                        | 413 ms                                                                   | 406 ms: 1.02x faster                                                     |
| scimark_sor                   | 55.9 ms                                                                  | 54.8 ms: 1.02x faster                                                    |
| deltablue                     | 1.60 ms                                                                  | 1.58 ms: 1.01x faster                                                    |
| deepcopy_reduce               | 1.21 us                                                                  | 1.19 us: 1.01x faster                                                    |
| deepcopy_memo                 | 12.9 us                                                                  | 12.7 us: 1.01x faster                                                    |
| fannkuch                      | 171 ms                                                                   | 169 ms: 1.01x faster                                                     |
| gc_traversal                  | 787 us                                                                   | 779 us: 1.01x faster                                                     |
| create_gc_cycles              | 501 us                                                                   | 496 us: 1.01x faster                                                     |
| telco                         | 3.00 ms                                                                  | 2.97 ms: 1.01x faster                                                    |
| meteor_contest                | 55.5 ms                                                                  | 55.0 ms: 1.01x faster                                                    |
| xml_etree_generate            | 36.4 ms                                                                  | 36.1 ms: 1.01x faster                                                    |
| float                         | 27.6 ms                                                                  | 27.4 ms: 1.01x faster                                                    |
| scimark_monte_carlo           | 33.5 ms                                                                  | 33.2 ms: 1.01x faster                                                    |
| regex_v8                      | 9.29 ms                                                                  | 9.21 ms: 1.01x faster                                                    |
| asyncio_websockets            | 189 ms                                                                   | 188 ms: 1.01x faster                                                     |
| json_dumps                    | 3.97 ms                                                                  | 3.94 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult       | 2.24 ms                                                                  | 2.22 ms: 1.01x faster                                                    |
| pprint_safe_repr              | 336 ms                                                                   | 334 ms: 1.01x faster                                                     |
| pprint_pformat                | 688 ms                                                                   | 684 ms: 1.01x faster                                                     |
| pyflate                       | 192 ms                                                                   | 191 ms: 1.01x faster                                                     |
| spectral_norm                 | 50.9 ms                                                                  | 50.6 ms: 1.01x faster                                                    |
| mdp                           | 605 ms                                                                   | 602 ms: 1.01x faster                                                     |
| mako                          | 5.55 ms                                                                  | 5.52 ms: 1.00x faster                                                    |
| regex_compile                 | 50.9 ms                                                                  | 50.7 ms: 1.00x faster                                                    |
| thrift                        | 333 us                                                                   | 331 us: 1.00x faster                                                     |
| sqlglot_v2_normalize          | 48.2 ms                                                                  | 47.9 ms: 1.00x faster                                                    |
| logging_format                | 2.69 us                                                                  | 2.68 us: 1.00x faster                                                    |
| 2to3                          | 121 ms                                                                   | 121 ms: 1.00x faster                                                     |
| crypto_pyaes                  | 42.3 ms                                                                  | 42.1 ms: 1.00x faster                                                    |
| async_tree_eager              | 46.8 ms                                                                  | 46.7 ms: 1.00x faster                                                    |
| xml_etree_process             | 26.3 ms                                                                  | 26.2 ms: 1.00x faster                                                    |
| bench_mp_pool                 | 45.9 ms                                                                  | 45.8 ms: 1.00x faster                                                    |
| bpe_tokeniser                 | 1.98 sec                                                                 | 1.98 sec: 1.00x slower                                                   |
| async_tree_io                 | 206 ms                                                                   | 207 ms: 1.00x slower                                                     |
| async_tree_io_tg              | 196 ms                                                                   | 196 ms: 1.00x slower                                                     |
| generators                    | 19.3 ms                                                                  | 19.4 ms: 1.00x slower                                                    |
| richards_super                | 26.0 ms                                                                  | 26.1 ms: 1.00x slower                                                    |
| genshi_xml                    | 22.9 ms                                                                  | 23.0 ms: 1.00x slower                                                    |
| async_tree_none               | 97.5 ms                                                                  | 97.9 ms: 1.00x slower                                                    |
| async_tree_eager_io           | 199 ms                                                                   | 199 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed | 223 ms                                                                   | 224 ms: 1.00x slower                                                     |
| sqlglot_v2_optimize           | 23.5 ms                                                                  | 23.6 ms: 1.00x slower                                                    |
| comprehensions                | 8.06 us                                                                  | 8.09 us: 1.00x slower                                                    |
| sympy_expand                  | 187 ms                                                                   | 188 ms: 1.00x slower                                                     |
| async_tree_cpu_io_mixed       | 243 ms                                                                   | 244 ms: 1.00x slower                                                     |
| sympy_str                     | 109 ms                                                                   | 110 ms: 1.00x slower                                                     |
| richards                      | 22.5 ms                                                                  | 22.6 ms: 1.00x slower                                                    |
| django_template               | 15.7 ms                                                                  | 15.8 ms: 1.01x slower                                                    |
| scimark_fft                   | 129 ms                                                                   | 130 ms: 1.01x slower                                                     |
| genshi_text                   | 11.1 ms                                                                  | 11.2 ms: 1.01x slower                                                    |
| json                          | 1.94 ms                                                                  | 1.96 ms: 1.01x slower                                                    |
| pycparser                     | 459 ms                                                                   | 462 ms: 1.01x slower                                                     |
| dulwich_log                   | 18.7 ms                                                                  | 18.8 ms: 1.01x slower                                                    |
| async_generators              | 180 ms                                                                   | 182 ms: 1.01x slower                                                     |
| many_optionals                | 378 us                                                                   | 383 us: 1.01x slower                                                     |
| subparsers                    | 18.6 ms                                                                  | 18.9 ms: 1.01x slower                                                    |
| scimark_lu                    | 53.7 ms                                                                  | 54.4 ms: 1.01x slower                                                    |
| logging_silent                | 44.0 ns                                                                  | 44.7 ns: 1.02x slower                                                    |
| unpickle_pure_python          | 107 us                                                                   | 109 us: 1.02x slower                                                     |
| coroutines                    | 10.6 ms                                                                  | 10.8 ms: 1.02x slower                                                    |
| Geometric mean                | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (37): regex_dna, docutils, go, async_tree_memoization_tg, coverage, bench_thread_pool, hexiom, async_tree_eager_io_tg, pathlib, async_tree_none_tg, sympy_integrate, logging_simple, chaos, pidigits, python_startup, python_startup_no_site, deepcopy, sympy_sum, html5lib, regex_effbot, async_tree_eager_memoization, async_tree_memoization, tomli_loads, async_tree_eager_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization_tg, nbody, raytrace, pickle_pure_python, sqlglot_v2_parse, async_tree_cpu_io_mixed_tg, sqlglot_v2_transpile, dask, typing_runtime_protocols, sqlite_synth, nqueens, json_loads
Ignored benchmarks (8) of results/bm-20251122-3.15.0a2+-227b9d3-NOGIL/bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 58.54% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x