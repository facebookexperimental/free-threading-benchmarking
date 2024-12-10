# Results vs. base

- fork: colesbury
- ref: stackpointer
- machine: linux-x86_64
- commit hash: bba99b4
- commit date: 2024-12-09
- overall geometric mean: 1.008x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 369 ms                                                                 | 372 ms: 1.01x slower                                              |
| docutils       | 3.08 sec                                                               | 3.11 sec: 1.01x slower                                            |
| html5lib       | 97.0 ms                                                                | 98.0 ms: 1.01x slower                                             |
| sphinx         | 1.19 sec                                                               | 1.20 sec: 1.01x slower                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 829 ms                                                                 | 838 ms: 1.01x slower                                              |
| async_tree_io              | 853 ms                                                                 | 864 ms: 1.01x slower                                              |
| async_tree_memoization     | 475 ms                                                                 | 482 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 642 ms                                                                 | 654 ms: 1.02x slower                                              |
| async_tree_none_tg         | 359 ms                                                                 | 366 ms: 1.02x slower                                              |
| async_tree_cpu_io_mixed_tg | 614 ms                                                                 | 627 ms: 1.02x slower                                              |
| async_tree_memoization_tg  | 449 ms                                                                 | 460 ms: 1.03x slower                                              |
| coroutines                 | 24.5 ms                                                                | 25.1 ms: 1.03x slower                                             |
| async_generators           | 457 ms                                                                 | 469 ms: 1.03x slower                                              |
| async_tree_none            | 388 ms                                                                 | 399 ms: 1.03x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 140 ms                                                                 | 142 ms: 1.01x slower                                              |
| pidigits       | 181 ms                                                                 | 184 ms: 1.01x slower                                              |
| nbody          | 131 ms                                                                 | 134 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.3 ms                                                                | 24.1 ms: 1.01x faster                                             |
| regex_compile  | 181 ms                                                                 | 185 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_loads           | 28.4 us                                                                | 28.6 us: 1.00x slower                                             |
| xml_etree_iterparse  | 91.0 ms                                                                | 91.5 ms: 1.00x slower                                             |
| json_dumps           | 14.2 ms                                                                | 14.3 ms: 1.01x slower                                             |
| pickle_pure_python   | 515 us                                                                 | 520 us: 1.01x slower                                              |
| unpickle_pure_python | 336 us                                                                 | 339 us: 1.01x slower                                              |
| xml_etree_generate   | 98.2 ms                                                                | 99.5 ms: 1.01x slower                                             |
| tomli_loads          | 2.66 sec                                                               | 2.72 sec: 1.02x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup | 17.5 ms                                                                | 17.4 ms: 1.00x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 52.1 ms                                                                | 51.5 ms: 1.01x faster                                             |
| genshi_text     | 31.7 ms                                                                | 32.3 ms: 1.02x slower                                             |
| mako            | 17.8 ms                                                                | 18.2 ms: 1.02x slower                                             |
| genshi_xml      | 63.8 ms                                                                | 66.0 ms: 1.03x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| scimark_monte_carlo        | 126 ms                                                                 | 121 ms: 1.05x faster                                              |
| gc_traversal               | 3.27 ms                                                                | 3.17 ms: 1.03x faster                                             |
| spectral_norm              | 125 ms                                                                 | 123 ms: 1.02x faster                                              |
| raytrace                   | 565 ms                                                                 | 555 ms: 1.02x faster                                              |
| go                         | 278 ms                                                                 | 274 ms: 1.01x faster                                              |
| json                       | 5.14 ms                                                                | 5.07 ms: 1.01x faster                                             |
| scimark_lu                 | 186 ms                                                                 | 184 ms: 1.01x faster                                              |
| django_template            | 52.1 ms                                                                | 51.5 ms: 1.01x faster                                             |
| deltablue                  | 8.28 ms                                                                | 8.21 ms: 1.01x faster                                             |
| regex_v8                   | 24.3 ms                                                                | 24.1 ms: 1.01x faster                                             |
| thrift                     | 1.17 ms                                                                | 1.16 ms: 1.01x faster                                             |
| chaos                      | 107 ms                                                                 | 106 ms: 1.01x faster                                              |
| python_startup             | 17.5 ms                                                                | 17.4 ms: 1.00x faster                                             |
| sqlalchemy_declarative     | 205 ms                                                                 | 205 ms: 1.00x slower                                              |
| sympy_sum                  | 350 ms                                                                 | 352 ms: 1.00x slower                                              |
| json_loads                 | 28.4 us                                                                | 28.6 us: 1.00x slower                                             |
| xml_etree_iterparse        | 91.0 ms                                                                | 91.5 ms: 1.00x slower                                             |
| sympy_integrate            | 29.6 ms                                                                | 29.7 ms: 1.01x slower                                             |
| sympy_expand               | 957 ms                                                                 | 963 ms: 1.01x slower                                              |
| k_core                     | 2.42 sec                                                               | 2.43 sec: 1.01x slower                                            |
| bpe_tokeniser              | 5.01 sec                                                               | 5.05 sec: 1.01x slower                                            |
| shortest_path              | 552 ms                                                                 | 555 ms: 1.01x slower                                              |
| sphinx                     | 1.19 sec                                                               | 1.20 sec: 1.01x slower                                            |
| json_dumps                 | 14.2 ms                                                                | 14.3 ms: 1.01x slower                                             |
| 2to3                       | 369 ms                                                                 | 372 ms: 1.01x slower                                              |
| pickle_pure_python         | 515 us                                                                 | 520 us: 1.01x slower                                              |
| unpickle_pure_python       | 336 us                                                                 | 339 us: 1.01x slower                                              |
| many_optionals             | 1.29 ms                                                                | 1.31 ms: 1.01x slower                                             |
| docutils                   | 3.08 sec                                                               | 3.11 sec: 1.01x slower                                            |
| html5lib                   | 97.0 ms                                                                | 98.0 ms: 1.01x slower                                             |
| async_tree_io_tg           | 829 ms                                                                 | 838 ms: 1.01x slower                                              |
| sqlite_synth               | 2.30 us                                                                | 2.32 us: 1.01x slower                                             |
| float                      | 140 ms                                                                 | 142 ms: 1.01x slower                                              |
| connected_components       | 501 ms                                                                 | 507 ms: 1.01x slower                                              |
| sympy_str                  | 476 ms                                                                 | 482 ms: 1.01x slower                                              |
| async_tree_io              | 853 ms                                                                 | 864 ms: 1.01x slower                                              |
| deepcopy_memo              | 40.1 us                                                                | 40.6 us: 1.01x slower                                             |
| xml_etree_generate         | 98.2 ms                                                                | 99.5 ms: 1.01x slower                                             |
| create_gc_cycles           | 1.79 ms                                                                | 1.81 ms: 1.01x slower                                             |
| pidigits                   | 181 ms                                                                 | 184 ms: 1.01x slower                                              |
| async_tree_memoization     | 475 ms                                                                 | 482 ms: 1.01x slower                                              |
| pathlib                    | 20.3 ms                                                                | 20.6 ms: 1.02x slower                                             |
| dulwich_log                | 96.1 ms                                                                | 97.6 ms: 1.02x slower                                             |
| generators                 | 39.1 ms                                                                | 39.8 ms: 1.02x slower                                             |
| nbody                      | 131 ms                                                                 | 134 ms: 1.02x slower                                              |
| sqlglot_optimize           | 69.3 ms                                                                | 70.6 ms: 1.02x slower                                             |
| async_tree_cpu_io_mixed    | 642 ms                                                                 | 654 ms: 1.02x slower                                              |
| telco                      | 8.65 ms                                                                | 8.82 ms: 1.02x slower                                             |
| nqueens                    | 97.7 ms                                                                | 99.5 ms: 1.02x slower                                             |
| async_tree_none_tg         | 359 ms                                                                 | 366 ms: 1.02x slower                                              |
| logging_format             | 12.0 us                                                                | 12.2 us: 1.02x slower                                             |
| pycparser                  | 1.55 sec                                                               | 1.58 sec: 1.02x slower                                            |
| genshi_text                | 31.7 ms                                                                | 32.3 ms: 1.02x slower                                             |
| logging_simple             | 10.8 us                                                                | 11.0 us: 1.02x slower                                             |
| async_tree_cpu_io_mixed_tg | 614 ms                                                                 | 627 ms: 1.02x slower                                              |
| regex_compile              | 181 ms                                                                 | 185 ms: 1.02x slower                                              |
| mako                       | 17.8 ms                                                                | 18.2 ms: 1.02x slower                                             |
| tomli_loads                | 2.66 sec                                                               | 2.72 sec: 1.02x slower                                            |
| crypto_pyaes               | 92.0 ms                                                                | 94.3 ms: 1.02x slower                                             |
| async_tree_memoization_tg  | 449 ms                                                                 | 460 ms: 1.03x slower                                              |
| comprehensions             | 27.2 us                                                                | 27.9 us: 1.03x slower                                             |
| sqlglot_normalize          | 138 ms                                                                 | 142 ms: 1.03x slower                                              |
| coroutines                 | 24.5 ms                                                                | 25.1 ms: 1.03x slower                                             |
| coverage                   | 98.1 ms                                                                | 101 ms: 1.03x slower                                              |
| hexiom                     | 9.85 ms                                                                | 10.1 ms: 1.03x slower                                             |
| async_generators           | 457 ms                                                                 | 469 ms: 1.03x slower                                              |
| pprint_pformat             | 2.03 sec                                                               | 2.08 sec: 1.03x slower                                            |
| async_tree_none            | 388 ms                                                                 | 399 ms: 1.03x slower                                              |
| pprint_safe_repr           | 981 ms                                                                 | 1.01 sec: 1.03x slower                                            |
| typing_runtime_protocols   | 202 us                                                                 | 208 us: 1.03x slower                                              |
| genshi_xml                 | 63.8 ms                                                                | 66.0 ms: 1.03x slower                                             |
| fannkuch                   | 494 ms                                                                 | 514 ms: 1.04x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (24): scimark_sor, logging_silent, xml_etree_parse, sqlalchemy_imperative, pyflate, regex_dna, regex_effbot, python_startup_no_site, bench_mp_pool, sqlglot_transpile, mdp, meteor_contest, deepcopy, xml_etree_process, asyncio_websockets, deepcopy_reduce, bench_thread_pool, sqlglot_parse, richards, scimark_sparse_mat_mult, scimark_fft, richards_super, subparsers, pylint

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x