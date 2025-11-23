# Results vs. base

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: linux-x86_64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.004x faster
- HPT reliability: 68.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 2.71 sec                                                               | 2.69 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 512 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed_tg | 533 ms                                                                 | 488 ms: 1.09x faster                                                   |
| async_tree_io              | 540 ms                                                                 | 544 ms: 1.01x slower                                                   |
| async_tree_io_tg           | 514 ms                                                                 | 519 ms: 1.01x slower                                                   |
| async_tree_memoization_tg  | 283 ms                                                                 | 286 ms: 1.01x slower                                                   |
| coroutines                 | 24.7 ms                                                                | 25.1 ms: 1.01x slower                                                  |
| async_tree_none_tg         | 224 ms                                                                 | 228 ms: 1.02x slower                                                   |
| async_generators           | 366 ms                                                                 | 376 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 227 ms                                                                 | 192 ms: 1.18x faster                                                   |
| nbody          | 126 ms                                                                 | 124 ms: 1.01x faster                                                   |
| float          | 70.4 ms                                                                | 70.1 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.99 ms                                                                | 2.66 ms: 1.12x faster                                                  |
| regex_dna      | 182 ms                                                                 | 164 ms: 1.11x faster                                                   |
| regex_v8       | 21.2 ms                                                                | 20.3 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python  | 342 us                                                                 | 337 us: 1.01x faster                                                   |
| xml_etree_generate  | 96.6 ms                                                                | 95.7 ms: 1.01x faster                                                  |
| json_dumps          | 11.0 ms                                                                | 10.9 ms: 1.01x faster                                                  |
| xml_etree_process   | 69.4 ms                                                                | 69.0 ms: 1.01x faster                                                  |
| xml_etree_iterparse | 88.1 ms                                                                | 88.7 ms: 1.01x slower                                                  |
| json_loads          | 31.5 us                                                                | 31.8 us: 1.01x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_parse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.63 ms                                                                | 9.57 ms: 1.01x faster                                                  |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 40.4 ms                                                                | 40.2 ms: 1.01x faster                                                  |
| genshi_text     | 26.5 ms                                                                | 26.7 ms: 1.01x slower                                                  |
| genshi_xml      | 57.2 ms                                                                | 58.1 ms: 1.02x slower                                                  |
| mako            | 15.4 ms                                                                | 15.8 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                   | 227 ms                                                                 | 192 ms: 1.18x faster                                                   |
| regex_effbot               | 2.99 ms                                                                | 2.66 ms: 1.12x faster                                                  |
| regex_dna                  | 182 ms                                                                 | 164 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 512 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed_tg | 533 ms                                                                 | 488 ms: 1.09x faster                                                   |
| regex_v8                   | 21.2 ms                                                                | 20.3 ms: 1.05x faster                                                  |
| thrift                     | 865 us                                                                 | 852 us: 1.01x faster                                                   |
| pickle_pure_python         | 342 us                                                                 | 337 us: 1.01x faster                                                   |
| create_gc_cycles           | 1.52 ms                                                                | 1.50 ms: 1.01x faster                                                  |
| coverage                   | 111 ms                                                                 | 110 ms: 1.01x faster                                                   |
| nbody                      | 126 ms                                                                 | 124 ms: 1.01x faster                                                   |
| typing_runtime_protocols   | 189 us                                                                 | 186 us: 1.01x faster                                                   |
| scimark_lu                 | 133 ms                                                                 | 131 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.05 us                                                                | 2.03 us: 1.01x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 345 ms: 1.01x faster                                                   |
| xml_etree_generate         | 96.6 ms                                                                | 95.7 ms: 1.01x faster                                                  |
| gc_traversal               | 1.95 ms                                                                | 1.93 ms: 1.01x faster                                                  |
| docutils                   | 2.71 sec                                                               | 2.69 sec: 1.01x faster                                                 |
| json_dumps                 | 11.0 ms                                                                | 10.9 ms: 1.01x faster                                                  |
| sympy_str                  | 311 ms                                                                 | 309 ms: 1.01x faster                                                   |
| django_template            | 40.4 ms                                                                | 40.2 ms: 1.01x faster                                                  |
| python_startup_no_site     | 9.63 ms                                                                | 9.57 ms: 1.01x faster                                                  |
| xml_etree_process          | 69.4 ms                                                                | 69.0 ms: 1.01x faster                                                  |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.43 sec                                                               | 4.41 sec: 1.01x faster                                                 |
| float                      | 70.4 ms                                                                | 70.1 ms: 1.00x faster                                                  |
| raytrace                   | 297 ms                                                                 | 296 ms: 1.00x faster                                                   |
| crypto_pyaes               | 86.0 ms                                                                | 86.3 ms: 1.00x slower                                                  |
| pprint_safe_repr           | 776 ms                                                                 | 779 ms: 1.00x slower                                                   |
| telco                      | 172 ms                                                                 | 173 ms: 1.00x slower                                                   |
| pathlib                    | 17.6 ms                                                                | 17.7 ms: 1.01x slower                                                  |
| comprehensions             | 17.8 us                                                                | 17.9 us: 1.01x slower                                                  |
| async_tree_io              | 540 ms                                                                 | 544 ms: 1.01x slower                                                   |
| hexiom                     | 6.40 ms                                                                | 6.44 ms: 1.01x slower                                                  |
| xml_etree_iterparse        | 88.1 ms                                                                | 88.7 ms: 1.01x slower                                                  |
| richards_super             | 59.4 ms                                                                | 59.8 ms: 1.01x slower                                                  |
| json                       | 5.36 ms                                                                | 5.39 ms: 1.01x slower                                                  |
| chaos                      | 62.5 ms                                                                | 62.9 ms: 1.01x slower                                                  |
| go                         | 120 ms                                                                 | 121 ms: 1.01x slower                                                   |
| genshi_text                | 26.5 ms                                                                | 26.7 ms: 1.01x slower                                                  |
| json_loads                 | 31.5 us                                                                | 31.8 us: 1.01x slower                                                  |
| richards                   | 51.2 ms                                                                | 51.7 ms: 1.01x slower                                                  |
| sqlglot_v2_normalize       | 115 ms                                                                 | 116 ms: 1.01x slower                                                   |
| async_tree_io_tg           | 514 ms                                                                 | 519 ms: 1.01x slower                                                   |
| async_tree_memoization_tg  | 283 ms                                                                 | 286 ms: 1.01x slower                                                   |
| nqueens                    | 87.7 ms                                                                | 88.8 ms: 1.01x slower                                                  |
| coroutines                 | 24.7 ms                                                                | 25.1 ms: 1.01x slower                                                  |
| deepcopy_memo              | 30.5 us                                                                | 30.9 us: 1.01x slower                                                  |
| deepcopy                   | 276 us                                                                 | 279 us: 1.01x slower                                                   |
| genshi_xml                 | 57.2 ms                                                                | 58.1 ms: 1.02x slower                                                  |
| spectral_norm              | 110 ms                                                                 | 112 ms: 1.02x slower                                                   |
| pyflate                    | 458 ms                                                                 | 467 ms: 1.02x slower                                                   |
| async_tree_none_tg         | 224 ms                                                                 | 228 ms: 1.02x slower                                                   |
| deepcopy_reduce            | 2.93 us                                                                | 3.00 us: 1.02x slower                                                  |
| mako                       | 15.4 ms                                                                | 15.8 ms: 1.02x slower                                                  |
| logging_format             | 7.62 us                                                                | 7.83 us: 1.03x slower                                                  |
| async_generators           | 366 ms                                                                 | 376 ms: 1.03x slower                                                   |
| logging_silent             | 105 ns                                                                 | 108 ns: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 5.28 ms                                                                | 5.50 ms: 1.04x slower                                                  |
| pycparser                  | 1.11 sec                                                               | 1.17 sec: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (31): html5lib, bench_mp_pool, sphinx, dulwich_log, many_optionals, meteor_contest, unpickle_pure_python, sympy_sum, pprint_pformat, sympy_integrate, sqlglot_v2_transpile, scimark_sor, fannkuch, scimark_monte_carlo, asyncio_websockets, bench_thread_pool, 2to3, generators, sympy_expand, pylint, regex_compile, mdp, xml_etree_parse, tomli_loads, sqlglot_v2_optimize, async_tree_memoization, deltablue, logging_simple, async_tree_none, sqlglot_v2_parse, subparsers
Ignored benchmarks (8) of results/bm-20251122-3.15.0a2+-227b9d3-NOGIL/bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2+-227b9d3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 68.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x