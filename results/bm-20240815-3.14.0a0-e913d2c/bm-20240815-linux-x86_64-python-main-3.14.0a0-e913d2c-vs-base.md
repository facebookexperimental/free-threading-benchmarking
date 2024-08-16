# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e913d2c
- commit date: 2024-08-15
- overall geometric mean: 1.00x slower
- HPT reliability: 54.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| html5lib       | 89.2 ms                                                               | 93.8 ms: 1.05x slower                                 |
| tornado_http   | 275 ms                                                                | 241 ms: 1.14x faster                                  |
| Geometric mean | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization | 722 ms                                                                | 670 ms: 1.08x faster                                  |
| asyncio_websockets     | 762 ms                                                                | 734 ms: 1.04x faster                                  |
| async_generators       | 594 ms                                                                | 574 ms: 1.03x faster                                  |
| asyncio_tcp_ssl        | 2.75 sec                                                              | 2.83 sec: 1.03x slower                                |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (9): async_tree_memoization_tg, async_tree_none_tg, asyncio_tcp, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_none, coroutines, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.87 ms                                                               | 5.30 ms: 1.09x slower                                 |
| regex_v8       | 32.4 ms                                                               | 35.4 ms: 1.09x slower                                 |
| Geometric mean | (ref)                                                                 | 1.04x slower                                          |

Benchmark hidden because not significant (2): regex_dna, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_generate   | 129 ms                                                                | 121 ms: 1.07x faster                                  |
| json_loads           | 40.2 us                                                               | 37.6 us: 1.07x faster                                 |
| unpickle_pure_python | 293 us                                                                | 275 us: 1.07x faster                                  |
| xml_etree_process    | 81.6 ms                                                               | 86.3 ms: 1.06x slower                                 |
| json_dumps           | 14.8 ms                                                               | 15.7 ms: 1.06x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, xml_etree_parse, unpickle, pickle, pickle_pure_python, tomli_loads, pickle_list, pickle_dict, unpickle_list

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml     | 68.0 ms                                                               | 71.8 ms: 1.06x slower                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (3): mako, django_template, genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|--------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| sympy_integrate          | 33.1 ms                                                               | 27.3 ms: 1.21x faster                                 |
| tornado_http             | 275 ms                                                                | 241 ms: 1.14x faster                                  |
| scimark_lu               | 167 ms                                                                | 152 ms: 1.10x faster                                  |
| async_tree_memoization   | 722 ms                                                                | 670 ms: 1.08x faster                                  |
| sqlite_synth             | 4.08 us                                                               | 3.80 us: 1.07x faster                                 |
| xml_etree_generate       | 129 ms                                                                | 121 ms: 1.07x faster                                  |
| json_loads               | 40.2 us                                                               | 37.6 us: 1.07x faster                                 |
| unpickle_pure_python     | 293 us                                                                | 275 us: 1.07x faster                                  |
| raytrace                 | 341 ms                                                                | 328 ms: 1.04x faster                                  |
| mdp                      | 3.86 sec                                                              | 3.71 sec: 1.04x faster                                |
| asyncio_websockets       | 762 ms                                                                | 734 ms: 1.04x faster                                  |
| async_generators         | 594 ms                                                                | 574 ms: 1.03x faster                                  |
| pycparser                | 1.62 sec                                                              | 1.67 sec: 1.03x slower                                |
| asyncio_tcp_ssl          | 2.75 sec                                                              | 2.83 sec: 1.03x slower                                |
| sqlglot_parse            | 1.74 ms                                                               | 1.81 ms: 1.04x slower                                 |
| generators               | 39.3 ms                                                               | 41.0 ms: 1.04x slower                                 |
| go                       | 187 ms                                                                | 196 ms: 1.05x slower                                  |
| html5lib                 | 89.2 ms                                                               | 93.8 ms: 1.05x slower                                 |
| richards                 | 60.3 ms                                                               | 63.5 ms: 1.05x slower                                 |
| genshi_xml               | 68.0 ms                                                               | 71.8 ms: 1.06x slower                                 |
| xml_etree_process        | 81.6 ms                                                               | 86.3 ms: 1.06x slower                                 |
| meteor_contest           | 142 ms                                                                | 150 ms: 1.06x slower                                  |
| json_dumps               | 14.8 ms                                                               | 15.7 ms: 1.06x slower                                 |
| coverage                 | 110 ms                                                                | 117 ms: 1.06x slower                                  |
| thrift                   | 1.12 ms                                                               | 1.19 ms: 1.07x slower                                 |
| deepcopy                 | 358 us                                                                | 383 us: 1.07x slower                                  |
| logging_format           | 8.86 us                                                               | 9.52 us: 1.07x slower                                 |
| create_gc_cycles         | 2.33 ms                                                               | 2.51 ms: 1.08x slower                                 |
| deepcopy_reduce          | 3.54 us                                                               | 3.83 us: 1.08x slower                                 |
| typing_runtime_protocols | 214 us                                                                | 233 us: 1.09x slower                                  |
| regex_effbot             | 4.87 ms                                                               | 5.30 ms: 1.09x slower                                 |
| regex_v8                 | 32.4 ms                                                               | 35.4 ms: 1.09x slower                                 |
| unpack_sequence          | 59.2 ns                                                               | 66.6 ns: 1.12x slower                                 |
| bench_thread_pool        | 2.89 ms                                                               | 3.58 ms: 1.24x slower                                 |
| Geometric mean           | (ref)                                                                 | 1.00x slower                                          |

Benchmark hidden because not significant (62): sympy_str, sqlglot_optimize, spectral_norm, scimark_sor, xml_etree_iterparse, xml_etree_parse, logging_simple, scimark_monte_carlo, sympy_expand, scimark_sparse_mat_mult, chaos, async_tree_memoization_tg, unpickle, sympy_sum, regex_dna, gc_traversal, pathlib, pyflate, pprint_pformat, sqlglot_normalize, python_startup_no_site, pickle, telco, async_tree_none_tg, pickle_pure_python, richards_super, json, nqueens, comprehensions, asyncio_tcp, deepcopy_memo, mako, docutils, 2to3, pprint_safe_repr, tomli_loads, nbody, pickle_list, async_tree_io, pylint, hexiom, django_template, logging_silent, pickle_dict, regex_compile, bpe_tokeniser, deltablue, genshi_text, async_tree_cpu_io_mixed_tg, async_tree_io_tg, python_startup, async_tree_none, coroutines, fannkuch, scimark_fft, pidigits, async_tree_cpu_io_mixed, sqlglot_transpile, crypto_pyaes, float, unpickle_list, bench_mp_pool

# HPT report

- Reliability score: 54.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x