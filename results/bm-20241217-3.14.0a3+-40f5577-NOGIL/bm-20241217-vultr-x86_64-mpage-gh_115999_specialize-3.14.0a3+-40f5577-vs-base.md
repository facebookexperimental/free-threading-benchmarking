# Results vs. base

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 40f5577
- commit date: 2024-12-17
- overall geometric mean: 1.027x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 364 ms                                                                 | 360 ms: 1.01x faster                                                  |
| html5lib       | 96.0 ms                                                                | 94.1 ms: 1.02x faster                                                 |
| sphinx         | 1.17 sec                                                               | 1.16 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 793 ms                                                                 | 732 ms: 1.08x faster                                                  |
| async_tree_none_tg         | 349 ms                                                                 | 323 ms: 1.08x faster                                                  |
| async_tree_memoization     | 464 ms                                                                 | 430 ms: 1.08x faster                                                  |
| async_tree_memoization_tg  | 434 ms                                                                 | 405 ms: 1.07x faster                                                  |
| async_tree_io              | 809 ms                                                                 | 760 ms: 1.07x faster                                                  |
| async_tree_none            | 376 ms                                                                 | 356 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 605 ms                                                                 | 579 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed    | 624 ms                                                                 | 600 ms: 1.04x faster                                                  |
| coroutines                 | 24.5 ms                                                                | 24.1 ms: 1.02x faster                                                 |
| async_generators           | 452 ms                                                                 | 448 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 132 ms                                                                 | 111 ms: 1.19x faster                                                  |
| pidigits       | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| nbody          | 127 ms                                                                 | 125 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 175 ms                                                                 | 170 ms: 1.03x faster                                                  |
| regex_v8       | 24.8 ms                                                                | 25.2 ms: 1.02x slower                                                 |
| regex_dna      | 179 ms                                                                 | 187 ms: 1.05x slower                                                  |
| regex_effbot   | 2.82 ms                                                                | 2.98 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_process    | 78.1 ms                                                                | 73.9 ms: 1.06x faster                                                 |
| unpickle_pure_python | 339 us                                                                 | 327 us: 1.04x faster                                                  |
| tomli_loads          | 2.55 sec                                                               | 2.53 sec: 1.01x faster                                                |
| pickle_pure_python   | 507 us                                                                 | 504 us: 1.01x faster                                                  |
| json_loads           | 28.5 us                                                                | 28.4 us: 1.00x faster                                                 |
| xml_etree_iterparse  | 89.4 ms                                                                | 90.2 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 17.1 ms                                                                | 17.1 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): django_template, genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float                      | 132 ms                                                                 | 111 ms: 1.19x faster                                                  |
| scimark_monte_carlo        | 118 ms                                                                 | 105 ms: 1.12x faster                                                  |
| richards                   | 77.0 ms                                                                | 68.9 ms: 1.12x faster                                                 |
| thrift                     | 1.09 ms                                                                | 987 us: 1.11x faster                                                  |
| richards_super             | 85.6 ms                                                                | 77.5 ms: 1.11x faster                                                 |
| logging_simple             | 10.0 us                                                                | 9.08 us: 1.11x faster                                                 |
| raytrace                   | 548 ms                                                                 | 498 ms: 1.10x faster                                                  |
| go                         | 266 ms                                                                 | 243 ms: 1.09x faster                                                  |
| sqlglot_parse              | 2.55 ms                                                                | 2.34 ms: 1.09x faster                                                 |
| chaos                      | 104 ms                                                                 | 95.1 ms: 1.09x faster                                                 |
| pycparser                  | 1.52 sec                                                               | 1.40 sec: 1.09x faster                                                |
| async_tree_io_tg           | 793 ms                                                                 | 732 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 2.92 ms                                                                | 2.70 ms: 1.08x faster                                                 |
| async_tree_none_tg         | 349 ms                                                                 | 323 ms: 1.08x faster                                                  |
| async_tree_memoization     | 464 ms                                                                 | 430 ms: 1.08x faster                                                  |
| logging_format             | 11.0 us                                                                | 10.2 us: 1.08x faster                                                 |
| gc_traversal               | 3.51 ms                                                                | 3.28 ms: 1.07x faster                                                 |
| deltablue                  | 8.14 ms                                                                | 7.60 ms: 1.07x faster                                                 |
| async_tree_memoization_tg  | 434 ms                                                                 | 405 ms: 1.07x faster                                                  |
| async_tree_io              | 809 ms                                                                 | 760 ms: 1.07x faster                                                  |
| xml_etree_process          | 78.1 ms                                                                | 73.9 ms: 1.06x faster                                                 |
| async_tree_none            | 376 ms                                                                 | 356 ms: 1.05x faster                                                  |
| spectral_norm              | 115 ms                                                                 | 109 ms: 1.05x faster                                                  |
| subparsers                 | 30.5 ms                                                                | 29.1 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed_tg | 605 ms                                                                 | 579 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed    | 624 ms                                                                 | 600 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 339 us                                                                 | 327 us: 1.04x faster                                                  |
| mdp                        | 2.79 sec                                                               | 2.69 sec: 1.04x faster                                                |
| regex_compile              | 175 ms                                                                 | 170 ms: 1.03x faster                                                  |
| dulwich_log                | 94.0 ms                                                                | 91.2 ms: 1.03x faster                                                 |
| pyflate                    | 670 ms                                                                 | 650 ms: 1.03x faster                                                  |
| sqlalchemy_imperative      | 28.5 ms                                                                | 27.8 ms: 1.02x faster                                                 |
| many_optionals             | 1.26 ms                                                                | 1.23 ms: 1.02x faster                                                 |
| html5lib                   | 96.0 ms                                                                | 94.1 ms: 1.02x faster                                                 |
| pathlib                    | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.20 us                                                                | 2.16 us: 1.02x faster                                                 |
| create_gc_cycles           | 1.83 ms                                                                | 1.80 ms: 1.02x faster                                                 |
| sqlalchemy_declarative     | 201 ms                                                                 | 197 ms: 1.02x faster                                                  |
| coroutines                 | 24.5 ms                                                                | 24.1 ms: 1.02x faster                                                 |
| hexiom                     | 9.86 ms                                                                | 9.72 ms: 1.02x faster                                                 |
| pprint_safe_repr           | 973 ms                                                                 | 961 ms: 1.01x faster                                                  |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| nbody                      | 127 ms                                                                 | 125 ms: 1.01x faster                                                  |
| pprint_pformat             | 2.02 sec                                                               | 2.00 sec: 1.01x faster                                                |
| tomli_loads                | 2.55 sec                                                               | 2.53 sec: 1.01x faster                                                |
| 2to3                       | 364 ms                                                                 | 360 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 5.00 sec                                                               | 4.96 sec: 1.01x faster                                                |
| async_generators           | 452 ms                                                                 | 448 ms: 1.01x faster                                                  |
| scimark_sor                | 233 ms                                                                 | 231 ms: 1.01x faster                                                  |
| crypto_pyaes               | 89.7 ms                                                                | 89.0 ms: 1.01x faster                                                 |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                 |
| bench_mp_pool              | 108 ms                                                                 | 107 ms: 1.01x faster                                                  |
| nqueens                    | 99.0 ms                                                                | 98.2 ms: 1.01x faster                                                 |
| comprehensions             | 27.7 us                                                                | 27.5 us: 1.01x faster                                                 |
| pickle_pure_python         | 507 us                                                                 | 504 us: 1.01x faster                                                  |
| fannkuch                   | 489 ms                                                                 | 486 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.40 ms                                                                | 3.38 ms: 1.01x faster                                                 |
| sympy_sum                  | 349 ms                                                                 | 347 ms: 1.01x faster                                                  |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                 |
| sphinx                     | 1.17 sec                                                               | 1.16 sec: 1.01x faster                                                |
| json_loads                 | 28.5 us                                                                | 28.4 us: 1.00x faster                                                 |
| scimark_fft                | 373 ms                                                                 | 372 ms: 1.00x faster                                                  |
| mako                       | 17.1 ms                                                                | 17.1 ms: 1.00x slower                                                 |
| sympy_expand               | 954 ms                                                                 | 956 ms: 1.00x slower                                                  |
| deepcopy_reduce            | 3.41 us                                                                | 3.42 us: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 5.39 ms                                                                | 5.42 ms: 1.01x slower                                                 |
| sqlglot_normalize          | 132 ms                                                                 | 133 ms: 1.01x slower                                                  |
| xml_etree_iterparse        | 89.4 ms                                                                | 90.2 ms: 1.01x slower                                                 |
| meteor_contest             | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| scimark_lu                 | 180 ms                                                                 | 183 ms: 1.01x slower                                                  |
| deepcopy                   | 321 us                                                                 | 325 us: 1.01x slower                                                  |
| regex_v8                   | 24.8 ms                                                                | 25.2 ms: 1.02x slower                                                 |
| typing_runtime_protocols   | 203 us                                                                 | 208 us: 1.03x slower                                                  |
| regex_dna                  | 179 ms                                                                 | 187 ms: 1.05x slower                                                  |
| regex_effbot               | 2.82 ms                                                                | 2.98 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (21): pylint, shortest_path, connected_components, coverage, xml_etree_generate, k_core, deepcopy_memo, sympy_integrate, django_template, sympy_str, xml_etree_parse, sqlglot_optimize, logging_silent, generators, json, asyncio_websockets, docutils, json_dumps, genshi_xml, genshi_text, telco

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x