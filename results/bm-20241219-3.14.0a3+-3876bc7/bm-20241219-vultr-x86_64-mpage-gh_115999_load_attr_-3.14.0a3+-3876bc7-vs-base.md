# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 3876bc7
- commit date: 2024-12-19
- overall geometric mean: 1.008x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 252 ms: 1.01x faster                                                  |
| docutils       | 2.54 sec                                                               | 2.53 sec: 1.00x faster                                                |
| sphinx         | 989 ms                                                                 | 980 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 22.2 ms                                                                | 21.4 ms: 1.04x faster                                                 |
| async_tree_io_tg           | 605 ms                                                                 | 613 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 600 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 582 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (7): async_tree_io, async_generators, asyncio_websockets, async_tree_none_tg, async_tree_memoization, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 91.1 ms                                                                | 88.6 ms: 1.03x faster                                                 |
| pidigits       | 217 ms                                                                 | 221 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 168 ms: 1.08x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 23.6 ms: 1.06x faster                                                 |
| regex_effbot   | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| regex_compile  | 127 ms                                                                 | 125 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 316 us                                                                 | 307 us: 1.03x faster                                                  |
| unpickle_pure_python | 213 us                                                                 | 208 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 90.6 ms                                                                | 90.0 ms: 1.01x faster                                                 |
| tomli_loads          | 1.90 sec                                                               | 1.89 sec: 1.01x faster                                                |
| xml_etree_generate   | 82.9 ms                                                                | 82.5 ms: 1.00x faster                                                 |
| xml_etree_process    | 57.9 ms                                                                | 57.6 ms: 1.00x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (3): json_dumps, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.4 ms                                                                | 20.9 ms: 1.02x faster                                                 |
| genshi_xml      | 48.9 ms                                                                | 48.0 ms: 1.02x faster                                                 |
| django_template | 34.7 ms                                                                | 34.2 ms: 1.01x faster                                                 |
| mako            | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                                | 4.03 ms: 1.09x faster                                                 |
| regex_dna                  | 181 ms                                                                 | 168 ms: 1.08x faster                                                  |
| regex_v8                   | 25.0 ms                                                                | 23.6 ms: 1.06x faster                                                 |
| coroutines                 | 22.2 ms                                                                | 21.4 ms: 1.04x faster                                                 |
| go                         | 116 ms                                                                 | 112 ms: 1.04x faster                                                  |
| generators                 | 27.1 ms                                                                | 26.3 ms: 1.03x faster                                                 |
| scimark_sor                | 117 ms                                                                 | 113 ms: 1.03x faster                                                  |
| pickle_pure_python         | 316 us                                                                 | 307 us: 1.03x faster                                                  |
| chaos                      | 58.9 ms                                                                | 57.2 ms: 1.03x faster                                                 |
| nbody                      | 91.1 ms                                                                | 88.6 ms: 1.03x faster                                                 |
| scimark_lu                 | 111 ms                                                                 | 108 ms: 1.03x faster                                                  |
| deltablue                  | 3.17 ms                                                                | 3.08 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 63.4 ms                                                                | 61.7 ms: 1.03x faster                                                 |
| raytrace                   | 260 ms                                                                 | 254 ms: 1.03x faster                                                  |
| scimark_fft                | 313 ms                                                                 | 305 ms: 1.03x faster                                                  |
| hexiom                     | 5.88 ms                                                                | 5.74 ms: 1.02x faster                                                 |
| genshi_text                | 21.4 ms                                                                | 20.9 ms: 1.02x faster                                                 |
| pyflate                    | 419 ms                                                                 | 410 ms: 1.02x faster                                                  |
| sqlglot_parse              | 1.26 ms                                                                | 1.23 ms: 1.02x faster                                                 |
| unpickle_pure_python       | 213 us                                                                 | 208 us: 1.02x faster                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| genshi_xml                 | 48.9 ms                                                                | 48.0 ms: 1.02x faster                                                 |
| deepcopy_memo              | 30.1 us                                                                | 29.6 us: 1.02x faster                                                 |
| sqlglot_transpile          | 1.56 ms                                                                | 1.54 ms: 1.02x faster                                                 |
| thrift                     | 739 us                                                                 | 728 us: 1.02x faster                                                  |
| bpe_tokeniser              | 4.28 sec                                                               | 4.22 sec: 1.02x faster                                                |
| richards_super             | 48.6 ms                                                                | 47.9 ms: 1.02x faster                                                 |
| pprint_safe_repr           | 704 ms                                                                 | 694 ms: 1.02x faster                                                  |
| comprehensions             | 17.0 us                                                                | 16.8 us: 1.02x faster                                                 |
| 2to3                       | 256 ms                                                                 | 252 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                                | 34.2 ms: 1.01x faster                                                 |
| pprint_pformat             | 1.44 sec                                                               | 1.42 sec: 1.01x faster                                                |
| regex_compile              | 127 ms                                                                 | 125 ms: 1.01x faster                                                  |
| logging_silent             | 106 ns                                                                 | 105 ns: 1.01x faster                                                  |
| pycparser                  | 1.11 sec                                                               | 1.10 sec: 1.01x faster                                                |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                                 |
| sphinx                     | 989 ms                                                                 | 980 ms: 1.01x faster                                                  |
| sympy_str                  | 272 ms                                                                 | 269 ms: 1.01x faster                                                  |
| sqlalchemy_declarative     | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| sympy_integrate            | 19.8 ms                                                                | 19.7 ms: 1.01x faster                                                 |
| json                       | 4.79 ms                                                                | 4.75 ms: 1.01x faster                                                 |
| shortest_path              | 433 ms                                                                 | 430 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 90.6 ms                                                                | 90.0 ms: 1.01x faster                                                 |
| connected_components       | 394 ms                                                                 | 392 ms: 1.01x faster                                                  |
| sympy_sum                  | 153 ms                                                                 | 152 ms: 1.01x faster                                                  |
| tomli_loads                | 1.90 sec                                                               | 1.89 sec: 1.01x faster                                                |
| xml_etree_generate         | 82.9 ms                                                                | 82.5 ms: 1.00x faster                                                 |
| xml_etree_process          | 57.9 ms                                                                | 57.6 ms: 1.00x faster                                                 |
| docutils                   | 2.54 sec                                                               | 2.53 sec: 1.00x faster                                                |
| dulwich_log                | 74.3 ms                                                                | 74.7 ms: 1.01x slower                                                 |
| pathlib                    | 17.9 ms                                                                | 18.0 ms: 1.01x slower                                                 |
| fannkuch                   | 365 ms                                                                 | 369 ms: 1.01x slower                                                  |
| mako                       | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                 |
| subparsers                 | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                 |
| async_tree_io_tg           | 605 ms                                                                 | 613 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 4.33 ms: 1.02x slower                                                 |
| pidigits                   | 217 ms                                                                 | 221 ms: 1.02x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 79.3 ms: 1.02x slower                                                 |
| spectral_norm              | 97.3 ms                                                                | 99.8 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 600 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 582 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (34): pylint, telco, create_gc_cycles, async_tree_io, typing_runtime_protocols, async_generators, richards, k_core, many_optionals, sympy_expand, json_dumps, json_loads, bench_thread_pool, sqlglot_normalize, mdp, coverage, python_startup_no_site, sqlglot_optimize, python_startup, bench_mp_pool, asyncio_websockets, deepcopy, crypto_pyaes, logging_format, meteor_contest, xml_etree_parse, async_tree_none_tg, async_tree_memoization, async_tree_none, async_tree_memoization_tg, logging_simple, deepcopy_reduce, float, sqlite_synth

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x