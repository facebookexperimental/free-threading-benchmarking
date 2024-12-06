# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.017x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 372 ms                                                                 | 363 ms: 1.03x faster                                                  |
| docutils       | 3.13 sec                                                               | 3.08 sec: 1.02x faster                                                |
| html5lib       | 101 ms                                                                 | 97.9 ms: 1.04x faster                                                 |
| sphinx         | 1.20 sec                                                               | 1.17 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 476 ms                                                                 | 459 ms: 1.04x faster                                                  |
| async_tree_io              | 850 ms                                                                 | 821 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 826 ms                                                                 | 804 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 450 ms                                                                 | 439 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 641 ms                                                                 | 626 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 357 ms                                                                 | 350 ms: 1.02x faster                                                  |
| async_tree_none            | 387 ms                                                                 | 379 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 615 ms                                                                 | 606 ms: 1.01x faster                                                  |
| async_generators           | 452 ms                                                                 | 459 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 126 ms: 1.07x faster                                                  |
| pidigits       | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| float          | 140 ms                                                                 | 139 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 191 ms                                                                 | 185 ms: 1.03x faster                                                  |
| regex_compile  | 181 ms                                                                 | 178 ms: 1.02x faster                                                  |
| regex_effbot   | 2.89 ms                                                                | 2.89 ms: 1.00x faster                                                 |
| regex_v8       | 24.6 ms                                                                | 24.7 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 527 us                                                                 | 512 us: 1.03x faster                                                  |
| json_dumps           | 14.3 ms                                                                | 13.9 ms: 1.02x faster                                                 |
| unpickle_pure_python | 336 us                                                                 | 332 us: 1.01x faster                                                  |
| json_loads           | 28.6 us                                                                | 28.3 us: 1.01x faster                                                 |
| xml_etree_generate   | 98.5 ms                                                                | 97.6 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 91.9 ms                                                                | 91.2 ms: 1.01x faster                                                 |
| xml_etree_process    | 77.9 ms                                                                | 78.2 ms: 1.00x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.6 ms                                                                | 17.2 ms: 1.02x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                                | 30.3 ms: 1.05x faster                                                 |
| mako            | 17.7 ms                                                                | 16.9 ms: 1.05x faster                                                 |
| genshi_xml      | 65.0 ms                                                                | 62.7 ms: 1.04x faster                                                 |
| django_template | 52.3 ms                                                                | 50.5 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_format             | 12.2 us                                                                | 11.0 us: 1.10x faster                                                 |
| logging_simple             | 10.9 us                                                                | 10.2 us: 1.08x faster                                                 |
| nbody                      | 134 ms                                                                 | 126 ms: 1.07x faster                                                  |
| genshi_text                | 31.8 ms                                                                | 30.3 ms: 1.05x faster                                                 |
| sqlite_synth               | 2.32 us                                                                | 2.21 us: 1.05x faster                                                 |
| mako                       | 17.7 ms                                                                | 16.9 ms: 1.05x faster                                                 |
| deepcopy_reduce            | 3.61 us                                                                | 3.46 us: 1.05x faster                                                 |
| nqueens                    | 99.8 ms                                                                | 95.6 ms: 1.04x faster                                                 |
| deepcopy                   | 339 us                                                                 | 325 us: 1.04x faster                                                  |
| sqlglot_optimize           | 69.9 ms                                                                | 67.0 ms: 1.04x faster                                                 |
| pylint                     | 386 ms                                                                 | 371 ms: 1.04x faster                                                  |
| async_tree_memoization     | 476 ms                                                                 | 459 ms: 1.04x faster                                                  |
| genshi_xml                 | 65.0 ms                                                                | 62.7 ms: 1.04x faster                                                 |
| async_tree_io              | 850 ms                                                                 | 821 ms: 1.04x faster                                                  |
| html5lib                   | 101 ms                                                                 | 97.9 ms: 1.04x faster                                                 |
| django_template            | 52.3 ms                                                                | 50.5 ms: 1.03x faster                                                 |
| subparsers                 | 31.9 ms                                                                | 30.9 ms: 1.03x faster                                                 |
| pprint_pformat             | 2.05 sec                                                               | 1.98 sec: 1.03x faster                                                |
| pickle_pure_python         | 527 us                                                                 | 512 us: 1.03x faster                                                  |
| sqlalchemy_imperative      | 30.0 ms                                                                | 29.2 ms: 1.03x faster                                                 |
| generators                 | 39.7 ms                                                                | 38.6 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 980 ms                                                                 | 954 ms: 1.03x faster                                                  |
| regex_dna                  | 191 ms                                                                 | 185 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 826 ms                                                                 | 804 ms: 1.03x faster                                                  |
| logging_silent             | 191 ns                                                                 | 186 ns: 1.03x faster                                                  |
| many_optionals             | 1.30 ms                                                                | 1.27 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 450 ms                                                                 | 439 ms: 1.03x faster                                                  |
| 2to3                       | 372 ms                                                                 | 363 ms: 1.03x faster                                                  |
| sphinx                     | 1.20 sec                                                               | 1.17 sec: 1.02x faster                                                |
| async_tree_cpu_io_mixed    | 641 ms                                                                 | 626 ms: 1.02x faster                                                  |
| pycparser                  | 1.55 sec                                                               | 1.52 sec: 1.02x faster                                                |
| json                       | 5.12 ms                                                                | 5.01 ms: 1.02x faster                                                 |
| go                         | 276 ms                                                                 | 270 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 139 ms                                                                 | 136 ms: 1.02x faster                                                  |
| json_dumps                 | 14.3 ms                                                                | 13.9 ms: 1.02x faster                                                 |
| sqlalchemy_declarative     | 205 ms                                                                 | 201 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 357 ms                                                                 | 350 ms: 1.02x faster                                                  |
| async_tree_none            | 387 ms                                                                 | 379 ms: 1.02x faster                                                  |
| crypto_pyaes               | 92.5 ms                                                                | 90.5 ms: 1.02x faster                                                 |
| mdp                        | 2.85 sec                                                               | 2.79 sec: 1.02x faster                                                |
| chaos                      | 105 ms                                                                 | 103 ms: 1.02x faster                                                  |
| coverage                   | 103 ms                                                                 | 101 ms: 1.02x faster                                                  |
| dulwich_log                | 96.7 ms                                                                | 94.9 ms: 1.02x faster                                                 |
| python_startup             | 17.6 ms                                                                | 17.2 ms: 1.02x faster                                                 |
| regex_compile              | 181 ms                                                                 | 178 ms: 1.02x faster                                                  |
| pathlib                    | 20.4 ms                                                                | 20.1 ms: 1.02x faster                                                 |
| hexiom                     | 9.98 ms                                                                | 9.82 ms: 1.02x faster                                                 |
| docutils                   | 3.13 sec                                                               | 3.08 sec: 1.02x faster                                                |
| async_tree_cpu_io_mixed_tg | 615 ms                                                                 | 606 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 336 us                                                                 | 332 us: 1.01x faster                                                  |
| sympy_expand               | 967 ms                                                                 | 955 ms: 1.01x faster                                                  |
| sqlglot_parse              | 2.61 ms                                                                | 2.57 ms: 1.01x faster                                                 |
| json_loads                 | 28.6 us                                                                | 28.3 us: 1.01x faster                                                 |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| sympy_str                  | 482 ms                                                                 | 476 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 3.00 ms                                                                | 2.96 ms: 1.01x faster                                                 |
| sympy_sum                  | 353 ms                                                                 | 349 ms: 1.01x faster                                                  |
| raytrace                   | 566 ms                                                                 | 559 ms: 1.01x faster                                                  |
| typing_runtime_protocols   | 207 us                                                                 | 205 us: 1.01x faster                                                  |
| spectral_norm              | 122 ms                                                                 | 121 ms: 1.01x faster                                                  |
| scimark_fft                | 392 ms                                                                 | 388 ms: 1.01x faster                                                  |
| telco                      | 8.94 ms                                                                | 8.84 ms: 1.01x faster                                                 |
| bench_mp_pool              | 109 ms                                                                 | 108 ms: 1.01x faster                                                  |
| xml_etree_generate         | 98.5 ms                                                                | 97.6 ms: 1.01x faster                                                 |
| scimark_sor                | 239 ms                                                                 | 237 ms: 1.01x faster                                                  |
| scimark_monte_carlo        | 119 ms                                                                 | 118 ms: 1.01x faster                                                  |
| float                      | 140 ms                                                                 | 139 ms: 1.01x faster                                                  |
| sympy_integrate            | 29.8 ms                                                                | 29.5 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.37 ms                                                                | 3.34 ms: 1.01x faster                                                 |
| k_core                     | 2.43 sec                                                               | 2.41 sec: 1.01x faster                                                |
| thrift                     | 1.16 ms                                                                | 1.15 ms: 1.01x faster                                                 |
| connected_components       | 504 ms                                                                 | 501 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 91.9 ms                                                                | 91.2 ms: 1.01x faster                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                 |
| regex_effbot               | 2.89 ms                                                                | 2.89 ms: 1.00x faster                                                 |
| regex_v8                   | 24.6 ms                                                                | 24.7 ms: 1.00x slower                                                 |
| deepcopy_memo              | 40.0 us                                                                | 40.1 us: 1.00x slower                                                 |
| xml_etree_process          | 77.9 ms                                                                | 78.2 ms: 1.00x slower                                                 |
| scimark_lu                 | 186 ms                                                                 | 187 ms: 1.01x slower                                                  |
| bpe_tokeniser              | 5.01 sec                                                               | 5.04 sec: 1.01x slower                                                |
| richards                   | 78.1 ms                                                                | 78.8 ms: 1.01x slower                                                 |
| richards_super             | 87.2 ms                                                                | 88.0 ms: 1.01x slower                                                 |
| pyflate                    | 692 ms                                                                 | 703 ms: 1.01x slower                                                  |
| comprehensions             | 27.4 us                                                                | 27.8 us: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 5.54 ms                                                                | 5.62 ms: 1.02x slower                                                 |
| async_generators           | 452 ms                                                                 | 459 ms: 1.02x slower                                                  |
| meteor_contest             | 129 ms                                                                 | 132 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (9): tomli_loads, asyncio_websockets, deltablue, shortest_path, fannkuch, gc_traversal, create_gc_cycles, coroutines, xml_etree_parse

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x