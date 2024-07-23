# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4606eff
- commit date: 2024-07-23
- overall geometric mean: 1.01x faster
- HPT reliability: 98.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| html5lib       | 139 ms                                                                | 157 ms: 1.13x slower                                  |
| tornado_http   | 349 ms                                                                | 320 ms: 1.09x faster                                  |
| Geometric mean | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io              | 1.30 sec                                                              | 1.22 sec: 1.06x faster                                |
| async_tree_cpu_io_mixed_tg | 817 ms                                                                | 859 ms: 1.05x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none, async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 36.3 ms                                                               | 33.7 ms: 1.08x faster                                 |
| regex_effbot   | 4.57 ms                                                               | 4.80 ms: 1.05x slower                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_list        | 8.14 us                                                               | 7.21 us: 1.13x faster                                 |
| unpickle_pure_python | 609 us                                                                | 540 us: 1.13x faster                                  |
| xml_etree_parse      | 231 ms                                                                | 213 ms: 1.08x faster                                  |
| pickle_pure_python   | 805 us                                                                | 760 us: 1.06x faster                                  |
| unpickle             | 22.3 us                                                               | 21.2 us: 1.05x faster                                 |
| tomli_loads          | 4.22 sec                                                              | 4.14 sec: 1.02x faster                                |
| json_loads           | 42.7 us                                                               | 45.2 us: 1.06x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (7): xml_etree_iterparse, xml_etree_generate, xml_etree_process, pickle, json_dumps, pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| mako            | 30.4 ms                                                               | 31.9 ms: 1.05x slower                                 |
| django_template | 80.4 ms                                                               | 84.5 ms: 1.05x slower                                 |
| genshi_xml      | 116 ms                                                                | 122 ms: 1.05x slower                                  |
| Geometric mean  | (ref)                                                                 | 1.04x slower                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_list              | 8.14 us                                                               | 7.21 us: 1.13x faster                                 |
| unpickle_pure_python       | 609 us                                                                | 540 us: 1.13x faster                                  |
| tornado_http               | 349 ms                                                                | 320 ms: 1.09x faster                                  |
| xml_etree_parse            | 231 ms                                                                | 213 ms: 1.08x faster                                  |
| regex_v8                   | 36.3 ms                                                               | 33.7 ms: 1.08x faster                                 |
| sqlglot_transpile          | 4.92 ms                                                               | 4.58 ms: 1.07x faster                                 |
| pathlib                    | 34.8 ms                                                               | 32.6 ms: 1.07x faster                                 |
| create_gc_cycles           | 1.94 ms                                                               | 1.82 ms: 1.06x faster                                 |
| async_tree_io              | 1.30 sec                                                              | 1.22 sec: 1.06x faster                                |
| scimark_lu                 | 332 ms                                                                | 314 ms: 1.06x faster                                  |
| pickle_pure_python         | 805 us                                                                | 760 us: 1.06x faster                                  |
| generators                 | 58.0 ms                                                               | 54.9 ms: 1.06x faster                                 |
| unpickle                   | 22.3 us                                                               | 21.2 us: 1.05x faster                                 |
| pycparser                  | 2.28 sec                                                              | 2.16 sec: 1.05x faster                                |
| scimark_monte_carlo        | 171 ms                                                                | 163 ms: 1.05x faster                                  |
| deepcopy_memo              | 72.8 us                                                               | 69.7 us: 1.05x faster                                 |
| logging_format             | 17.3 us                                                               | 16.6 us: 1.04x faster                                 |
| fannkuch                   | 808 ms                                                                | 783 ms: 1.03x faster                                  |
| asyncio_tcp_ssl            | 3.36 sec                                                              | 3.27 sec: 1.03x faster                                |
| bpe_tokeniser              | 10.3 sec                                                              | 10.1 sec: 1.02x faster                                |
| tomli_loads                | 4.22 sec                                                              | 4.14 sec: 1.02x faster                                |
| mako                       | 30.4 ms                                                               | 31.9 ms: 1.05x slower                                 |
| django_template            | 80.4 ms                                                               | 84.5 ms: 1.05x slower                                 |
| regex_effbot               | 4.57 ms                                                               | 4.80 ms: 1.05x slower                                 |
| async_tree_cpu_io_mixed_tg | 817 ms                                                                | 859 ms: 1.05x slower                                  |
| genshi_xml                 | 116 ms                                                                | 122 ms: 1.05x slower                                  |
| coroutines                 | 43.2 ms                                                               | 45.6 ms: 1.06x slower                                 |
| json_loads                 | 42.7 us                                                               | 45.2 us: 1.06x slower                                 |
| json                       | 7.98 ms                                                               | 8.61 ms: 1.08x slower                                 |
| html5lib                   | 139 ms                                                                | 157 ms: 1.13x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (67): dulwich_log, unpack_sequence, pylint, nqueens, gc_traversal, sqlglot_normalize, xml_etree_iterparse, xml_etree_generate, richards, sqlglot_optimize, sqlite_synth, deepcopy_reduce, async_tree_memoization_tg, scimark_fft, go, richards_super, xml_etree_process, comprehensions, scimark_sparse_mat_mult, deltablue, logging_silent, deepcopy, async_generators, nbody, pickle, pprint_pformat, bench_mp_pool, float, mdp, python_startup, json_dumps, asyncio_websockets, docutils, sympy_sum, scimark_sor, logging_simple, regex_compile, async_tree_cpu_io_mixed, chaos, bench_thread_pool, pidigits, async_tree_io_tg, pyflate, pprint_safe_repr, spectral_norm, raytrace, thrift, typing_runtime_protocols, sqlglot_parse, asyncio_tcp, async_tree_none, pickle_dict, telco, meteor_contest, coverage, sympy_expand, genshi_text, python_startup_no_site, sympy_integrate, async_tree_none_tg, async_tree_memoization, crypto_pyaes, 2to3, regex_dna, pickle_list, sympy_str, hexiom

# HPT report

- Reliability score: 98.18% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x