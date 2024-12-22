# Results vs. base

- fork: Yhg1s
- ref: optimise_recursive_c
- machine: linux-x86_64
- commit hash: b28153d
- commit date: 2024-12-20
- overall geometric mean: 1.024x faster
- HPT reliability: 99.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 360 ms                                                                 | 350 ms: 1.03x faster                                                  |
| docutils       | 3.05 sec                                                               | 3.00 sec: 1.02x faster                                                |
| html5lib       | 91.4 ms                                                                | 90.2 ms: 1.01x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 352 ms                                                                 | 351 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 575 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed    | 598 ms                                                                 | 601 ms: 1.01x slower                                                  |
| coroutines                 | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_memoization_tg, async_generators, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 113 ms                                                                 | 112 ms: 1.01x faster                                                  |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| nbody          | 127 ms                                                                 | 133 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_compile, regex_dna, regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps          | 14.3 ms                                                                | 14.0 ms: 1.02x faster                                                 |
| xml_etree_process   | 73.4 ms                                                                | 73.0 ms: 1.01x faster                                                 |
| xml_etree_iterparse | 90.4 ms                                                                | 90.1 ms: 1.00x faster                                                 |
| xml_etree_parse     | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (5): tomli_loads, pickle_pure_python, xml_etree_generate, json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 15.7 ms: 1.10x faster                                                 |
| python_startup_no_site | 10.2 ms                                                                | 9.79 ms: 1.04x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.6 ms                                                                | 48.6 ms: 1.02x faster                                                 |
| mako            | 17.1 ms                                                                | 17.0 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sympy_sum                  | 349 ms                                                                 | 195 ms: 1.79x faster                                                  |
| sympy_expand               | 951 ms                                                                 | 591 ms: 1.61x faster                                                  |
| sympy_str                  | 478 ms                                                                 | 359 ms: 1.33x faster                                                  |
| sympy_integrate            | 29.6 ms                                                                | 25.3 ms: 1.17x faster                                                 |
| python_startup             | 17.2 ms                                                                | 15.7 ms: 1.10x faster                                                 |
| sqlalchemy_declarative     | 197 ms                                                                 | 182 ms: 1.08x faster                                                  |
| bench_mp_pool              | 108 ms                                                                 | 100 ms: 1.07x faster                                                  |
| deltablue                  | 7.67 ms                                                                | 7.31 ms: 1.05x faster                                                 |
| pylint                     | 365 ms                                                                 | 349 ms: 1.05x faster                                                  |
| python_startup_no_site     | 10.2 ms                                                                | 9.79 ms: 1.04x faster                                                 |
| richards                   | 69.1 ms                                                                | 66.6 ms: 1.04x faster                                                 |
| go                         | 244 ms                                                                 | 236 ms: 1.03x faster                                                  |
| 2to3                       | 360 ms                                                                 | 350 ms: 1.03x faster                                                  |
| raytrace                   | 497 ms                                                                 | 483 ms: 1.03x faster                                                  |
| coverage                   | 102 ms                                                                 | 99.3 ms: 1.03x faster                                                 |
| scimark_fft                | 388 ms                                                                 | 379 ms: 1.02x faster                                                  |
| scimark_sor                | 219 ms                                                                 | 214 ms: 1.02x faster                                                  |
| chaos                      | 96.1 ms                                                                | 93.9 ms: 1.02x faster                                                 |
| richards_super             | 76.4 ms                                                                | 74.7 ms: 1.02x faster                                                 |
| json_dumps                 | 14.3 ms                                                                | 14.0 ms: 1.02x faster                                                 |
| comprehensions             | 27.9 us                                                                | 27.3 us: 1.02x faster                                                 |
| generators                 | 38.4 ms                                                                | 37.7 ms: 1.02x faster                                                 |
| django_template            | 49.6 ms                                                                | 48.6 ms: 1.02x faster                                                 |
| logging_silent             | 184 ns                                                                 | 180 ns: 1.02x faster                                                  |
| scimark_lu                 | 158 ms                                                                 | 155 ms: 1.02x faster                                                  |
| docutils                   | 3.05 sec                                                               | 3.00 sec: 1.02x faster                                                |
| hexiom                     | 9.66 ms                                                                | 9.52 ms: 1.02x faster                                                 |
| thrift                     | 1.00 ms                                                                | 990 us: 1.01x faster                                                  |
| scimark_monte_carlo        | 107 ms                                                                 | 105 ms: 1.01x faster                                                  |
| pathlib                    | 19.8 ms                                                                | 19.5 ms: 1.01x faster                                                 |
| sqlglot_parse              | 2.38 ms                                                                | 2.34 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.14 us                                                                | 2.12 us: 1.01x faster                                                 |
| sqlglot_transpile          | 2.73 ms                                                                | 2.69 ms: 1.01x faster                                                 |
| html5lib                   | 91.4 ms                                                                | 90.2 ms: 1.01x faster                                                 |
| json                       | 5.04 ms                                                                | 4.98 ms: 1.01x faster                                                 |
| logging_simple             | 9.21 us                                                                | 9.10 us: 1.01x faster                                                 |
| many_optionals             | 1.25 ms                                                                | 1.24 ms: 1.01x faster                                                 |
| pyflate                    | 655 ms                                                                 | 648 ms: 1.01x faster                                                  |
| float                      | 113 ms                                                                 | 112 ms: 1.01x faster                                                  |
| sphinx                     | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                                |
| deepcopy_reduce            | 3.40 us                                                                | 3.38 us: 1.01x faster                                                 |
| subparsers                 | 28.9 ms                                                                | 28.7 ms: 1.01x faster                                                 |
| mako                       | 17.1 ms                                                                | 17.0 ms: 1.01x faster                                                 |
| xml_etree_process          | 73.4 ms                                                                | 73.0 ms: 1.01x faster                                                 |
| async_tree_none            | 352 ms                                                                 | 351 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 90.4 ms                                                                | 90.1 ms: 1.00x faster                                                 |
| pidigits                   | 181 ms                                                                 | 181 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 575 ms: 1.00x slower                                                  |
| pprint_pformat             | 1.99 sec                                                               | 2.00 sec: 1.00x slower                                                |
| fannkuch                   | 490 ms                                                                 | 493 ms: 1.00x slower                                                  |
| sqlglot_normalize          | 133 ms                                                                 | 133 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 598 ms                                                                 | 601 ms: 1.01x slower                                                  |
| bench_thread_pool          | 3.38 ms                                                                | 3.39 ms: 1.01x slower                                                 |
| bpe_tokeniser              | 4.99 sec                                                               | 5.02 sec: 1.01x slower                                                |
| dulwich_log                | 90.1 ms                                                                | 90.7 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 956 ms                                                                 | 963 ms: 1.01x slower                                                  |
| spectral_norm              | 111 ms                                                                 | 111 ms: 1.01x slower                                                  |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| coroutines                 | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 5.47 ms                                                                | 5.53 ms: 1.01x slower                                                 |
| nqueens                    | 98.0 ms                                                                | 99.1 ms: 1.01x slower                                                 |
| deepcopy_memo              | 39.9 us                                                                | 40.6 us: 1.02x slower                                                 |
| create_gc_cycles           | 1.79 ms                                                                | 1.84 ms: 1.03x slower                                                 |
| nbody                      | 127 ms                                                                 | 133 ms: 1.05x slower                                                  |
| gc_traversal               | 3.26 ms                                                                | 3.51 ms: 1.08x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (31): regex_compile, connected_components, shortest_path, tomli_loads, logging_format, pickle_pure_python, async_tree_memoization, genshi_xml, xml_etree_generate, async_tree_io, json_loads, genshi_text, async_tree_none_tg, deepcopy, unpickle_pure_python, async_tree_memoization_tg, crypto_pyaes, regex_dna, mdp, async_generators, regex_effbot, sqlglot_optimize, telco, asyncio_websockets, async_tree_io_tg, k_core, meteor_contest, sqlalchemy_imperative, pycparser, regex_v8, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 99.39% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x