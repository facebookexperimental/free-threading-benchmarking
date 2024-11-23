# Results vs. base

- fork: colesbury
- ref: gh_115999_store_subs
- machine: linux-x86_64
- commit hash: 2b63929
- commit date: 2024-11-22
- overall geometric mean: 1.00x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 378 ms                                                                 | 379 ms: 1.00x slower                                                      |
| docutils       | 3.23 sec                                                               | 3.21 sec: 1.01x faster                                                    |
| html5lib       | 103 ms                                                                 | 99.7 ms: 1.03x faster                                                     |
| sphinx         | 1.24 sec                                                               | 1.24 sec: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 677 ms                                                                 | 660 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed_tg | 648 ms                                                                 | 633 ms: 1.02x faster                                                      |
| async_tree_memoization     | 505 ms                                                                 | 496 ms: 1.02x faster                                                      |
| async_tree_io              | 913 ms                                                                 | 898 ms: 1.02x faster                                                      |
| async_tree_none_tg         | 378 ms                                                                 | 373 ms: 1.01x faster                                                      |
| async_generators           | 478 ms                                                                 | 471 ms: 1.01x faster                                                      |
| async_tree_memoization_tg  | 473 ms                                                                 | 467 ms: 1.01x faster                                                      |
| async_tree_io_tg           | 885 ms                                                                 | 874 ms: 1.01x faster                                                      |
| async_tree_none            | 412 ms                                                                 | 407 ms: 1.01x faster                                                      |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                      |
| coroutines                 | 27.0 ms                                                                | 27.6 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 160 ms                                                                 | 144 ms: 1.11x faster                                                      |
| pidigits       | 181 ms                                                                 | 184 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 185 ms                                                                 | 181 ms: 1.03x faster                                                      |
| regex_compile  | 196 ms                                                                 | 194 ms: 1.01x faster                                                      |
| regex_v8       | 24.3 ms                                                                | 24.7 ms: 1.02x slower                                                     |
| regex_effbot   | 2.77 ms                                                                | 2.84 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_loads           | 28.3 us                                                                | 27.8 us: 1.02x faster                                                     |
| json_dumps           | 14.4 ms                                                                | 14.3 ms: 1.01x faster                                                     |
| xml_etree_generate   | 103 ms                                                                 | 103 ms: 1.00x slower                                                      |
| xml_etree_iterparse  | 95.0 ms                                                                | 95.9 ms: 1.01x slower                                                     |
| xml_etree_parse      | 131 ms                                                                 | 132 ms: 1.01x slower                                                      |
| unpickle_pure_python | 363 us                                                                 | 370 us: 1.02x slower                                                      |
| pickle_pure_python   | 539 us                                                                 | 561 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (2): xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x slower                                                     |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 69.3 ms                                                                | 67.6 ms: 1.03x faster                                                     |
| genshi_text     | 34.6 ms                                                                | 33.9 ms: 1.02x faster                                                     |
| django_template | 56.5 ms                                                                | 55.6 ms: 1.02x faster                                                     |
| mako            | 19.5 ms                                                                | 19.8 ms: 1.01x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2+-a264637 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody                      | 160 ms                                                                 | 144 ms: 1.11x faster                                                      |
| generators                 | 39.7 ms                                                                | 38.6 ms: 1.03x faster                                                     |
| html5lib                   | 103 ms                                                                 | 99.7 ms: 1.03x faster                                                     |
| nqueens                    | 108 ms                                                                 | 105 ms: 1.03x faster                                                      |
| deepcopy_reduce            | 3.78 us                                                                | 3.68 us: 1.03x faster                                                     |
| fannkuch                   | 547 ms                                                                 | 533 ms: 1.03x faster                                                      |
| regex_dna                  | 185 ms                                                                 | 181 ms: 1.03x faster                                                      |
| genshi_xml                 | 69.3 ms                                                                | 67.6 ms: 1.03x faster                                                     |
| logging_simple             | 11.2 us                                                                | 11.0 us: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 677 ms                                                                 | 660 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed_tg | 648 ms                                                                 | 633 ms: 1.02x faster                                                      |
| genshi_text                | 34.6 ms                                                                | 33.9 ms: 1.02x faster                                                     |
| coverage                   | 104 ms                                                                 | 102 ms: 1.02x faster                                                      |
| async_tree_memoization     | 505 ms                                                                 | 496 ms: 1.02x faster                                                      |
| sympy_integrate            | 31.4 ms                                                                | 30.8 ms: 1.02x faster                                                     |
| sqlite_synth               | 2.33 us                                                                | 2.29 us: 1.02x faster                                                     |
| json                       | 5.10 ms                                                                | 5.01 ms: 1.02x faster                                                     |
| thrift                     | 1.24 ms                                                                | 1.22 ms: 1.02x faster                                                     |
| async_tree_io              | 913 ms                                                                 | 898 ms: 1.02x faster                                                      |
| json_loads                 | 28.3 us                                                                | 27.8 us: 1.02x faster                                                     |
| meteor_contest             | 137 ms                                                                 | 135 ms: 1.02x faster                                                      |
| django_template            | 56.5 ms                                                                | 55.6 ms: 1.02x faster                                                     |
| subparsers                 | 33.6 ms                                                                | 33.1 ms: 1.01x faster                                                     |
| async_tree_none_tg         | 378 ms                                                                 | 373 ms: 1.01x faster                                                      |
| json_dumps                 | 14.4 ms                                                                | 14.3 ms: 1.01x faster                                                     |
| async_generators           | 478 ms                                                                 | 471 ms: 1.01x faster                                                      |
| k_core                     | 2.50 sec                                                               | 2.47 sec: 1.01x faster                                                    |
| async_tree_memoization_tg  | 473 ms                                                                 | 467 ms: 1.01x faster                                                      |
| async_tree_io_tg           | 885 ms                                                                 | 874 ms: 1.01x faster                                                      |
| async_tree_none            | 412 ms                                                                 | 407 ms: 1.01x faster                                                      |
| pathlib                    | 20.9 ms                                                                | 20.7 ms: 1.01x faster                                                     |
| regex_compile              | 196 ms                                                                 | 194 ms: 1.01x faster                                                      |
| many_optionals             | 1.39 ms                                                                | 1.37 ms: 1.01x faster                                                     |
| deepcopy                   | 355 us                                                                 | 352 us: 1.01x faster                                                      |
| scimark_monte_carlo        | 121 ms                                                                 | 120 ms: 1.01x faster                                                      |
| docutils                   | 3.23 sec                                                               | 3.21 sec: 1.01x faster                                                    |
| sympy_str                  | 498 ms                                                                 | 495 ms: 1.01x faster                                                      |
| sympy_sum                  | 359 ms                                                                 | 357 ms: 1.01x faster                                                      |
| dulwich_log                | 99.9 ms                                                                | 99.3 ms: 1.01x faster                                                     |
| sqlglot_optimize           | 75.3 ms                                                                | 74.9 ms: 1.01x faster                                                     |
| pyflate                    | 733 ms                                                                 | 728 ms: 1.01x faster                                                      |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                      |
| pprint_pformat             | 2.21 sec                                                               | 2.20 sec: 1.01x faster                                                    |
| sphinx                     | 1.24 sec                                                               | 1.24 sec: 1.01x faster                                                    |
| spectral_norm              | 130 ms                                                                 | 129 ms: 1.01x faster                                                      |
| sympy_expand               | 996 ms                                                                 | 992 ms: 1.00x faster                                                      |
| pprint_safe_repr           | 1.06 sec                                                               | 1.06 sec: 1.00x faster                                                    |
| hexiom                     | 11.1 ms                                                                | 11.2 ms: 1.00x slower                                                     |
| xml_etree_generate         | 103 ms                                                                 | 103 ms: 1.00x slower                                                      |
| 2to3                       | 378 ms                                                                 | 379 ms: 1.00x slower                                                      |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x slower                                                     |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                     |
| crypto_pyaes               | 102 ms                                                                 | 103 ms: 1.00x slower                                                      |
| shortest_path              | 563 ms                                                                 | 566 ms: 1.01x slower                                                      |
| scimark_lu                 | 202 ms                                                                 | 203 ms: 1.01x slower                                                      |
| comprehensions             | 28.5 us                                                                | 28.7 us: 1.01x slower                                                     |
| bpe_tokeniser              | 5.54 sec                                                               | 5.59 sec: 1.01x slower                                                    |
| xml_etree_iterparse        | 95.0 ms                                                                | 95.9 ms: 1.01x slower                                                     |
| xml_etree_parse            | 131 ms                                                                 | 132 ms: 1.01x slower                                                      |
| telco                      | 8.90 ms                                                                | 8.99 ms: 1.01x slower                                                     |
| richards_super             | 96.9 ms                                                                | 97.9 ms: 1.01x slower                                                     |
| deepcopy_memo              | 43.6 us                                                                | 44.1 us: 1.01x slower                                                     |
| mako                       | 19.5 ms                                                                | 19.8 ms: 1.01x slower                                                     |
| pidigits                   | 181 ms                                                                 | 184 ms: 1.02x slower                                                      |
| regex_v8                   | 24.3 ms                                                                | 24.7 ms: 1.02x slower                                                     |
| richards                   | 80.6 ms                                                                | 82.1 ms: 1.02x slower                                                     |
| coroutines                 | 27.0 ms                                                                | 27.6 ms: 1.02x slower                                                     |
| create_gc_cycles           | 1.82 ms                                                                | 1.85 ms: 1.02x slower                                                     |
| unpickle_pure_python       | 363 us                                                                 | 370 us: 1.02x slower                                                      |
| regex_effbot               | 2.77 ms                                                                | 2.84 ms: 1.02x slower                                                     |
| logging_silent             | 189 ns                                                                 | 196 ns: 1.03x slower                                                      |
| pickle_pure_python         | 539 us                                                                 | 561 us: 1.04x slower                                                      |
| gc_traversal               | 3.20 ms                                                                | 3.52 ms: 1.10x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (21): pylint, scimark_sor, scimark_sparse_mat_mult, bench_thread_pool, pycparser, sqlglot_normalize, deltablue, raytrace, go, scimark_fft, xml_etree_process, mdp, float, chaos, logging_format, tomli_loads, sqlglot_parse, bench_mp_pool, typing_runtime_protocols, connected_components, sqlglot_transpile

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x