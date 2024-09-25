# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8145ebe
- commit date: 2024-09-12
- overall geometric mean: 1.01x faster
- HPT reliability: 97.21%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 721 ms                                                                | 669 ms: 1.08x faster                                  |
| docutils       | 5.09 sec                                                              | 4.89 sec: 1.04x faster                                |
| html5lib       | 141 ms                                                                | 133 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io              | 1.35 sec                                                              | 1.24 sec: 1.09x faster                                |
| async_tree_io_tg           | 1.26 sec                                                              | 1.17 sec: 1.08x faster                                |
| asyncio_tcp                | 1.19 sec                                                              | 1.10 sec: 1.08x faster                                |
| async_tree_cpu_io_mixed_tg | 906 ms                                                                | 844 ms: 1.07x faster                                  |
| async_tree_none            | 647 ms                                                                | 609 ms: 1.06x faster                                  |
| asyncio_tcp_ssl            | 3.12 sec                                                              | 3.36 sec: 1.08x slower                                |
| Geometric mean             | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_memoization_tg, coroutines, async_tree_none_tg, asyncio_websockets, async_generators, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.89 ms                                                               | 4.42 ms: 1.11x faster                                 |
| regex_compile  | 301 ms                                                                | 288 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_pure_python | 581 us                                                                | 516 us: 1.13x faster                                  |
| unpickle             | 24.2 us                                                               | 22.3 us: 1.08x faster                                 |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (12): json_loads, xml_etree_parse, xml_etree_process, pickle_dict, unpickle_list, json_dumps, pickle_list, pickle_pure_python, tomli_loads, xml_etree_generate, xml_etree_iterparse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 23.8 ms                                                               | 21.3 ms: 1.12x faster                                 |
| python_startup         | 35.1 ms                                                               | 32.2 ms: 1.09x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.10x faster                                          |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_text, django_template, genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| sqlglot_optimize           | 134 ms                                                                | 117 ms: 1.14x faster                                  |
| nqueens                    | 177 ms                                                                | 155 ms: 1.14x faster                                  |
| unpickle_pure_python       | 581 us                                                                | 516 us: 1.13x faster                                  |
| python_startup_no_site     | 23.8 ms                                                               | 21.3 ms: 1.12x faster                                 |
| richards_super             | 137 ms                                                                | 123 ms: 1.11x faster                                  |
| regex_effbot               | 4.89 ms                                                               | 4.42 ms: 1.11x faster                                 |
| logging_simple             | 16.7 us                                                               | 15.2 us: 1.10x faster                                 |
| logging_format             | 17.9 us                                                               | 16.3 us: 1.09x faster                                 |
| unpack_sequence            | 220 ns                                                                | 201 ns: 1.09x faster                                  |
| python_startup             | 35.1 ms                                                               | 32.2 ms: 1.09x faster                                 |
| async_tree_io              | 1.35 sec                                                              | 1.24 sec: 1.09x faster                                |
| comprehensions             | 40.4 us                                                               | 37.2 us: 1.09x faster                                 |
| unpickle                   | 24.2 us                                                               | 22.3 us: 1.08x faster                                 |
| pycparser                  | 2.43 sec                                                              | 2.24 sec: 1.08x faster                                |
| chaos                      | 172 ms                                                                | 159 ms: 1.08x faster                                  |
| async_tree_io_tg           | 1.26 sec                                                              | 1.17 sec: 1.08x faster                                |
| asyncio_tcp                | 1.19 sec                                                              | 1.10 sec: 1.08x faster                                |
| 2to3                       | 721 ms                                                                | 669 ms: 1.08x faster                                  |
| async_tree_cpu_io_mixed_tg | 906 ms                                                                | 844 ms: 1.07x faster                                  |
| scimark_sor                | 367 ms                                                                | 345 ms: 1.07x faster                                  |
| generators                 | 56.1 ms                                                               | 52.8 ms: 1.06x faster                                 |
| spectral_norm              | 260 ms                                                                | 245 ms: 1.06x faster                                  |
| async_tree_none            | 647 ms                                                                | 609 ms: 1.06x faster                                  |
| html5lib                   | 141 ms                                                                | 133 ms: 1.06x faster                                  |
| sqlglot_transpile          | 4.66 ms                                                               | 4.40 ms: 1.06x faster                                 |
| sympy_str                  | 721 ms                                                                | 687 ms: 1.05x faster                                  |
| regex_compile              | 301 ms                                                                | 288 ms: 1.05x faster                                  |
| docutils                   | 5.09 sec                                                              | 4.89 sec: 1.04x faster                                |
| fannkuch                   | 786 ms                                                                | 767 ms: 1.03x faster                                  |
| thrift                     | 1.61 ms                                                               | 1.71 ms: 1.06x slower                                 |
| sympy_sum                  | 460 ms                                                                | 491 ms: 1.07x slower                                  |
| asyncio_tcp_ssl            | 3.12 sec                                                              | 3.36 sec: 1.08x slower                                |
| gc_traversal               | 4.51 ms                                                               | 4.89 ms: 1.08x slower                                 |
| create_gc_cycles           | 1.83 ms                                                               | 2.04 ms: 1.11x slower                                 |
| bench_thread_pool          | 4.27 ms                                                               | 4.74 ms: 1.11x slower                                 |
| dulwich_log                | 125 ms                                                                | 159 ms: 1.27x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (61): hexiom, telco, pidigits, deepcopy_memo, float, pylint, pathlib, json_loads, deepcopy, logging_silent, regex_dna, xml_etree_parse, pyflate, xml_etree_process, pprint_pformat, json, nbody, crypto_pyaes, pickle_dict, unpickle_list, bpe_tokeniser, json_dumps, scimark_sparse_mat_mult, scimark_fft, pprint_safe_repr, go, genshi_text, sqlite_synth, pickle_list, typing_runtime_protocols, async_tree_memoization, raytrace, async_tree_memoization_tg, mdp, coroutines, richards, async_tree_none_tg, coverage, sympy_expand, asyncio_websockets, tornado_http, pickle_pure_python, scimark_monte_carlo, scimark_lu, tomli_loads, sqlglot_normalize, async_generators, django_template, xml_etree_generate, deltablue, regex_v8, xml_etree_iterparse, pickle, genshi_xml, sympy_integrate, async_tree_cpu_io_mixed, sqlglot_parse, meteor_contest, mako, deepcopy_reduce, bench_mp_pool

# HPT report

- Reliability score: 97.21% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x