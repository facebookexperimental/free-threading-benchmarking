# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: e7db011
- commit date: 2025-02-19
- overall geometric mean: 1.003x slower
- HPT reliability: 92.01%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 302 ms                                                                 | 303 ms: 1.00x slower                                              |
| docutils       | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                            |
| html5lib       | 72.1 ms                                                                | 71.5 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 23.8 ms                                                                | 23.1 ms: 1.03x faster                                             |
| async_tree_cpu_io_mixed    | 547 ms                                                                 | 540 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 513 ms                                                                 | 508 ms: 1.01x faster                                              |
| async_generators           | 374 ms                                                                 | 370 ms: 1.01x faster                                              |
| async_tree_memoization     | 352 ms                                                                 | 354 ms: 1.01x slower                                              |
| async_tree_io_tg           | 574 ms                                                                 | 579 ms: 1.01x slower                                              |
| async_tree_none_tg         | 248 ms                                                                 | 252 ms: 1.01x slower                                              |
| async_tree_none            | 286 ms                                                                 | 291 ms: 1.02x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (3): async_tree_io, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 198 ms: 1.01x faster                                              |
| float          | 75.8 ms                                                                | 77.2 ms: 1.02x slower                                             |
| nbody          | 129 ms                                                                 | 133 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 184 ms: 1.01x slower                                              |
| regex_compile  | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| regex_v8       | 23.6 ms                                                                | 24.2 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 252 us                                                                 | 249 us: 1.01x faster                                              |
| xml_etree_process    | 70.3 ms                                                                | 69.6 ms: 1.01x faster                                             |
| xml_etree_generate   | 96.6 ms                                                                | 95.9 ms: 1.01x faster                                             |
| tomli_loads          | 2.32 sec                                                               | 2.33 sec: 1.01x slower                                            |
| json_loads           | 31.2 us                                                                | 31.5 us: 1.01x slower                                             |
| pickle_pure_python   | 360 us                                                                 | 363 us: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (3): json_dumps, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| python_startup_no_site | 9.62 ms                                                                | 9.69 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako           | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (3): django_template, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e7db011 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| logging_silent             | 114 ns                                                                 | 110 ns: 1.04x faster                                              |
| coroutines                 | 23.8 ms                                                                | 23.1 ms: 1.03x faster                                             |
| scimark_sor                | 132 ms                                                                 | 130 ms: 1.02x faster                                              |
| pyflate                    | 496 ms                                                                 | 487 ms: 1.02x faster                                              |
| thrift                     | 893 us                                                                 | 879 us: 1.02x faster                                              |
| deepcopy_memo              | 38.4 us                                                                | 37.8 us: 1.01x faster                                             |
| fannkuch                   | 492 ms                                                                 | 485 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed    | 547 ms                                                                 | 540 ms: 1.01x faster                                              |
| docutils                   | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                            |
| unpickle_pure_python       | 252 us                                                                 | 249 us: 1.01x faster                                              |
| deepcopy                   | 310 us                                                                 | 306 us: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 513 ms                                                                 | 508 ms: 1.01x faster                                              |
| async_generators           | 374 ms                                                                 | 370 ms: 1.01x faster                                              |
| deepcopy_reduce            | 3.18 us                                                                | 3.15 us: 1.01x faster                                             |
| xml_etree_process          | 70.3 ms                                                                | 69.6 ms: 1.01x faster                                             |
| hexiom                     | 7.41 ms                                                                | 7.35 ms: 1.01x faster                                             |
| comprehensions             | 19.9 us                                                                | 19.7 us: 1.01x faster                                             |
| shortest_path              | 550 ms                                                                 | 546 ms: 1.01x faster                                              |
| xml_etree_generate         | 96.6 ms                                                                | 95.9 ms: 1.01x faster                                             |
| json                       | 5.41 ms                                                                | 5.37 ms: 1.01x faster                                             |
| html5lib                   | 72.1 ms                                                                | 71.5 ms: 1.01x faster                                             |
| pidigits                   | 199 ms                                                                 | 198 ms: 1.01x faster                                              |
| chaos                      | 70.0 ms                                                                | 69.7 ms: 1.00x faster                                             |
| sqlalchemy_declarative     | 157 ms                                                                 | 157 ms: 1.00x faster                                              |
| scimark_monte_carlo        | 82.6 ms                                                                | 82.3 ms: 1.00x faster                                             |
| sqlglot_normalize          | 120 ms                                                                 | 120 ms: 1.00x faster                                              |
| bpe_tokeniser              | 4.68 sec                                                               | 4.67 sec: 1.00x faster                                            |
| 2to3                       | 302 ms                                                                 | 303 ms: 1.00x slower                                              |
| mako                       | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                             |
| pathlib                    | 19.8 ms                                                                | 19.9 ms: 1.00x slower                                             |
| go                         | 140 ms                                                                 | 140 ms: 1.00x slower                                              |
| create_gc_cycles           | 1.37 ms                                                                | 1.38 ms: 1.00x slower                                             |
| coverage                   | 97.9 ms                                                                | 98.4 ms: 1.01x slower                                             |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| tomli_loads                | 2.32 sec                                                               | 2.33 sec: 1.01x slower                                            |
| async_tree_memoization     | 352 ms                                                                 | 354 ms: 1.01x slower                                              |
| bench_mp_pool              | 94.9 ms                                                                | 95.5 ms: 1.01x slower                                             |
| python_startup_no_site     | 9.62 ms                                                                | 9.69 ms: 1.01x slower                                             |
| json_loads                 | 31.2 us                                                                | 31.5 us: 1.01x slower                                             |
| pickle_pure_python         | 360 us                                                                 | 363 us: 1.01x slower                                              |
| crypto_pyaes               | 87.2 ms                                                                | 87.8 ms: 1.01x slower                                             |
| sympy_integrate            | 24.1 ms                                                                | 24.3 ms: 1.01x slower                                             |
| regex_dna                  | 183 ms                                                                 | 184 ms: 1.01x slower                                              |
| regex_compile              | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| pprint_safe_repr           | 825 ms                                                                 | 833 ms: 1.01x slower                                              |
| async_tree_io_tg           | 574 ms                                                                 | 579 ms: 1.01x slower                                              |
| dulwich_log                | 82.7 ms                                                                | 83.5 ms: 1.01x slower                                             |
| sympy_expand               | 546 ms                                                                 | 553 ms: 1.01x slower                                              |
| pprint_pformat             | 1.70 sec                                                               | 1.72 sec: 1.01x slower                                            |
| sympy_str                  | 334 ms                                                                 | 338 ms: 1.01x slower                                              |
| meteor_contest             | 130 ms                                                                 | 132 ms: 1.01x slower                                              |
| sqlalchemy_imperative      | 23.8 ms                                                                | 24.2 ms: 1.01x slower                                             |
| async_tree_none_tg         | 248 ms                                                                 | 252 ms: 1.01x slower                                              |
| subparsers                 | 25.4 ms                                                                | 25.8 ms: 1.01x slower                                             |
| sqlglot_transpile          | 1.91 ms                                                                | 1.94 ms: 1.01x slower                                             |
| scimark_fft                | 386 ms                                                                 | 392 ms: 1.02x slower                                              |
| sqlite_synth               | 2.03 us                                                                | 2.06 us: 1.02x slower                                             |
| many_optionals             | 1.18 ms                                                                | 1.20 ms: 1.02x slower                                             |
| logging_format             | 8.13 us                                                                | 8.27 us: 1.02x slower                                             |
| sqlglot_parse              | 1.58 ms                                                                | 1.61 ms: 1.02x slower                                             |
| raytrace                   | 324 ms                                                                 | 330 ms: 1.02x slower                                              |
| async_tree_none            | 286 ms                                                                 | 291 ms: 1.02x slower                                              |
| float                      | 75.8 ms                                                                | 77.2 ms: 1.02x slower                                             |
| regex_v8                   | 23.6 ms                                                                | 24.2 ms: 1.03x slower                                             |
| logging_simple             | 7.06 us                                                                | 7.28 us: 1.03x slower                                             |
| nbody                      | 129 ms                                                                 | 133 ms: 1.03x slower                                              |
| mdp                        | 2.61 sec                                                               | 2.71 sec: 1.04x slower                                            |
| scimark_sparse_mat_mult    | 5.48 ms                                                                | 5.77 ms: 1.05x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (28): typing_runtime_protocols, sphinx, connected_components, pycparser, spectral_norm, deltablue, sympy_sum, richards, generators, richards_super, json_dumps, sqlglot_optimize, xml_etree_iterparse, xml_etree_parse, django_template, nqueens, regex_effbot, gc_traversal, k_core, genshi_text, bench_thread_pool, scimark_lu, async_tree_io, asyncio_websockets, telco, async_tree_memoization_tg, genshi_xml, pylint

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 92.01% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x