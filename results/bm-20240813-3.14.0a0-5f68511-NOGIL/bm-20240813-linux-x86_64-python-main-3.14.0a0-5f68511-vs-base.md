# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5f68511
- commit date: 2024-08-13
- overall geometric mean: 1.02x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| docutils       | 4.97 sec                                                              | 5.15 sec: 1.04x slower                                |
| Geometric mean | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg | 707 ms                                                                | 671 ms: 1.05x faster                                  |
| async_tree_cpu_io_mixed   | 991 ms                                                                | 945 ms: 1.05x faster                                  |
| async_tree_io_tg          | 1.22 sec                                                              | 1.17 sec: 1.05x faster                                |
| asyncio_websockets        | 753 ms                                                                | 788 ms: 1.05x slower                                  |
| asyncio_tcp               | 1.08 sec                                                              | 1.17 sec: 1.08x slower                                |
| asyncio_tcp_ssl           | 3.28 sec                                                              | 3.55 sec: 1.08x slower                                |
| async_tree_memoization    | 721 ms                                                                | 787 ms: 1.09x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (6): coroutines, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_generators, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 252 ms                                                                | 242 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_dna, regex_compile, regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 6.64 us                                                               | 6.17 us: 1.08x faster                                 |
| pickle_pure_python   | 763 us                                                                | 803 us: 1.05x slower                                  |
| xml_etree_parse      | 211 ms                                                                | 223 ms: 1.06x slower                                  |
| xml_etree_iterparse  | 158 ms                                                                | 168 ms: 1.07x slower                                  |
| pickle_dict          | 41.6 us                                                               | 45.2 us: 1.09x slower                                 |
| unpickle_pure_python | 547 us                                                                | 619 us: 1.13x slower                                  |
| unpickle_list        | 7.48 us                                                               | 8.50 us: 1.14x slower                                 |
| xml_etree_process    | 120 ms                                                                | 137 ms: 1.14x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.04x slower                                          |

Benchmark hidden because not significant (6): json_dumps, tomli_loads, unpickle, pickle, json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 20.1 ms                                                               | 21.2 ms: 1.06x slower                                 |
| python_startup         | 29.8 ms                                                               | 31.5 ms: 1.06x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.06x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml     | 111 ms                                                                | 117 ms: 1.05x slower                                  |
| Geometric mean | (ref)                                                                 | 1.04x slower                                          |

Benchmark hidden because not significant (3): genshi_text, mako, django_template

All benchmarks:
===============

| Benchmark                 | bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| sqlglot_optimize          | 134 ms                                                                | 124 ms: 1.08x faster                                  |
| pickle_list               | 6.64 us                                                               | 6.17 us: 1.08x faster                                 |
| sqlglot_normalize         | 246 ms                                                                | 231 ms: 1.07x faster                                  |
| async_tree_memoization_tg | 707 ms                                                                | 671 ms: 1.05x faster                                  |
| richards                  | 112 ms                                                                | 106 ms: 1.05x faster                                  |
| async_tree_cpu_io_mixed   | 991 ms                                                                | 945 ms: 1.05x faster                                  |
| async_tree_io_tg          | 1.22 sec                                                              | 1.17 sec: 1.05x faster                                |
| pidigits                  | 252 ms                                                                | 242 ms: 1.04x faster                                  |
| unpack_sequence           | 186 ns                                                                | 180 ns: 1.03x faster                                  |
| docutils                  | 4.97 sec                                                              | 5.15 sec: 1.04x slower                                |
| spectral_norm             | 247 ms                                                                | 258 ms: 1.04x slower                                  |
| asyncio_websockets        | 753 ms                                                                | 788 ms: 1.05x slower                                  |
| bpe_tokeniser             | 10.1 sec                                                              | 10.6 sec: 1.05x slower                                |
| genshi_xml                | 111 ms                                                                | 117 ms: 1.05x slower                                  |
| meteor_contest            | 199 ms                                                                | 210 ms: 1.05x slower                                  |
| go                        | 442 ms                                                                | 465 ms: 1.05x slower                                  |
| pickle_pure_python        | 763 us                                                                | 803 us: 1.05x slower                                  |
| python_startup_no_site    | 20.1 ms                                                               | 21.2 ms: 1.06x slower                                 |
| python_startup            | 29.8 ms                                                               | 31.5 ms: 1.06x slower                                 |
| xml_etree_parse           | 211 ms                                                                | 223 ms: 1.06x slower                                  |
| json                      | 8.07 ms                                                               | 8.55 ms: 1.06x slower                                 |
| comprehensions            | 38.1 us                                                               | 40.4 us: 1.06x slower                                 |
| create_gc_cycles          | 1.89 ms                                                               | 2.01 ms: 1.06x slower                                 |
| xml_etree_iterparse       | 158 ms                                                                | 168 ms: 1.07x slower                                  |
| telco                     | 13.8 ms                                                               | 14.8 ms: 1.07x slower                                 |
| sqlglot_parse             | 3.58 ms                                                               | 3.84 ms: 1.07x slower                                 |
| asyncio_tcp               | 1.08 sec                                                              | 1.17 sec: 1.08x slower                                |
| asyncio_tcp_ssl           | 3.28 sec                                                              | 3.55 sec: 1.08x slower                                |
| pickle_dict               | 41.6 us                                                               | 45.2 us: 1.09x slower                                 |
| async_tree_memoization    | 721 ms                                                                | 787 ms: 1.09x slower                                  |
| nqueens                   | 154 ms                                                                | 170 ms: 1.10x slower                                  |
| bench_thread_pool         | 4.35 ms                                                               | 4.83 ms: 1.11x slower                                 |
| unpickle_pure_python      | 547 us                                                                | 619 us: 1.13x slower                                  |
| unpickle_list             | 7.48 us                                                               | 8.50 us: 1.14x slower                                 |
| xml_etree_process         | 120 ms                                                                | 137 ms: 1.14x slower                                  |
| sympy_integrate           | 44.8 ms                                                               | 51.8 ms: 1.16x slower                                 |
| gc_traversal              | 4.64 ms                                                               | 5.42 ms: 1.17x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (59): coroutines, logging_format, deepcopy_reduce, sqlglot_transpile, html5lib, deepcopy, logging_simple, logging_silent, coverage, json_dumps, nbody, 2to3, pprint_safe_repr, sympy_sum, regex_dna, scimark_lu, pycparser, pprint_pformat, raytrace, tomli_loads, thrift, unpickle, async_tree_io, scimark_fft, hexiom, pyflate, pickle, json_loads, scimark_sparse_mat_mult, pathlib, async_tree_cpu_io_mixed_tg, mdp, chaos, pylint, async_tree_none_tg, tornado_http, regex_compile, generators, scimark_sor, deltablue, xml_etree_generate, fannkuch, genshi_text, async_generators, sympy_expand, mako, typing_runtime_protocols, richards_super, float, regex_effbot, async_tree_none, sqlite_synth, sympy_str, scimark_monte_carlo, crypto_pyaes, regex_v8, deepcopy_memo, django_template, bench_mp_pool

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x