# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b868363
- commit date: 2024-12-20
- overall geometric mean: 1.008x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 253 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 22.2 ms                                                                | 21.0 ms: 1.06x faster                                                 |
| async_tree_io              | 624 ms                                                                 | 612 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 302 ms: 1.02x faster                                                  |
| async_generators           | 357 ms                                                                 | 353 ms: 1.01x faster                                                  |
| async_tree_memoization     | 332 ms                                                                 | 328 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 576 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 595 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (4): async_tree_none, async_tree_none_tg, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 91.1 ms                                                                | 88.1 ms: 1.03x faster                                                 |
| pidigits       | 217 ms                                                                 | 222 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 166 ms: 1.09x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 23.5 ms: 1.07x faster                                                 |
| regex_effbot   | 2.81 ms                                                                | 2.73 ms: 1.03x faster                                                 |
| regex_compile  | 127 ms                                                                 | 126 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 316 us                                                                 | 306 us: 1.03x faster                                                  |
| unpickle_pure_python | 213 us                                                                 | 209 us: 1.02x faster                                                  |
| json_loads           | 26.1 us                                                                | 25.8 us: 1.01x faster                                                 |
| xml_etree_process    | 57.9 ms                                                                | 57.3 ms: 1.01x faster                                                 |
| tomli_loads          | 1.90 sec                                                               | 1.88 sec: 1.01x faster                                                |
| json_dumps           | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| xml_etree_generate   | 82.9 ms                                                                | 82.4 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 90.6 ms                                                                | 90.2 ms: 1.00x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.48 ms                                                                | 7.46 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.4 ms                                                                | 21.1 ms: 1.01x faster                                                 |
| genshi_xml      | 48.9 ms                                                                | 48.5 ms: 1.01x faster                                                 |
| django_template | 34.7 ms                                                                | 34.4 ms: 1.01x faster                                                 |
| mako            | 11.5 ms                                                                | 11.5 ms: 1.00x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna                  | 181 ms                                                                 | 166 ms: 1.09x faster                                                  |
| regex_v8                   | 25.0 ms                                                                | 23.5 ms: 1.07x faster                                                 |
| coroutines                 | 22.2 ms                                                                | 21.0 ms: 1.06x faster                                                 |
| scimark_sor                | 117 ms                                                                 | 112 ms: 1.04x faster                                                  |
| nbody                      | 91.1 ms                                                                | 88.1 ms: 1.03x faster                                                 |
| deepcopy_memo              | 30.1 us                                                                | 29.1 us: 1.03x faster                                                 |
| pickle_pure_python         | 316 us                                                                 | 306 us: 1.03x faster                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.73 ms: 1.03x faster                                                 |
| chaos                      | 58.9 ms                                                                | 57.4 ms: 1.03x faster                                                 |
| spectral_norm              | 97.3 ms                                                                | 95.0 ms: 1.02x faster                                                 |
| scimark_fft                | 313 ms                                                                 | 306 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 157 us                                                                 | 154 us: 1.02x faster                                                  |
| scimark_monte_carlo        | 63.4 ms                                                                | 62.2 ms: 1.02x faster                                                 |
| pprint_safe_repr           | 704 ms                                                                 | 690 ms: 1.02x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 612 ms: 1.02x faster                                                  |
| gc_traversal               | 4.37 ms                                                                | 4.30 ms: 1.02x faster                                                 |
| hexiom                     | 5.88 ms                                                                | 5.78 ms: 1.02x faster                                                 |
| go                         | 116 ms                                                                 | 115 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 302 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 213 us                                                                 | 209 us: 1.02x faster                                                  |
| pprint_pformat             | 1.44 sec                                                               | 1.42 sec: 1.01x faster                                                |
| bpe_tokeniser              | 4.28 sec                                                               | 4.23 sec: 1.01x faster                                                |
| json_loads                 | 26.1 us                                                                | 25.8 us: 1.01x faster                                                 |
| genshi_text                | 21.4 ms                                                                | 21.1 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.5 ms                                                                | 66.7 ms: 1.01x faster                                                 |
| connected_components       | 394 ms                                                                 | 389 ms: 1.01x faster                                                  |
| deltablue                  | 3.17 ms                                                                | 3.13 ms: 1.01x faster                                                 |
| generators                 | 27.1 ms                                                                | 26.8 ms: 1.01x faster                                                 |
| async_generators           | 357 ms                                                                 | 353 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                                | 2.19 us: 1.01x faster                                                 |
| 2to3                       | 256 ms                                                                 | 253 ms: 1.01x faster                                                  |
| xml_etree_process          | 57.9 ms                                                                | 57.3 ms: 1.01x faster                                                 |
| async_tree_memoization     | 332 ms                                                                 | 328 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.9 ms                                                                | 48.5 ms: 1.01x faster                                                 |
| sqlglot_parse              | 1.26 ms                                                                | 1.25 ms: 1.01x faster                                                 |
| deepcopy_reduce            | 2.57 us                                                                | 2.55 us: 1.01x faster                                                 |
| tomli_loads                | 1.90 sec                                                               | 1.88 sec: 1.01x faster                                                |
| subparsers                 | 21.6 ms                                                                | 21.4 ms: 1.01x faster                                                 |
| django_template            | 34.7 ms                                                                | 34.4 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 4.23 ms: 1.01x faster                                                 |
| sqlglot_normalize          | 103 ms                                                                 | 102 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                                | 1.55 ms: 1.01x faster                                                 |
| json_dumps                 | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| raytrace                   | 260 ms                                                                 | 259 ms: 1.01x faster                                                  |
| regex_compile              | 127 ms                                                                 | 126 ms: 1.01x faster                                                  |
| pycparser                  | 1.11 sec                                                               | 1.11 sec: 1.01x faster                                                |
| sqlglot_optimize           | 52.0 ms                                                                | 51.7 ms: 1.01x faster                                                 |
| xml_etree_generate         | 82.9 ms                                                                | 82.4 ms: 1.01x faster                                                 |
| sympy_str                  | 272 ms                                                                 | 270 ms: 1.00x faster                                                  |
| deepcopy                   | 253 us                                                                 | 252 us: 1.00x faster                                                  |
| xml_etree_iterparse        | 90.6 ms                                                                | 90.2 ms: 1.00x faster                                                 |
| sympy_integrate            | 19.8 ms                                                                | 19.8 ms: 1.00x faster                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.00x faster                                                 |
| python_startup_no_site     | 7.48 ms                                                                | 7.46 ms: 1.00x faster                                                 |
| mako                       | 11.5 ms                                                                | 11.5 ms: 1.00x slower                                                 |
| fannkuch                   | 365 ms                                                                 | 368 ms: 1.01x slower                                                  |
| dulwich_log                | 74.3 ms                                                                | 75.0 ms: 1.01x slower                                                 |
| richards                   | 42.3 ms                                                                | 42.7 ms: 1.01x slower                                                 |
| comprehensions             | 17.0 us                                                                | 17.2 us: 1.01x slower                                                 |
| logging_simple             | 5.95 us                                                                | 6.02 us: 1.01x slower                                                 |
| pidigits                   | 217 ms                                                                 | 222 ms: 1.02x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.44 sec: 1.04x slower                                                |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 576 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 595 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (31): async_tree_none, pylint, async_tree_none_tg, telco, thrift, json, k_core, sphinx, scimark_lu, logging_format, shortest_path, xml_etree_parse, sqlalchemy_declarative, bench_mp_pool, many_optionals, sqlalchemy_imperative, create_gc_cycles, coverage, sympy_expand, pyflate, sympy_sum, docutils, pathlib, meteor_contest, asyncio_websockets, async_tree_io_tg, python_startup, float, richards_super, nqueens, logging_silent

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x