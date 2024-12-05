# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.013x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 372 ms                                                                 | 365 ms: 1.02x faster                                                  |
| docutils       | 3.13 sec                                                               | 3.07 sec: 1.02x faster                                                |
| html5lib       | 101 ms                                                                 | 99.2 ms: 1.02x faster                                                 |
| sphinx         | 1.20 sec                                                               | 1.17 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 850 ms                                                                 | 818 ms: 1.04x faster                                                  |
| async_tree_memoization     | 476 ms                                                                 | 459 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 826 ms                                                                 | 798 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 450 ms                                                                 | 437 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 357 ms                                                                 | 348 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 641 ms                                                                 | 626 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 615 ms                                                                 | 602 ms: 1.02x faster                                                  |
| async_tree_none            | 387 ms                                                                 | 379 ms: 1.02x faster                                                  |
| async_generators           | 452 ms                                                                 | 454 ms: 1.00x slower                                                  |
| coroutines                 | 25.5 ms                                                                | 25.8 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 183 ms: 1.00x faster                                                  |
| float          | 140 ms                                                                 | 142 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 191 ms                                                                 | 188 ms: 1.01x faster                                                  |
| regex_v8       | 24.6 ms                                                                | 24.7 ms: 1.00x slower                                                 |
| regex_effbot   | 2.89 ms                                                                | 2.94 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 527 us                                                                 | 513 us: 1.03x faster                                                  |
| json_dumps           | 14.3 ms                                                                | 14.1 ms: 1.01x faster                                                 |
| json_loads           | 28.6 us                                                                | 28.4 us: 1.01x faster                                                 |
| xml_etree_generate   | 98.5 ms                                                                | 98.2 ms: 1.00x faster                                                 |
| xml_etree_parse      | 131 ms                                                                 | 131 ms: 1.00x slower                                                  |
| unpickle_pure_python | 336 us                                                                 | 338 us: 1.00x slower                                                  |
| xml_etree_process    | 77.9 ms                                                                | 78.6 ms: 1.01x slower                                                 |
| tomli_loads          | 2.65 sec                                                               | 2.68 sec: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.6 ms                                                                | 17.2 ms: 1.02x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                                | 30.4 ms: 1.05x faster                                                 |
| mako            | 17.7 ms                                                                | 17.1 ms: 1.04x faster                                                 |
| django_template | 52.3 ms                                                                | 50.6 ms: 1.03x faster                                                 |
| genshi_xml      | 65.0 ms                                                                | 63.0 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_format             | 12.2 us                                                                | 11.1 us: 1.10x faster                                                 |
| logging_simple             | 10.9 us                                                                | 10.1 us: 1.09x faster                                                 |
| gc_traversal               | 3.53 ms                                                                | 3.31 ms: 1.07x faster                                                 |
| deepcopy_reduce            | 3.61 us                                                                | 3.41 us: 1.06x faster                                                 |
| deepcopy                   | 339 us                                                                 | 323 us: 1.05x faster                                                  |
| sqlite_synth               | 2.32 us                                                                | 2.22 us: 1.05x faster                                                 |
| genshi_text                | 31.8 ms                                                                | 30.4 ms: 1.05x faster                                                 |
| subparsers                 | 31.9 ms                                                                | 30.6 ms: 1.04x faster                                                 |
| async_tree_io              | 850 ms                                                                 | 818 ms: 1.04x faster                                                  |
| sqlglot_optimize           | 69.9 ms                                                                | 67.3 ms: 1.04x faster                                                 |
| async_tree_memoization     | 476 ms                                                                 | 459 ms: 1.04x faster                                                  |
| sqlalchemy_imperative      | 30.0 ms                                                                | 28.9 ms: 1.04x faster                                                 |
| mako                       | 17.7 ms                                                                | 17.1 ms: 1.04x faster                                                 |
| pylint                     | 386 ms                                                                 | 372 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 826 ms                                                                 | 798 ms: 1.03x faster                                                  |
| django_template            | 52.3 ms                                                                | 50.6 ms: 1.03x faster                                                 |
| thrift                     | 1.16 ms                                                                | 1.12 ms: 1.03x faster                                                 |
| genshi_xml                 | 65.0 ms                                                                | 63.0 ms: 1.03x faster                                                 |
| crypto_pyaes               | 92.5 ms                                                                | 89.7 ms: 1.03x faster                                                 |
| telco                      | 8.94 ms                                                                | 8.68 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 450 ms                                                                 | 437 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 357 ms                                                                 | 348 ms: 1.03x faster                                                  |
| pickle_pure_python         | 527 us                                                                 | 513 us: 1.03x faster                                                  |
| many_optionals             | 1.30 ms                                                                | 1.26 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 641 ms                                                                 | 626 ms: 1.03x faster                                                  |
| create_gc_cycles           | 1.87 ms                                                                | 1.83 ms: 1.02x faster                                                 |
| sphinx                     | 1.20 sec                                                               | 1.17 sec: 1.02x faster                                                |
| sqlglot_normalize          | 139 ms                                                                 | 136 ms: 1.02x faster                                                  |
| html5lib                   | 101 ms                                                                 | 99.2 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed_tg | 615 ms                                                                 | 602 ms: 1.02x faster                                                  |
| mdp                        | 2.85 sec                                                               | 2.79 sec: 1.02x faster                                                |
| python_startup             | 17.6 ms                                                                | 17.2 ms: 1.02x faster                                                 |
| async_tree_none            | 387 ms                                                                 | 379 ms: 1.02x faster                                                  |
| sqlalchemy_declarative     | 205 ms                                                                 | 201 ms: 1.02x faster                                                  |
| pycparser                  | 1.55 sec                                                               | 1.52 sec: 1.02x faster                                                |
| docutils                   | 3.13 sec                                                               | 3.07 sec: 1.02x faster                                                |
| 2to3                       | 372 ms                                                                 | 365 ms: 1.02x faster                                                  |
| dulwich_log                | 96.7 ms                                                                | 95.0 ms: 1.02x faster                                                 |
| nqueens                    | 99.8 ms                                                                | 98.1 ms: 1.02x faster                                                 |
| pathlib                    | 20.4 ms                                                                | 20.1 ms: 1.02x faster                                                 |
| pprint_pformat             | 2.05 sec                                                               | 2.02 sec: 1.01x faster                                                |
| json_dumps                 | 14.3 ms                                                                | 14.1 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.37 ms                                                                | 3.33 ms: 1.01x faster                                                 |
| regex_dna                  | 191 ms                                                                 | 188 ms: 1.01x faster                                                  |
| bench_mp_pool              | 109 ms                                                                 | 108 ms: 1.01x faster                                                  |
| raytrace                   | 566 ms                                                                 | 559 ms: 1.01x faster                                                  |
| sympy_sum                  | 353 ms                                                                 | 349 ms: 1.01x faster                                                  |
| scimark_lu                 | 186 ms                                                                 | 184 ms: 1.01x faster                                                  |
| json                       | 5.12 ms                                                                | 5.07 ms: 1.01x faster                                                 |
| scimark_sor                | 239 ms                                                                 | 237 ms: 1.01x faster                                                  |
| connected_components       | 504 ms                                                                 | 500 ms: 1.01x faster                                                  |
| shortest_path              | 554 ms                                                                 | 550 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 980 ms                                                                 | 973 ms: 1.01x faster                                                  |
| sympy_str                  | 482 ms                                                                 | 479 ms: 1.01x faster                                                  |
| json_loads                 | 28.6 us                                                                | 28.4 us: 1.01x faster                                                 |
| chaos                      | 105 ms                                                                 | 104 ms: 1.01x faster                                                  |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.01x faster                                                 |
| sympy_expand               | 967 ms                                                                 | 961 ms: 1.01x faster                                                  |
| sympy_integrate            | 29.8 ms                                                                | 29.6 ms: 1.01x faster                                                 |
| go                         | 276 ms                                                                 | 275 ms: 1.00x faster                                                  |
| k_core                     | 2.43 sec                                                               | 2.42 sec: 1.00x faster                                                |
| logging_silent             | 191 ns                                                                 | 190 ns: 1.00x faster                                                  |
| bpe_tokeniser              | 5.01 sec                                                               | 4.99 sec: 1.00x faster                                                |
| xml_etree_generate         | 98.5 ms                                                                | 98.2 ms: 1.00x faster                                                 |
| pidigits                   | 184 ms                                                                 | 183 ms: 1.00x faster                                                  |
| xml_etree_parse            | 131 ms                                                                 | 131 ms: 1.00x slower                                                  |
| hexiom                     | 9.98 ms                                                                | 10.0 ms: 1.00x slower                                                 |
| regex_v8                   | 24.6 ms                                                                | 24.7 ms: 1.00x slower                                                 |
| async_generators           | 452 ms                                                                 | 454 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 336 us                                                                 | 338 us: 1.00x slower                                                  |
| scimark_fft                | 392 ms                                                                 | 394 ms: 1.01x slower                                                  |
| xml_etree_process          | 77.9 ms                                                                | 78.6 ms: 1.01x slower                                                 |
| coroutines                 | 25.5 ms                                                                | 25.8 ms: 1.01x slower                                                 |
| coverage                   | 103 ms                                                                 | 104 ms: 1.01x slower                                                  |
| tomli_loads                | 2.65 sec                                                               | 2.68 sec: 1.01x slower                                                |
| scimark_monte_carlo        | 119 ms                                                                 | 121 ms: 1.01x slower                                                  |
| float                      | 140 ms                                                                 | 142 ms: 1.01x slower                                                  |
| pyflate                    | 692 ms                                                                 | 703 ms: 1.01x slower                                                  |
| deltablue                  | 8.22 ms                                                                | 8.34 ms: 1.02x slower                                                 |
| regex_effbot               | 2.89 ms                                                                | 2.94 ms: 1.02x slower                                                 |
| richards                   | 78.1 ms                                                                | 79.4 ms: 1.02x slower                                                 |
| comprehensions             | 27.4 us                                                                | 28.1 us: 1.02x slower                                                 |
| richards_super             | 87.2 ms                                                                | 89.5 ms: 1.03x slower                                                 |
| scimark_sparse_mat_mult    | 5.54 ms                                                                | 5.69 ms: 1.03x slower                                                 |
| meteor_contest             | 129 ms                                                                 | 134 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (11): typing_runtime_protocols, asyncio_websockets, spectral_norm, nbody, generators, regex_compile, deepcopy_memo, xml_etree_iterparse, fannkuch, sqlglot_transpile, sqlglot_parse

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x