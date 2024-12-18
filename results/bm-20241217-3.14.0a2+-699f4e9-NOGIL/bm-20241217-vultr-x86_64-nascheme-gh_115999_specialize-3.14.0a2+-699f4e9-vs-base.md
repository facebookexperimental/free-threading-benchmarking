# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.012x faster
- HPT reliability: 99.56%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 365 ms                                                                 | 371 ms: 1.02x slower                                                     |
| docutils       | 3.08 sec                                                               | 3.12 sec: 1.01x slower                                                   |
| sphinx         | 1.17 sec                                                               | 1.19 sec: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 793 ms                                                                 | 759 ms: 1.04x faster                                                     |
| async_tree_none_tg         | 347 ms                                                                 | 334 ms: 1.04x faster                                                     |
| async_tree_memoization_tg  | 434 ms                                                                 | 417 ms: 1.04x faster                                                     |
| async_tree_memoization     | 462 ms                                                                 | 446 ms: 1.04x faster                                                     |
| async_tree_io              | 813 ms                                                                 | 789 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 587 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed    | 627 ms                                                                 | 613 ms: 1.02x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 368 ms: 1.02x faster                                                     |
| async_generators           | 453 ms                                                                 | 450 ms: 1.01x faster                                                     |
| coroutines                 | 25.2 ms                                                                | 25.3 ms: 1.00x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 136 ms                                                                 | 112 ms: 1.22x faster                                                     |
| pidigits       | 181 ms                                                                 | 184 ms: 1.01x slower                                                     |
| nbody          | 128 ms                                                                 | 130 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                 | 174 ms: 1.02x faster                                                     |
| regex_dna      | 181 ms                                                                 | 183 ms: 1.01x slower                                                     |
| regex_v8       | 23.7 ms                                                                | 24.4 ms: 1.03x slower                                                    |
| regex_effbot   | 2.82 ms                                                                | 2.92 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 79.0 ms                                                                | 74.3 ms: 1.06x faster                                                    |
| tomli_loads          | 2.59 sec                                                               | 2.56 sec: 1.01x faster                                                   |
| xml_etree_parse      | 130 ms                                                                 | 130 ms: 1.00x slower                                                     |
| json_dumps           | 14.0 ms                                                                | 14.4 ms: 1.03x slower                                                    |
| unpickle_pure_python | 335 us                                                                 | 346 us: 1.03x slower                                                     |
| pickle_pure_python   | 503 us                                                                 | 535 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| python_startup         | 17.2 ms                                                                | 17.1 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                    |
| genshi_text     | 30.5 ms                                                                | 30.7 ms: 1.01x slower                                                    |
| genshi_xml      | 63.2 ms                                                                | 64.0 ms: 1.01x slower                                                    |
| django_template | 49.5 ms                                                                | 51.6 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float                      | 136 ms                                                                 | 112 ms: 1.22x faster                                                     |
| thrift                     | 1.11 ms                                                                | 1.00 ms: 1.11x faster                                                    |
| sqlglot_parse              | 2.59 ms                                                                | 2.37 ms: 1.09x faster                                                    |
| sqlglot_transpile          | 2.95 ms                                                                | 2.73 ms: 1.08x faster                                                    |
| logging_format             | 11.1 us                                                                | 10.3 us: 1.08x faster                                                    |
| logging_simple             | 10.00 us                                                               | 9.28 us: 1.08x faster                                                    |
| gc_traversal               | 3.52 ms                                                                | 3.27 ms: 1.08x faster                                                    |
| pycparser                  | 1.54 sec                                                               | 1.44 sec: 1.07x faster                                                   |
| xml_etree_process          | 79.0 ms                                                                | 74.3 ms: 1.06x faster                                                    |
| scimark_sparse_mat_mult    | 5.64 ms                                                                | 5.35 ms: 1.05x faster                                                    |
| scimark_monte_carlo        | 118 ms                                                                 | 113 ms: 1.04x faster                                                     |
| async_tree_io_tg           | 793 ms                                                                 | 759 ms: 1.04x faster                                                     |
| async_tree_none_tg         | 347 ms                                                                 | 334 ms: 1.04x faster                                                     |
| async_tree_memoization_tg  | 434 ms                                                                 | 417 ms: 1.04x faster                                                     |
| subparsers                 | 30.7 ms                                                                | 29.6 ms: 1.04x faster                                                    |
| raytrace                   | 555 ms                                                                 | 534 ms: 1.04x faster                                                     |
| chaos                      | 104 ms                                                                 | 101 ms: 1.04x faster                                                     |
| async_tree_memoization     | 462 ms                                                                 | 446 ms: 1.04x faster                                                     |
| richards_super             | 86.0 ms                                                                | 83.0 ms: 1.04x faster                                                    |
| sqlite_synth               | 2.21 us                                                                | 2.14 us: 1.04x faster                                                    |
| async_tree_io              | 813 ms                                                                 | 789 ms: 1.03x faster                                                     |
| richards                   | 77.4 ms                                                                | 75.2 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg | 603 ms                                                                 | 587 ms: 1.03x faster                                                     |
| sqlalchemy_imperative      | 29.0 ms                                                                | 28.2 ms: 1.03x faster                                                    |
| dulwich_log                | 93.9 ms                                                                | 91.5 ms: 1.03x faster                                                    |
| spectral_norm              | 112 ms                                                                 | 109 ms: 1.03x faster                                                     |
| create_gc_cycles           | 1.83 ms                                                                | 1.79 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed    | 627 ms                                                                 | 613 ms: 1.02x faster                                                     |
| async_tree_none            | 376 ms                                                                 | 368 ms: 1.02x faster                                                     |
| scimark_fft                | 385 ms                                                                 | 376 ms: 1.02x faster                                                     |
| fannkuch                   | 496 ms                                                                 | 487 ms: 1.02x faster                                                     |
| sqlalchemy_declarative     | 202 ms                                                                 | 198 ms: 1.02x faster                                                     |
| regex_compile              | 177 ms                                                                 | 174 ms: 1.02x faster                                                     |
| pathlib                    | 19.7 ms                                                                | 19.4 ms: 1.01x faster                                                    |
| tomli_loads                | 2.59 sec                                                               | 2.56 sec: 1.01x faster                                                   |
| mdp                        | 2.90 sec                                                               | 2.87 sec: 1.01x faster                                                   |
| meteor_contest             | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| bench_mp_pool              | 108 ms                                                                 | 107 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 5.02 sec                                                               | 4.98 sec: 1.01x faster                                                   |
| mako                       | 17.2 ms                                                                | 17.1 ms: 1.01x faster                                                    |
| async_generators           | 453 ms                                                                 | 450 ms: 1.01x faster                                                     |
| sympy_expand               | 958 ms                                                                 | 954 ms: 1.00x faster                                                     |
| sympy_str                  | 478 ms                                                                 | 476 ms: 1.00x faster                                                     |
| python_startup             | 17.2 ms                                                                | 17.1 ms: 1.00x faster                                                    |
| go                         | 268 ms                                                                 | 267 ms: 1.00x faster                                                     |
| k_core                     | 2.35 sec                                                               | 2.35 sec: 1.00x faster                                                   |
| coroutines                 | 25.2 ms                                                                | 25.3 ms: 1.00x slower                                                    |
| deepcopy                   | 320 us                                                                 | 321 us: 1.00x slower                                                     |
| xml_etree_parse            | 130 ms                                                                 | 130 ms: 1.00x slower                                                     |
| sympy_integrate            | 29.5 ms                                                                | 29.7 ms: 1.01x slower                                                    |
| genshi_text                | 30.5 ms                                                                | 30.7 ms: 1.01x slower                                                    |
| pprint_safe_repr           | 979 ms                                                                 | 987 ms: 1.01x slower                                                     |
| sqlglot_normalize          | 133 ms                                                                 | 134 ms: 1.01x slower                                                     |
| nqueens                    | 97.2 ms                                                                | 97.9 ms: 1.01x slower                                                    |
| sphinx                     | 1.17 sec                                                               | 1.19 sec: 1.01x slower                                                   |
| regex_dna                  | 181 ms                                                                 | 183 ms: 1.01x slower                                                     |
| deltablue                  | 8.19 ms                                                                | 8.28 ms: 1.01x slower                                                    |
| docutils                   | 3.08 sec                                                               | 3.12 sec: 1.01x slower                                                   |
| genshi_xml                 | 63.2 ms                                                                | 64.0 ms: 1.01x slower                                                    |
| pidigits                   | 181 ms                                                                 | 184 ms: 1.01x slower                                                     |
| pyflate                    | 671 ms                                                                 | 681 ms: 1.02x slower                                                     |
| json                       | 5.02 ms                                                                | 5.10 ms: 1.02x slower                                                    |
| 2to3                       | 365 ms                                                                 | 371 ms: 1.02x slower                                                     |
| nbody                      | 128 ms                                                                 | 130 ms: 1.02x slower                                                     |
| telco                      | 8.60 ms                                                                | 8.79 ms: 1.02x slower                                                    |
| comprehensions             | 28.0 us                                                                | 28.7 us: 1.03x slower                                                    |
| json_dumps                 | 14.0 ms                                                                | 14.4 ms: 1.03x slower                                                    |
| scimark_lu                 | 184 ms                                                                 | 189 ms: 1.03x slower                                                     |
| unpickle_pure_python       | 335 us                                                                 | 346 us: 1.03x slower                                                     |
| regex_v8                   | 23.7 ms                                                                | 24.4 ms: 1.03x slower                                                    |
| regex_effbot               | 2.82 ms                                                                | 2.92 ms: 1.04x slower                                                    |
| generators                 | 38.6 ms                                                                | 40.1 ms: 1.04x slower                                                    |
| hexiom                     | 9.83 ms                                                                | 10.2 ms: 1.04x slower                                                    |
| django_template            | 49.5 ms                                                                | 51.6 ms: 1.04x slower                                                    |
| scimark_sor                | 235 ms                                                                 | 245 ms: 1.04x slower                                                     |
| pickle_pure_python         | 503 us                                                                 | 535 us: 1.06x slower                                                     |
| logging_silent             | 182 ns                                                                 | 201 ns: 1.10x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (18): pylint, deepcopy_reduce, many_optionals, xml_etree_iterparse, connected_components, asyncio_websockets, sympy_sum, sqlglot_optimize, coverage, html5lib, bench_thread_pool, crypto_pyaes, pprint_pformat, shortest_path, deepcopy_memo, xml_etree_generate, json_loads, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 99.56% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x