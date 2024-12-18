# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.017x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 365 ms                                                                 | 367 ms: 1.01x slower                                                     |
| html5lib       | 98.4 ms                                                                | 95.7 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 347 ms                                                                 | 327 ms: 1.06x faster                                                     |
| async_tree_io_tg           | 793 ms                                                                 | 752 ms: 1.06x faster                                                     |
| async_tree_memoization_tg  | 434 ms                                                                 | 415 ms: 1.05x faster                                                     |
| async_tree_io              | 813 ms                                                                 | 777 ms: 1.05x faster                                                     |
| async_tree_memoization     | 462 ms                                                                 | 442 ms: 1.04x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 363 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 583 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed    | 627 ms                                                                 | 608 ms: 1.03x faster                                                     |
| async_generators           | 453 ms                                                                 | 446 ms: 1.02x faster                                                     |
| coroutines                 | 25.2 ms                                                                | 25.1 ms: 1.01x faster                                                    |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 136 ms                                                                 | 111 ms: 1.22x faster                                                     |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x faster                                                     |
| nbody          | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 172 ms: 1.03x faster                                                     |
| regex_effbot   | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                    |
| regex_dna      | 181 ms                                                                 | 188 ms: 1.04x slower                                                     |
| regex_v8       | 23.7 ms                                                                | 24.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 79.0 ms                                                                | 74.3 ms: 1.06x faster                                                    |
| xml_etree_iterparse  | 90.7 ms                                                                | 89.9 ms: 1.01x faster                                                    |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| json_dumps           | 14.0 ms                                                                | 14.2 ms: 1.02x slower                                                    |
| unpickle_pure_python | 335 us                                                                 | 346 us: 1.03x slower                                                     |
| pickle_pure_python   | 503 us                                                                 | 533 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (3): json_loads, xml_etree_generate, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 30.5 ms                                                                | 30.6 ms: 1.01x slower                                                    |
| django_template | 49.5 ms                                                                | 51.2 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float                      | 136 ms                                                                 | 111 ms: 1.22x faster                                                     |
| gc_traversal               | 3.52 ms                                                                | 3.16 ms: 1.11x faster                                                    |
| thrift                     | 1.11 ms                                                                | 998 us: 1.11x faster                                                     |
| sqlglot_parse              | 2.59 ms                                                                | 2.35 ms: 1.10x faster                                                    |
| sqlglot_transpile          | 2.95 ms                                                                | 2.71 ms: 1.09x faster                                                    |
| scimark_sparse_mat_mult    | 5.64 ms                                                                | 5.20 ms: 1.08x faster                                                    |
| pycparser                  | 1.54 sec                                                               | 1.43 sec: 1.08x faster                                                   |
| logging_simple             | 10.00 us                                                               | 9.35 us: 1.07x faster                                                    |
| xml_etree_process          | 79.0 ms                                                                | 74.3 ms: 1.06x faster                                                    |
| async_tree_none_tg         | 347 ms                                                                 | 327 ms: 1.06x faster                                                     |
| raytrace                   | 555 ms                                                                 | 523 ms: 1.06x faster                                                     |
| scimark_monte_carlo        | 118 ms                                                                 | 111 ms: 1.06x faster                                                     |
| logging_format             | 11.1 us                                                                | 10.5 us: 1.06x faster                                                    |
| async_tree_io_tg           | 793 ms                                                                 | 752 ms: 1.06x faster                                                     |
| chaos                      | 104 ms                                                                 | 99.0 ms: 1.05x faster                                                    |
| richards_super             | 86.0 ms                                                                | 81.6 ms: 1.05x faster                                                    |
| richards                   | 77.4 ms                                                                | 73.6 ms: 1.05x faster                                                    |
| async_tree_memoization_tg  | 434 ms                                                                 | 415 ms: 1.05x faster                                                     |
| async_tree_io              | 813 ms                                                                 | 777 ms: 1.05x faster                                                     |
| async_tree_memoization     | 462 ms                                                                 | 442 ms: 1.04x faster                                                     |
| spectral_norm              | 112 ms                                                                 | 107 ms: 1.04x faster                                                     |
| scimark_fft                | 385 ms                                                                 | 371 ms: 1.04x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 363 ms: 1.04x faster                                                     |
| subparsers                 | 30.7 ms                                                                | 29.7 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 583 ms: 1.04x faster                                                     |
| sqlite_synth               | 2.21 us                                                                | 2.14 us: 1.04x faster                                                    |
| async_tree_cpu_io_mixed    | 627 ms                                                                 | 608 ms: 1.03x faster                                                     |
| regex_compile              | 177 ms                                                                 | 172 ms: 1.03x faster                                                     |
| dulwich_log                | 93.9 ms                                                                | 91.2 ms: 1.03x faster                                                    |
| html5lib                   | 98.4 ms                                                                | 95.7 ms: 1.03x faster                                                    |
| sqlalchemy_imperative      | 29.0 ms                                                                | 28.2 ms: 1.03x faster                                                    |
| create_gc_cycles           | 1.83 ms                                                                | 1.78 ms: 1.03x faster                                                    |
| go                         | 268 ms                                                                 | 261 ms: 1.03x faster                                                     |
| sqlalchemy_declarative     | 202 ms                                                                 | 198 ms: 1.02x faster                                                     |
| deltablue                  | 8.19 ms                                                                | 8.05 ms: 1.02x faster                                                    |
| async_generators           | 453 ms                                                                 | 446 ms: 1.02x faster                                                     |
| meteor_contest             | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| regex_effbot               | 2.82 ms                                                                | 2.79 ms: 1.01x faster                                                    |
| sympy_str                  | 478 ms                                                                 | 473 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 90.7 ms                                                                | 89.9 ms: 1.01x faster                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| many_optionals             | 1.26 ms                                                                | 1.25 ms: 1.01x faster                                                    |
| bench_mp_pool              | 108 ms                                                                 | 107 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 5.02 sec                                                               | 4.99 sec: 1.01x faster                                                   |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                    |
| fannkuch                   | 496 ms                                                                 | 493 ms: 1.01x faster                                                     |
| mdp                        | 2.90 sec                                                               | 2.88 sec: 1.01x faster                                                   |
| sympy_expand               | 958 ms                                                                 | 953 ms: 1.01x faster                                                     |
| coroutines                 | 25.2 ms                                                                | 25.1 ms: 1.01x faster                                                    |
| deepcopy_memo              | 40.4 us                                                                | 40.2 us: 1.00x faster                                                    |
| sympy_sum                  | 349 ms                                                                 | 348 ms: 1.00x faster                                                     |
| pidigits                   | 181 ms                                                                 | 181 ms: 1.00x faster                                                     |
| pprint_safe_repr           | 979 ms                                                                 | 984 ms: 1.01x slower                                                     |
| genshi_text                | 30.5 ms                                                                | 30.6 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 133 ms                                                                 | 133 ms: 1.01x slower                                                     |
| nqueens                    | 97.2 ms                                                                | 97.8 ms: 1.01x slower                                                    |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| json                       | 5.02 ms                                                                | 5.05 ms: 1.01x slower                                                    |
| 2to3                       | 365 ms                                                                 | 367 ms: 1.01x slower                                                     |
| scimark_lu                 | 184 ms                                                                 | 187 ms: 1.02x slower                                                     |
| comprehensions             | 28.0 us                                                                | 28.5 us: 1.02x slower                                                    |
| json_dumps                 | 14.0 ms                                                                | 14.2 ms: 1.02x slower                                                    |
| deepcopy                   | 320 us                                                                 | 327 us: 1.02x slower                                                     |
| crypto_pyaes               | 90.6 ms                                                                | 92.7 ms: 1.02x slower                                                    |
| generators                 | 38.6 ms                                                                | 39.5 ms: 1.02x slower                                                    |
| nbody                      | 128 ms                                                                 | 131 ms: 1.02x slower                                                     |
| unpickle_pure_python       | 335 us                                                                 | 346 us: 1.03x slower                                                     |
| django_template            | 49.5 ms                                                                | 51.2 ms: 1.04x slower                                                    |
| regex_dna                  | 181 ms                                                                 | 188 ms: 1.04x slower                                                     |
| hexiom                     | 9.83 ms                                                                | 10.2 ms: 1.04x slower                                                    |
| coverage                   | 101 ms                                                                 | 105 ms: 1.04x slower                                                     |
| scimark_sor                | 235 ms                                                                 | 245 ms: 1.04x slower                                                     |
| regex_v8                   | 23.7 ms                                                                | 24.8 ms: 1.05x slower                                                    |
| pickle_pure_python         | 503 us                                                                 | 533 us: 1.06x slower                                                     |
| logging_silent             | 182 ns                                                                 | 200 ns: 1.10x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (21): pylint, docutils, typing_runtime_protocols, asyncio_websockets, sphinx, telco, json_loads, mako, pathlib, deepcopy_reduce, bench_thread_pool, xml_etree_generate, pyflate, pprint_pformat, sympy_integrate, sqlglot_optimize, tomli_loads, k_core, connected_components, genshi_xml, shortest_path

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x