# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 39cab3f
- commit date: 2024-12-12
- overall geometric mean: 1.004x slower
- HPT reliability: 98.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 253 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 617 ms                                                                 | 606 ms: 1.02x faster                                                  |
| async_tree_io              | 631 ms                                                                 | 619 ms: 1.02x faster                                                  |
| async_tree_memoization     | 337 ms                                                                 | 332 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 309 ms                                                                 | 305 ms: 1.01x faster                                                  |
| async_tree_none            | 280 ms                                                                 | 276 ms: 1.01x faster                                                  |
| coroutines                 | 21.3 ms                                                                | 21.4 ms: 1.01x slower                                                 |
| async_generators           | 359 ms                                                                 | 362 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 504 ms                                                                 | 599 ms: 1.19x slower                                                  |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 580 ms: 1.20x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (2): async_tree_none_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 90.7 ms                                                                | 89.8 ms: 1.01x faster                                                 |
| pidigits       | 186 ms                                                                 | 225 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 172 ms                                                                 | 168 ms: 1.02x faster                                                  |
| regex_v8       | 23.5 ms                                                                | 23.0 ms: 1.02x faster                                                 |
| regex_effbot   | 2.78 ms                                                                | 2.73 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark         | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|-------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads        | 26.6 us                                                                | 25.9 us: 1.03x faster                                                 |
| json_dumps        | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| xml_etree_parse   | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| xml_etree_process | 58.0 ms                                                                | 58.8 ms: 1.01x slower                                                 |
| Geometric mean    | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (5): tomli_loads, unpickle_pure_python, pickle_pure_python, xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.0 ms                                                                | 21.3 ms: 1.03x faster                                                 |
| genshi_xml      | 50.5 ms                                                                | 49.5 ms: 1.02x faster                                                 |
| mako            | 11.5 ms                                                                | 11.4 ms: 1.01x faster                                                 |
| django_template | 35.4 ms                                                                | 35.3 ms: 1.00x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2+-487fdbe | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text                | 22.0 ms                                                                | 21.3 ms: 1.03x faster                                                 |
| deepcopy_memo              | 30.1 us                                                                | 29.2 us: 1.03x faster                                                 |
| subparsers                 | 22.4 ms                                                                | 21.8 ms: 1.03x faster                                                 |
| json_loads                 | 26.6 us                                                                | 25.9 us: 1.03x faster                                                 |
| regex_dna                  | 172 ms                                                                 | 168 ms: 1.02x faster                                                  |
| regex_v8                   | 23.5 ms                                                                | 23.0 ms: 1.02x faster                                                 |
| genshi_xml                 | 50.5 ms                                                                | 49.5 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                                 | 99.5 ms: 1.02x faster                                                 |
| async_tree_io_tg           | 617 ms                                                                 | 606 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 2.59 us                                                                | 2.54 us: 1.02x faster                                                 |
| json                       | 4.82 ms                                                                | 4.73 ms: 1.02x faster                                                 |
| async_tree_io              | 631 ms                                                                 | 619 ms: 1.02x faster                                                  |
| regex_effbot               | 2.78 ms                                                                | 2.73 ms: 1.02x faster                                                 |
| async_tree_memoization     | 337 ms                                                                 | 332 ms: 1.02x faster                                                  |
| deepcopy                   | 255 us                                                                 | 251 us: 1.02x faster                                                  |
| logging_format             | 6.78 us                                                                | 6.68 us: 1.01x faster                                                 |
| async_tree_memoization_tg  | 309 ms                                                                 | 305 ms: 1.01x faster                                                  |
| mako                       | 11.5 ms                                                                | 11.4 ms: 1.01x faster                                                 |
| async_tree_none            | 280 ms                                                                 | 276 ms: 1.01x faster                                                  |
| thrift                     | 742 us                                                                 | 733 us: 1.01x faster                                                  |
| pprint_pformat             | 1.45 sec                                                               | 1.43 sec: 1.01x faster                                                |
| typing_runtime_protocols   | 157 us                                                                 | 155 us: 1.01x faster                                                  |
| telco                      | 7.25 ms                                                                | 7.17 ms: 1.01x faster                                                 |
| nbody                      | 90.7 ms                                                                | 89.8 ms: 1.01x faster                                                 |
| json_dumps                 | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| comprehensions             | 17.2 us                                                                | 17.0 us: 1.01x faster                                                 |
| crypto_pyaes               | 67.6 ms                                                                | 67.1 ms: 1.01x faster                                                 |
| shortest_path              | 440 ms                                                                 | 437 ms: 1.01x faster                                                  |
| go                         | 119 ms                                                                 | 118 ms: 1.01x faster                                                  |
| django_template            | 35.4 ms                                                                | 35.3 ms: 1.00x faster                                                 |
| fannkuch                   | 374 ms                                                                 | 372 ms: 1.00x faster                                                  |
| 2to3                       | 254 ms                                                                 | 253 ms: 1.00x faster                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 126 ms: 1.00x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 19.7 ms: 1.00x faster                                                 |
| bpe_tokeniser              | 4.22 sec                                                               | 4.21 sec: 1.00x faster                                                |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                 |
| sqlglot_parse              | 1.26 ms                                                                | 1.26 ms: 1.00x slower                                                 |
| chaos                      | 57.5 ms                                                                | 57.7 ms: 1.00x slower                                                 |
| sqlglot_optimize           | 51.9 ms                                                                | 52.2 ms: 1.00x slower                                                 |
| deltablue                  | 3.21 ms                                                                | 3.22 ms: 1.00x slower                                                 |
| coroutines                 | 21.3 ms                                                                | 21.4 ms: 1.01x slower                                                 |
| sqlglot_normalize          | 103 ms                                                                 | 103 ms: 1.01x slower                                                  |
| scimark_sor                | 130 ms                                                                 | 131 ms: 1.01x slower                                                  |
| logging_silent             | 104 ns                                                                 | 105 ns: 1.01x slower                                                  |
| scimark_fft                | 327 ms                                                                 | 330 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.82 ms                                                                | 1.84 ms: 1.01x slower                                                 |
| async_generators           | 359 ms                                                                 | 362 ms: 1.01x slower                                                  |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                                | 2.23 us: 1.01x slower                                                 |
| pathlib                    | 18.1 ms                                                                | 18.3 ms: 1.01x slower                                                 |
| raytrace                   | 258 ms                                                                 | 261 ms: 1.01x slower                                                  |
| xml_etree_process          | 58.0 ms                                                                | 58.8 ms: 1.01x slower                                                 |
| pyflate                    | 435 ms                                                                 | 442 ms: 1.02x slower                                                  |
| hexiom                     | 5.77 ms                                                                | 5.87 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.40 ms                                                                | 4.48 ms: 1.02x slower                                                 |
| scimark_lu                 | 108 ms                                                                 | 111 ms: 1.03x slower                                                  |
| gc_traversal               | 3.97 ms                                                                | 4.21 ms: 1.06x slower                                                 |
| async_tree_cpu_io_mixed    | 504 ms                                                                 | 599 ms: 1.19x slower                                                  |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 580 ms: 1.20x slower                                                  |
| pidigits                   | 186 ms                                                                 | 225 ms: 1.21x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (35): async_tree_none_tg, k_core, sympy_expand, richards, sqlalchemy_imperative, connected_components, sphinx, docutils, logging_simple, richards_super, bench_mp_pool, pprint_safe_repr, pycparser, coverage, tomli_loads, sympy_str, unpickle_pure_python, sympy_sum, pylint, many_optionals, pickle_pure_python, python_startup_no_site, nqueens, asyncio_websockets, sqlglot_transpile, regex_compile, mdp, float, xml_etree_iterparse, spectral_norm, scimark_monte_carlo, dulwich_log, bench_thread_pool, xml_etree_generate, generators

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 98.80% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x