# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3bd942f
- commit date: 2024-09-11
- overall geometric mean: 1.01x faster
- HPT reliability: 85.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240911-linux-x86_64-python-eb169f40276a86118277-3.14.0a0-eb169f4 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none        | 613 ms                                                                | 575 ms: 1.06x faster                                  |
| async_tree_memoization | 719 ms                                                                | 748 ms: 1.04x slower                                  |
| coroutines             | 42.9 ms                                                               | 45.1 ms: 1.05x slower                                 |
| async_tree_io          | 1.24 sec                                                              | 1.31 sec: 1.06x slower                                |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                          |

Benchmark hidden because not significant (9): async_tree_memoization_tg, async_generators, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io_tg, asyncio_tcp_ssl, async_tree_cpu_io_mixed, asyncio_tcp

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240911-linux-x86_64-python-eb169f40276a86118277-3.14.0a0-eb169f4 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 38.9 ms                                                               | 36.1 ms: 1.08x faster                                 |
| regex_compile  | 275 ms                                                                | 290 ms: 1.05x slower                                  |
| Geometric mean | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark       | bm-20240911-linux-x86_64-python-eb169f40276a86118277-3.14.0a0-eb169f4 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict     | 46.0 us                                                               | 43.5 us: 1.06x faster                                 |
| unpickle        | 21.5 us                                                               | 22.7 us: 1.06x slower                                 |
| json_dumps      | 17.6 ms                                                               | 18.9 ms: 1.08x slower                                 |
| xml_etree_parse | 214 ms                                                                | 235 ms: 1.09x slower                                  |
| Geometric mean  | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (10): xml_etree_process, xml_etree_generate, tomli_loads, json_loads, pickle_list, pickle_pure_python, unpickle_pure_python, unpickle_list, xml_etree_iterparse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240911-linux-x86_64-python-eb169f40276a86118277-3.14.0a0-eb169f4 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 34.5 ms                                                               | 30.9 ms: 1.12x faster                                 |
| python_startup_no_site | 23.7 ms                                                               | 21.2 ms: 1.12x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.12x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240911-linux-x86_64-python-eb169f40276a86118277-3.14.0a0-eb169f4 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 54.4 ms                                                               | 58.2 ms: 1.07x slower                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (3): django_template, genshi_xml, mako

All benchmarks:
===============

| Benchmark               | bm-20240911-linux-x86_64-python-eb169f40276a86118277-3.14.0a0-eb169f4 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpack_sequence         | 231 ns                                                                | 187 ns: 1.23x faster                                  |
| bench_thread_pool       | 5.02 ms                                                               | 4.19 ms: 1.20x faster                                 |
| sqlglot_parse           | 4.18 ms                                                               | 3.50 ms: 1.19x faster                                 |
| richards_super          | 148 ms                                                                | 130 ms: 1.13x faster                                  |
| python_startup          | 34.5 ms                                                               | 30.9 ms: 1.12x faster                                 |
| python_startup_no_site  | 23.7 ms                                                               | 21.2 ms: 1.12x faster                                 |
| scimark_fft             | 649 ms                                                                | 587 ms: 1.11x faster                                  |
| thrift                  | 1.82 ms                                                               | 1.65 ms: 1.10x faster                                 |
| scimark_sor             | 371 ms                                                                | 337 ms: 1.10x faster                                  |
| scimark_monte_carlo     | 172 ms                                                                | 157 ms: 1.10x faster                                  |
| scimark_sparse_mat_mult | 9.47 ms                                                               | 8.77 ms: 1.08x faster                                 |
| regex_v8                | 38.9 ms                                                               | 36.1 ms: 1.08x faster                                 |
| sympy_sum               | 499 ms                                                                | 464 ms: 1.07x faster                                  |
| gc_traversal            | 4.84 ms                                                               | 4.51 ms: 1.07x faster                                 |
| richards                | 112 ms                                                                | 105 ms: 1.07x faster                                  |
| async_tree_none         | 613 ms                                                                | 575 ms: 1.06x faster                                  |
| generators              | 58.3 ms                                                               | 54.8 ms: 1.06x faster                                 |
| telco                   | 14.9 ms                                                               | 14.0 ms: 1.06x faster                                 |
| pickle_dict             | 46.0 us                                                               | 43.5 us: 1.06x faster                                 |
| coverage                | 155 ms                                                                | 147 ms: 1.05x faster                                  |
| deltablue               | 11.5 ms                                                               | 10.9 ms: 1.05x faster                                 |
| meteor_contest          | 196 ms                                                                | 186 ms: 1.05x faster                                  |
| logging_format          | 16.7 us                                                               | 16.0 us: 1.04x faster                                 |
| sympy_integrate         | 45.7 ms                                                               | 43.8 ms: 1.04x faster                                 |
| deepcopy_reduce         | 6.12 us                                                               | 5.88 us: 1.04x faster                                 |
| bpe_tokeniser           | 9.78 sec                                                              | 10.0 sec: 1.03x slower                                |
| async_tree_memoization  | 719 ms                                                                | 748 ms: 1.04x slower                                  |
| sympy_expand            | 1.30 sec                                                              | 1.36 sec: 1.05x slower                                |
| coroutines              | 42.9 ms                                                               | 45.1 ms: 1.05x slower                                 |
| regex_compile           | 275 ms                                                                | 290 ms: 1.05x slower                                  |
| unpickle                | 21.5 us                                                               | 22.7 us: 1.06x slower                                 |
| async_tree_io           | 1.24 sec                                                              | 1.31 sec: 1.06x slower                                |
| go                      | 348 ms                                                                | 369 ms: 1.06x slower                                  |
| genshi_text             | 54.4 ms                                                               | 58.2 ms: 1.07x slower                                 |
| logging_silent          | 254 ns                                                                | 272 ns: 1.07x slower                                  |
| pathlib                 | 34.2 ms                                                               | 36.6 ms: 1.07x slower                                 |
| deepcopy_memo           | 68.7 us                                                               | 73.7 us: 1.07x slower                                 |
| json_dumps              | 17.6 ms                                                               | 18.9 ms: 1.08x slower                                 |
| xml_etree_parse         | 214 ms                                                                | 235 ms: 1.09x slower                                  |
| bench_mp_pool           | 13.1 ms                                                               | 17.5 ms: 1.33x slower                                 |
| Geometric mean          | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (57): chaos, sqlglot_optimize, spectral_norm, sqlglot_normalize, deepcopy, regex_effbot, pylint, regex_dna, sympy_str, 2to3, float, async_tree_memoization_tg, async_generators, asyncio_websockets, xml_etree_process, dulwich_log, tornado_http, django_template, xml_etree_generate, raytrace, create_gc_cycles, json, mdp, fannkuch, async_tree_cpu_io_mixed_tg, typing_runtime_protocols, tomli_loads, nqueens, json_loads, pprint_safe_repr, async_tree_none_tg, async_tree_io_tg, scimark_lu, genshi_xml, mako, sqlite_synth, asyncio_tcp_ssl, async_tree_cpu_io_mixed, hexiom, logging_simple, pprint_pformat, pycparser, pickle_list, docutils, pickle_pure_python, unpickle_pure_python, unpickle_list, asyncio_tcp, pidigits, pyflate, crypto_pyaes, sqlglot_transpile, html5lib, nbody, xml_etree_iterparse, comprehensions, pickle

# HPT report

- Reliability score: 85.70% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x