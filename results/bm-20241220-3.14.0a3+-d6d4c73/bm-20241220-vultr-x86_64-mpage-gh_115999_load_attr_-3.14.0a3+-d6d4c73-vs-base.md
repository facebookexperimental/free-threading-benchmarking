# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.011x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 254 ms: 1.01x faster                                                  |
| sphinx         | 989 ms                                                                 | 980 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 475 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 491 ms: 1.15x faster                                                  |
| coroutines                 | 22.2 ms                                                                | 21.7 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 307 ms                                                                 | 302 ms: 1.01x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 616 ms: 1.01x faster                                                  |
| async_tree_none_tg         | 254 ms                                                                 | 252 ms: 1.01x faster                                                  |
| async_tree_memoization     | 332 ms                                                                 | 328 ms: 1.01x faster                                                  |
| async_generators           | 357 ms                                                                 | 355 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): async_tree_none, async_tree_io_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 185 ms: 1.17x faster                                                  |
| nbody          | 91.1 ms                                                                | 89.9 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 166 ms: 1.09x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| regex_effbot   | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 316 us                                                                 | 308 us: 1.03x faster                                                  |
| unpickle_pure_python | 213 us                                                                 | 210 us: 1.01x faster                                                  |
| json_loads           | 26.1 us                                                                | 25.9 us: 1.01x faster                                                 |
| xml_etree_iterparse  | 90.6 ms                                                                | 90.3 ms: 1.00x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (5): tomli_loads, json_dumps, xml_etree_process, xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.48 ms                                                                | 7.44 ms: 1.00x faster                                                 |
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.4 ms                                                                | 21.1 ms: 1.02x faster                                                 |
| genshi_xml     | 48.9 ms                                                                | 48.6 ms: 1.01x faster                                                 |
| mako           | 11.5 ms                                                                | 11.7 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                                 | 185 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 475 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 491 ms: 1.15x faster                                                  |
| regex_dna                  | 181 ms                                                                 | 166 ms: 1.09x faster                                                  |
| regex_v8                   | 25.0 ms                                                                | 23.2 ms: 1.08x faster                                                 |
| gc_traversal               | 4.37 ms                                                                | 4.17 ms: 1.05x faster                                                 |
| logging_silent             | 106 ns                                                                 | 102 ns: 1.04x faster                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                                 |
| scimark_sor                | 117 ms                                                                 | 113 ms: 1.03x faster                                                  |
| spectral_norm              | 97.3 ms                                                                | 94.5 ms: 1.03x faster                                                 |
| pickle_pure_python         | 316 us                                                                 | 308 us: 1.03x faster                                                  |
| deltablue                  | 3.17 ms                                                                | 3.09 ms: 1.03x faster                                                 |
| coroutines                 | 22.2 ms                                                                | 21.7 ms: 1.03x faster                                                 |
| go                         | 116 ms                                                                 | 114 ms: 1.03x faster                                                  |
| hexiom                     | 5.88 ms                                                                | 5.77 ms: 1.02x faster                                                 |
| telco                      | 7.25 ms                                                                | 7.12 ms: 1.02x faster                                                 |
| genshi_text                | 21.4 ms                                                                | 21.1 ms: 1.02x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.82 ms: 1.02x faster                                                 |
| bpe_tokeniser              | 4.28 sec                                                               | 4.22 sec: 1.02x faster                                                |
| async_tree_memoization_tg  | 307 ms                                                                 | 302 ms: 1.01x faster                                                  |
| scimark_fft                | 313 ms                                                                 | 309 ms: 1.01x faster                                                  |
| nbody                      | 91.1 ms                                                                | 89.9 ms: 1.01x faster                                                 |
| chaos                      | 58.9 ms                                                                | 58.1 ms: 1.01x faster                                                 |
| deepcopy_memo              | 30.1 us                                                                | 29.8 us: 1.01x faster                                                 |
| async_tree_io              | 624 ms                                                                 | 616 ms: 1.01x faster                                                  |
| sympy_expand               | 456 ms                                                                 | 451 ms: 1.01x faster                                                  |
| async_tree_none_tg         | 254 ms                                                                 | 252 ms: 1.01x faster                                                  |
| async_tree_memoization     | 332 ms                                                                 | 328 ms: 1.01x faster                                                  |
| scimark_monte_carlo        | 63.4 ms                                                                | 62.8 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 213 us                                                                 | 210 us: 1.01x faster                                                  |
| json                       | 4.79 ms                                                                | 4.74 ms: 1.01x faster                                                 |
| json_loads                 | 26.1 us                                                                | 25.9 us: 1.01x faster                                                 |
| pyflate                    | 419 ms                                                                 | 415 ms: 1.01x faster                                                  |
| sphinx                     | 989 ms                                                                 | 980 ms: 1.01x faster                                                  |
| generators                 | 27.1 ms                                                                | 26.9 ms: 1.01x faster                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                                 |
| 2to3                       | 256 ms                                                                 | 254 ms: 1.01x faster                                                  |
| shortest_path              | 433 ms                                                                 | 430 ms: 1.01x faster                                                  |
| fannkuch                   | 365 ms                                                                 | 362 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.5 ms                                                                | 67.0 ms: 1.01x faster                                                 |
| richards_super             | 48.6 ms                                                                | 48.3 ms: 1.01x faster                                                 |
| genshi_xml                 | 48.9 ms                                                                | 48.6 ms: 1.01x faster                                                 |
| comprehensions             | 17.0 us                                                                | 16.9 us: 1.01x faster                                                 |
| async_generators           | 357 ms                                                                 | 355 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.48 ms                                                                | 7.44 ms: 1.00x faster                                                 |
| sqlalchemy_declarative     | 128 ms                                                                 | 128 ms: 1.00x faster                                                  |
| sqlglot_optimize           | 52.0 ms                                                                | 51.8 ms: 1.00x faster                                                 |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                 |
| xml_etree_iterparse        | 90.6 ms                                                                | 90.3 ms: 1.00x faster                                                 |
| deepcopy                   | 253 us                                                                 | 255 us: 1.01x slower                                                  |
| pprint_safe_repr           | 704 ms                                                                 | 710 ms: 1.01x slower                                                  |
| scimark_lu                 | 111 ms                                                                 | 112 ms: 1.01x slower                                                  |
| subparsers                 | 21.6 ms                                                                | 21.8 ms: 1.01x slower                                                 |
| dulwich_log                | 74.3 ms                                                                | 75.1 ms: 1.01x slower                                                 |
| pathlib                    | 17.9 ms                                                                | 18.1 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.44 sec                                                               | 1.46 sec: 1.01x slower                                                |
| mako                       | 11.5 ms                                                                | 11.7 ms: 1.01x slower                                                 |
| logging_simple             | 5.95 us                                                                | 6.03 us: 1.01x slower                                                 |
| logging_format             | 6.63 us                                                                | 6.74 us: 1.02x slower                                                 |
| deepcopy_reduce            | 2.57 us                                                                | 2.64 us: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 4.45 ms: 1.04x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.45 sec: 1.05x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (33): async_tree_none, k_core, pylint, float, async_tree_io_tg, tomli_loads, json_dumps, xml_etree_process, regex_compile, connected_components, meteor_contest, sqlglot_normalize, bench_thread_pool, sqlglot_parse, sympy_integrate, raytrace, docutils, pycparser, thrift, django_template, bench_mp_pool, asyncio_websockets, nqueens, many_optionals, sympy_str, coverage, sympy_sum, richards, sqlglot_transpile, xml_etree_parse, sqlite_synth, typing_runtime_protocols, xml_etree_generate

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x