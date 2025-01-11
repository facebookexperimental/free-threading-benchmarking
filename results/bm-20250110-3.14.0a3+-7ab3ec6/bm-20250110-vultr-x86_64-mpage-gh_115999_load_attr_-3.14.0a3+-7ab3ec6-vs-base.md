# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 7ab3ec6
- commit date: 2025-01-10
- overall geometric mean: 1.000x faster
- HPT reliability: 59.69%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 253 ms: 1.00x slower                                                  |
| docutils       | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization    | 324 ms                                                                 | 320 ms: 1.01x faster                                                  |
| async_tree_memoization_tg | 300 ms                                                                 | 297 ms: 1.01x faster                                                  |
| async_tree_none_tg        | 252 ms                                                                 | 250 ms: 1.01x faster                                                  |
| coroutines                | 21.0 ms                                                                | 21.1 ms: 1.00x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_none, async_tree_io_tg, async_generators, async_tree_io, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 89.9 ms                                                                | 88.2 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 179 ms: 1.01x faster                                                  |
| regex_effbot   | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                 |
| regex_v8       | 24.4 ms                                                                | 24.3 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 25.8 us                                                                | 25.6 us: 1.01x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| pickle_pure_python   | 303 us                                                                 | 305 us: 1.01x slower                                                  |
| xml_etree_generate   | 82.5 ms                                                                | 83.1 ms: 1.01x slower                                                 |
| unpickle_pure_python | 209 us                                                                 | 211 us: 1.01x slower                                                  |
| xml_etree_process    | 56.9 ms                                                                | 57.5 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): tomli_loads, xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.48 ms                                                                | 7.48 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 11.6 ms                                                                | 11.4 ms: 1.02x faster                                                 |
| genshi_xml     | 48.7 ms                                                                | 48.3 ms: 1.01x faster                                                 |
| genshi_text    | 21.0 ms                                                                | 21.1 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                 | bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3+-1b39b50 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal              | 4.39 ms                                                                | 4.20 ms: 1.05x faster                                                 |
| logging_simple            | 6.11 us                                                                | 5.95 us: 1.03x faster                                                 |
| mako                      | 11.6 ms                                                                | 11.4 ms: 1.02x faster                                                 |
| nbody                     | 89.9 ms                                                                | 88.2 ms: 1.02x faster                                                 |
| generators                | 27.4 ms                                                                | 26.9 ms: 1.02x faster                                                 |
| sqlite_synth              | 2.20 us                                                                | 2.16 us: 1.02x faster                                                 |
| regex_dna                 | 182 ms                                                                 | 179 ms: 1.01x faster                                                  |
| async_tree_memoization    | 324 ms                                                                 | 320 ms: 1.01x faster                                                  |
| async_tree_memoization_tg | 300 ms                                                                 | 297 ms: 1.01x faster                                                  |
| logging_format            | 6.85 us                                                                | 6.77 us: 1.01x faster                                                 |
| regex_effbot              | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                 |
| json                      | 4.73 ms                                                                | 4.68 ms: 1.01x faster                                                 |
| logging_silent            | 104 ns                                                                 | 103 ns: 1.01x faster                                                  |
| async_tree_none_tg        | 252 ms                                                                 | 250 ms: 1.01x faster                                                  |
| json_loads                | 25.8 us                                                                | 25.6 us: 1.01x faster                                                 |
| spectral_norm             | 102 ms                                                                 | 101 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult   | 4.42 ms                                                                | 4.37 ms: 1.01x faster                                                 |
| create_gc_cycles          | 1.85 ms                                                                | 1.84 ms: 1.01x faster                                                 |
| xml_etree_parse           | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| deepcopy_memo             | 29.7 us                                                                | 29.4 us: 1.01x faster                                                 |
| dulwich_log               | 75.0 ms                                                                | 74.4 ms: 1.01x faster                                                 |
| genshi_xml                | 48.7 ms                                                                | 48.3 ms: 1.01x faster                                                 |
| deltablue                 | 3.12 ms                                                                | 3.11 ms: 1.01x faster                                                 |
| regex_v8                  | 24.4 ms                                                                | 24.3 ms: 1.00x faster                                                 |
| raytrace                  | 256 ms                                                                 | 255 ms: 1.00x faster                                                  |
| python_startup_no_site    | 7.48 ms                                                                | 7.48 ms: 1.00x slower                                                 |
| bpe_tokeniser             | 4.23 sec                                                               | 4.24 sec: 1.00x slower                                                |
| coroutines                | 21.0 ms                                                                | 21.1 ms: 1.00x slower                                                 |
| coverage                  | 79.1 ms                                                                | 79.4 ms: 1.00x slower                                                 |
| 2to3                      | 252 ms                                                                 | 253 ms: 1.00x slower                                                  |
| sqlglot_optimize          | 51.8 ms                                                                | 52.1 ms: 1.01x slower                                                 |
| scimark_monte_carlo       | 61.7 ms                                                                | 62.1 ms: 1.01x slower                                                 |
| richards                  | 41.7 ms                                                                | 42.0 ms: 1.01x slower                                                 |
| mdp                       | 2.30 sec                                                               | 2.31 sec: 1.01x slower                                                |
| pickle_pure_python        | 303 us                                                                 | 305 us: 1.01x slower                                                  |
| xml_etree_generate        | 82.5 ms                                                                | 83.1 ms: 1.01x slower                                                 |
| docutils                  | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                |
| genshi_text               | 21.0 ms                                                                | 21.1 ms: 1.01x slower                                                 |
| sqlglot_normalize         | 102 ms                                                                 | 103 ms: 1.01x slower                                                  |
| pyflate                   | 413 ms                                                                 | 417 ms: 1.01x slower                                                  |
| unpickle_pure_python      | 209 us                                                                 | 211 us: 1.01x slower                                                  |
| xml_etree_process         | 56.9 ms                                                                | 57.5 ms: 1.01x slower                                                 |
| pathlib                   | 17.8 ms                                                                | 18.0 ms: 1.01x slower                                                 |
| sympy_integrate           | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                                 |
| hexiom                    | 5.69 ms                                                                | 5.76 ms: 1.01x slower                                                 |
| telco                     | 7.20 ms                                                                | 7.29 ms: 1.01x slower                                                 |
| pprint_pformat            | 1.39 sec                                                               | 1.41 sec: 1.01x slower                                                |
| pprint_safe_repr          | 682 ms                                                                 | 691 ms: 1.01x slower                                                  |
| thrift                    | 725 us                                                                 | 735 us: 1.01x slower                                                  |
| go                        | 113 ms                                                                 | 115 ms: 1.01x slower                                                  |
| crypto_pyaes              | 64.9 ms                                                                | 65.9 ms: 1.02x slower                                                 |
| subparsers                | 21.5 ms                                                                | 21.9 ms: 1.02x slower                                                 |
| fannkuch                  | 364 ms                                                                 | 377 ms: 1.04x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (42): k_core, async_tree_cpu_io_mixed, async_tree_none, async_tree_io_tg, shortest_path, async_generators, async_tree_io, typing_runtime_protocols, sqlalchemy_imperative, bench_thread_pool, sympy_expand, pycparser, nqueens, sqlalchemy_declarative, connected_components, pidigits, async_tree_cpu_io_mixed_tg, float, bench_mp_pool, asyncio_websockets, tomli_loads, comprehensions, sqlglot_parse, pylint, deepcopy, sqlglot_transpile, xml_etree_iterparse, python_startup, meteor_contest, chaos, regex_compile, deepcopy_reduce, scimark_lu, scimark_fft, richards_super, many_optionals, json_dumps, sympy_sum, sympy_str, django_template, sphinx, scimark_sor

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 59.69% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x