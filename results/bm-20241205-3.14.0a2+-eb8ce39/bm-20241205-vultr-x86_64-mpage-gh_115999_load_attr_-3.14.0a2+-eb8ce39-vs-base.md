# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: eb8ce39
- commit date: 2024-12-05
- overall geometric mean: 1.005x faster
- HPT reliability: 81.34%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 258 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 487 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 505 ms: 1.20x faster                                                  |
| async_generators           | 370 ms                                                                 | 364 ms: 1.02x faster                                                  |
| coroutines                 | 21.9 ms                                                                | 22.5 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (7): async_tree_memoization_tg, asyncio_websockets, async_tree_none, async_tree_none_tg, async_tree_memoization, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 185 ms: 1.20x faster                                                  |
| float          | 78.6 ms                                                                | 77.7 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.74 ms                                                                | 2.77 ms: 1.01x slower                                                 |
| regex_dna      | 169 ms                                                                 | 175 ms: 1.03x slower                                                  |
| regex_v8       | 23.3 ms                                                                | 24.8 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 11.5 ms                                                                | 11.3 ms: 1.02x faster                                                 |
| json_loads           | 25.1 us                                                                | 24.8 us: 1.01x faster                                                 |
| unpickle_pure_python | 216 us                                                                 | 213 us: 1.01x faster                                                  |
| pickle_pure_python   | 316 us                                                                 | 314 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 92.1 ms                                                                | 91.7 ms: 1.00x faster                                                 |
| tomli_loads          | 2.11 sec                                                               | 2.12 sec: 1.00x slower                                                |
| xml_etree_generate   | 85.1 ms                                                                | 86.0 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.43 ms                                                                | 7.46 ms: 1.00x slower                                                 |
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| genshi_xml      | 51.2 ms                                                                | 50.8 ms: 1.01x faster                                                 |
| django_template | 35.6 ms                                                                | 35.9 ms: 1.01x slower                                                 |
| mako            | 11.5 ms                                                                | 11.7 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 487 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 505 ms: 1.20x faster                                                  |
| pidigits                   | 222 ms                                                                 | 185 ms: 1.20x faster                                                  |
| chaos                      | 60.1 ms                                                                | 58.6 ms: 1.03x faster                                                 |
| hexiom                     | 5.99 ms                                                                | 5.87 ms: 1.02x faster                                                 |
| richards                   | 46.7 ms                                                                | 45.8 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.28 us                                                                | 2.24 us: 1.02x faster                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.0 ms: 1.02x faster                                                 |
| logging_format             | 7.04 us                                                                | 6.92 us: 1.02x faster                                                 |
| async_generators           | 370 ms                                                                 | 364 ms: 1.02x faster                                                  |
| json_dumps                 | 11.5 ms                                                                | 11.3 ms: 1.02x faster                                                 |
| richards_super             | 52.7 ms                                                                | 51.9 ms: 1.01x faster                                                 |
| json_loads                 | 25.1 us                                                                | 24.8 us: 1.01x faster                                                 |
| crypto_pyaes               | 68.1 ms                                                                | 67.3 ms: 1.01x faster                                                 |
| typing_runtime_protocols   | 161 us                                                                 | 159 us: 1.01x faster                                                  |
| unpickle_pure_python       | 216 us                                                                 | 213 us: 1.01x faster                                                  |
| deepcopy_memo              | 30.7 us                                                                | 30.3 us: 1.01x faster                                                 |
| float                      | 78.6 ms                                                                | 77.7 ms: 1.01x faster                                                 |
| genshi_text                | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| shortest_path              | 444 ms                                                                 | 439 ms: 1.01x faster                                                  |
| logging_simple             | 6.27 us                                                                | 6.22 us: 1.01x faster                                                 |
| deltablue                  | 3.25 ms                                                                | 3.23 ms: 1.01x faster                                                 |
| pickle_pure_python         | 316 us                                                                 | 314 us: 1.01x faster                                                  |
| go                         | 120 ms                                                                 | 119 ms: 1.01x faster                                                  |
| genshi_xml                 | 51.2 ms                                                                | 50.8 ms: 1.01x faster                                                 |
| coverage                   | 79.8 ms                                                                | 79.3 ms: 1.01x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 374 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 92.1 ms                                                                | 91.7 ms: 1.00x faster                                                 |
| sympy_integrate            | 20.1 ms                                                                | 20.0 ms: 1.00x faster                                                 |
| sqlglot_optimize           | 53.6 ms                                                                | 53.7 ms: 1.00x slower                                                 |
| 2to3                       | 257 ms                                                                 | 258 ms: 1.00x slower                                                  |
| mdp                        | 2.35 sec                                                               | 2.36 sec: 1.00x slower                                                |
| python_startup_no_site     | 7.43 ms                                                                | 7.46 ms: 1.00x slower                                                 |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                 |
| sqlalchemy_declarative     | 127 ms                                                                 | 127 ms: 1.00x slower                                                  |
| bench_mp_pool              | 88.5 ms                                                                | 88.9 ms: 1.00x slower                                                 |
| tomli_loads                | 2.11 sec                                                               | 2.12 sec: 1.00x slower                                                |
| scimark_sor                | 133 ms                                                                 | 133 ms: 1.00x slower                                                  |
| pprint_safe_repr           | 715 ms                                                                 | 719 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 107 ms                                                                 | 108 ms: 1.01x slower                                                  |
| gc_traversal               | 4.58 ms                                                                | 4.61 ms: 1.01x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.01x slower                                                  |
| subparsers                 | 22.1 ms                                                                | 22.2 ms: 1.01x slower                                                 |
| meteor_contest             | 99.1 ms                                                                | 99.8 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.45 sec                                                               | 1.47 sec: 1.01x slower                                                |
| django_template            | 35.6 ms                                                                | 35.9 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.1 ms                                                                | 86.0 ms: 1.01x slower                                                 |
| pathlib                    | 18.2 ms                                                                | 18.4 ms: 1.01x slower                                                 |
| regex_effbot               | 2.74 ms                                                                | 2.77 ms: 1.01x slower                                                 |
| bench_thread_pool          | 1.02 ms                                                                | 1.03 ms: 1.01x slower                                                 |
| pycparser                  | 1.13 sec                                                               | 1.14 sec: 1.01x slower                                                |
| sympy_expand               | 460 ms                                                                 | 466 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.83 ms                                                                | 1.85 ms: 1.01x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 111 ms: 1.01x slower                                                  |
| mako                       | 11.5 ms                                                                | 11.7 ms: 1.02x slower                                                 |
| spectral_norm              | 107 ms                                                                 | 109 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.57 ms                                                                | 4.66 ms: 1.02x slower                                                 |
| scimark_fft                | 340 ms                                                                 | 346 ms: 1.02x slower                                                  |
| coroutines                 | 21.9 ms                                                                | 22.5 ms: 1.02x slower                                                 |
| thrift                     | 736 us                                                                 | 755 us: 1.03x slower                                                  |
| telco                      | 7.19 ms                                                                | 7.41 ms: 1.03x slower                                                 |
| regex_dna                  | 169 ms                                                                 | 175 ms: 1.03x slower                                                  |
| regex_v8                   | 23.3 ms                                                                | 24.8 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (32): scimark_monte_carlo, nbody, connected_components, sympy_str, k_core, xml_etree_process, generators, xml_etree_parse, dulwich_log, logging_silent, nqueens, deepcopy, async_tree_memoization_tg, docutils, pyflate, asyncio_websockets, regex_compile, sqlglot_parse, many_optionals, comprehensions, bpe_tokeniser, raytrace, pylint, async_tree_none, async_tree_none_tg, sphinx, sqlglot_transpile, json, async_tree_memoization, deepcopy_reduce, async_tree_io, async_tree_io_tg

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 81.34% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x