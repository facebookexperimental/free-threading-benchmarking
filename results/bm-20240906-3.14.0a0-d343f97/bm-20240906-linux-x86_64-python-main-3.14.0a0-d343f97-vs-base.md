# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d343f97
- commit date: 2024-09-06
- overall geometric mean: 1.00x faster
- HPT reliability: 79.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| html5lib       | 94.5 ms                                                               | 89.1 ms: 1.06x faster                                 |
| Geometric mean | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| asyncio_tcp_ssl        | 2.90 sec                                                              | 2.99 sec: 1.03x slower                                |
| async_tree_none_tg     | 494 ms                                                                | 519 ms: 1.05x slower                                  |
| async_tree_memoization | 647 ms                                                                | 686 ms: 1.06x slower                                  |
| Geometric mean         | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (10): async_tree_none, async_tree_io, async_generators, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_cpu_io_mixed_tg, asyncio_tcp, coroutines, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 36.2 ms                                                               | 32.1 ms: 1.13x faster                                 |
| regex_effbot   | 5.19 ms                                                               | 4.96 ms: 1.05x faster                                 |
| Geometric mean | (ref)                                                                 | 1.05x faster                                          |

Benchmark hidden because not significant (2): regex_dna, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse     | 253 ms                                                                | 233 ms: 1.08x faster                                  |
| xml_etree_iterparse | 182 ms                                                                | 170 ms: 1.07x faster                                  |
| json_dumps          | 15.4 ms                                                               | 14.4 ms: 1.07x faster                                 |
| tomli_loads         | 2.72 sec                                                              | 2.84 sec: 1.04x slower                                |
| pickle              | 15.5 us                                                               | 16.6 us: 1.07x slower                                 |
| pickle_dict         | 45.7 us                                                               | 49.2 us: 1.08x slower                                 |
| json_loads          | 37.8 us                                                               | 41.2 us: 1.09x slower                                 |
| pickle_pure_python  | 418 us                                                                | 458 us: 1.10x slower                                  |
| Geometric mean      | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (6): xml_etree_process, unpickle, xml_etree_generate, unpickle_pure_python, unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 31.2 ms                                                               | 34.1 ms: 1.09x slower                                 |
| Geometric mean | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (3): mako, django_template, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|-------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool           | 26.6 ms                                                               | 22.8 ms: 1.16x faster                                 |
| unpack_sequence         | 72.4 ns                                                               | 62.2 ns: 1.16x faster                                 |
| deepcopy_reduce         | 4.09 us                                                               | 3.61 us: 1.14x faster                                 |
| regex_v8                | 36.2 ms                                                               | 32.1 ms: 1.13x faster                                 |
| xml_etree_parse         | 253 ms                                                                | 233 ms: 1.08x faster                                  |
| sympy_str               | 402 ms                                                                | 373 ms: 1.08x faster                                  |
| thrift                  | 1.17 ms                                                               | 1.09 ms: 1.08x faster                                 |
| hexiom                  | 9.21 ms                                                               | 8.58 ms: 1.07x faster                                 |
| xml_etree_iterparse     | 182 ms                                                                | 170 ms: 1.07x faster                                  |
| pycparser               | 1.79 sec                                                              | 1.67 sec: 1.07x faster                                |
| json_dumps              | 15.4 ms                                                               | 14.4 ms: 1.07x faster                                 |
| pyflate                 | 735 ms                                                                | 690 ms: 1.07x faster                                  |
| deepcopy                | 362 us                                                                | 341 us: 1.06x faster                                  |
| html5lib                | 94.5 ms                                                               | 89.1 ms: 1.06x faster                                 |
| regex_effbot            | 5.19 ms                                                               | 4.96 ms: 1.05x faster                                 |
| richards                | 66.0 ms                                                               | 63.3 ms: 1.04x faster                                 |
| asyncio_tcp_ssl         | 2.90 sec                                                              | 2.99 sec: 1.03x slower                                |
| mdp                     | 3.93 sec                                                              | 4.09 sec: 1.04x slower                                |
| comprehensions          | 22.1 us                                                               | 23.0 us: 1.04x slower                                 |
| tomli_loads             | 2.72 sec                                                              | 2.84 sec: 1.04x slower                                |
| async_tree_none_tg      | 494 ms                                                                | 519 ms: 1.05x slower                                  |
| scimark_lu              | 149 ms                                                                | 156 ms: 1.05x slower                                  |
| async_tree_memoization  | 647 ms                                                                | 686 ms: 1.06x slower                                  |
| scimark_fft             | 470 ms                                                                | 499 ms: 1.06x slower                                  |
| pickle                  | 15.5 us                                                               | 16.6 us: 1.07x slower                                 |
| pickle_dict             | 45.7 us                                                               | 49.2 us: 1.08x slower                                 |
| sqlglot_parse           | 1.87 ms                                                               | 2.03 ms: 1.09x slower                                 |
| json_loads              | 37.8 us                                                               | 41.2 us: 1.09x slower                                 |
| genshi_text             | 31.2 ms                                                               | 34.1 ms: 1.09x slower                                 |
| pickle_pure_python      | 418 us                                                                | 458 us: 1.10x slower                                  |
| logging_format          | 9.69 us                                                               | 10.7 us: 1.11x slower                                 |
| scimark_sparse_mat_mult | 6.13 ms                                                               | 6.93 ms: 1.13x slower                                 |
| Geometric mean          | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (65): dulwich_log, nbody, deltablue, xml_etree_process, float, typing_runtime_protocols, async_tree_none, regex_dna, unpickle, coverage, sqlglot_transpile, sqlglot_normalize, pidigits, docutils, fannkuch, async_tree_io, xml_etree_generate, crypto_pyaes, pathlib, sympy_expand, python_startup, unpickle_pure_python, chaos, sqlglot_optimize, async_generators, 2to3, bench_thread_pool, pylint, async_tree_cpu_io_mixed, pprint_pformat, spectral_norm, sympy_integrate, meteor_contest, sqlite_synth, create_gc_cycles, asyncio_websockets, deepcopy_memo, python_startup_no_site, raytrace, pprint_safe_repr, scimark_sor, bpe_tokeniser, go, async_tree_cpu_io_mixed_tg, json, generators, nqueens, regex_compile, logging_silent, unpickle_list, asyncio_tcp, logging_simple, mako, gc_traversal, scimark_monte_carlo, tornado_http, telco, coroutines, django_template, async_tree_memoization_tg, richards_super, pickle_list, async_tree_io_tg, genshi_xml, sympy_sum

# HPT report

- Reliability score: 79.86% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x