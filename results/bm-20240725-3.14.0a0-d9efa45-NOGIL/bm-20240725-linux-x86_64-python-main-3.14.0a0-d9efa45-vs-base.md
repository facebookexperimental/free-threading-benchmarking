# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d9efa45
- commit date: 2024-07-25
- overall geometric mean: 1.01x slower
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| tornado_http   | 314 ms                                                                | 358 ms: 1.14x slower                                  |
| Geometric mean | (ref)                                                                 | 1.03x slower                                          |

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.16 sec                                                              | 1.19 sec: 1.03x slower                                |
| async_tree_memoization_tg | 621 ms                                                                | 641 ms: 1.03x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.47 ms                                                               | 4.78 ms: 1.07x slower                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (3): regex_dna, regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_list       | 7.64 us                                                               | 6.83 us: 1.12x faster                                 |
| pickle_pure_python  | 814 us                                                                | 768 us: 1.06x faster                                  |
| pickle_list         | 6.22 us                                                               | 6.46 us: 1.04x slower                                 |
| xml_etree_process   | 129 ms                                                                | 137 ms: 1.06x slower                                  |
| xml_etree_parse     | 199 ms                                                                | 213 ms: 1.07x slower                                  |
| xml_etree_iterparse | 159 ms                                                                | 177 ms: 1.11x slower                                  |
| Geometric mean      | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (8): xml_etree_generate, json_dumps, tomli_loads, json_loads, pickle, unpickle, unpickle_pure_python, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 28.3 ms                                                               | 29.3 ms: 1.03x slower                                 |
| python_startup_no_site | 18.6 ms                                                               | 19.9 ms: 1.07x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.05x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| mako           | 31.5 ms                                                               | 29.5 ms: 1.07x faster                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (3): genshi_xml, genshi_text, django_template

All benchmarks:
===============

| Benchmark                 | bm-20240725-linux-x86_64-python-1d607fe759ef22177b50-3.14.0a0-1d607fe | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| bench_thread_pool         | 4.80 ms                                                               | 3.97 ms: 1.21x faster                                 |
| unpickle_list             | 7.64 us                                                               | 6.83 us: 1.12x faster                                 |
| mako                      | 31.5 ms                                                               | 29.5 ms: 1.07x faster                                 |
| pickle_pure_python        | 814 us                                                                | 768 us: 1.06x faster                                  |
| deepcopy_memo             | 71.9 us                                                               | 67.8 us: 1.06x faster                                 |
| create_gc_cycles          | 1.97 ms                                                               | 1.87 ms: 1.06x faster                                 |
| bpe_tokeniser             | 10.4 sec                                                              | 9.93 sec: 1.05x faster                                |
| crypto_pyaes              | 156 ms                                                                | 149 ms: 1.05x faster                                  |
| asyncio_tcp               | 1.15 sec                                                              | 1.10 sec: 1.04x faster                                |
| logging_silent            | 269 ns                                                                | 259 ns: 1.04x faster                                  |
| pyflate                   | 1.13 sec                                                              | 1.09 sec: 1.03x faster                                |
| raytrace                  | 781 ms                                                                | 805 ms: 1.03x slower                                  |
| async_tree_io_tg          | 1.16 sec                                                              | 1.19 sec: 1.03x slower                                |
| async_tree_memoization_tg | 621 ms                                                                | 641 ms: 1.03x slower                                  |
| python_startup            | 28.3 ms                                                               | 29.3 ms: 1.03x slower                                 |
| pickle_list               | 6.22 us                                                               | 6.46 us: 1.04x slower                                 |
| sympy_sum                 | 462 ms                                                                | 487 ms: 1.05x slower                                  |
| xml_etree_process         | 129 ms                                                                | 137 ms: 1.06x slower                                  |
| python_startup_no_site    | 18.6 ms                                                               | 19.9 ms: 1.07x slower                                 |
| regex_effbot              | 4.47 ms                                                               | 4.78 ms: 1.07x slower                                 |
| xml_etree_parse           | 199 ms                                                                | 213 ms: 1.07x slower                                  |
| unpack_sequence           | 176 ns                                                                | 190 ns: 1.08x slower                                  |
| sympy_str                 | 657 ms                                                                | 713 ms: 1.09x slower                                  |
| deltablue                 | 11.1 ms                                                               | 12.1 ms: 1.09x slower                                 |
| typing_runtime_protocols  | 341 us                                                                | 377 us: 1.11x slower                                  |
| xml_etree_iterparse       | 159 ms                                                                | 177 ms: 1.11x slower                                  |
| bench_mp_pool             | 14.1 ms                                                               | 15.8 ms: 1.12x slower                                 |
| tornado_http              | 314 ms                                                                | 358 ms: 1.14x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (68): float, richards, html5lib, sqlglot_normalize, async_tree_none_tg, go, comprehensions, sympy_integrate, genshi_xml, coverage, nqueens, mdp, sqlglot_optimize, xml_etree_generate, nbody, logging_format, asyncio_websockets, scimark_fft, regex_dna, logging_simple, spectral_norm, deepcopy, sympy_expand, pidigits, async_tree_none, docutils, gc_traversal, scimark_sor, json_dumps, sqlite_synth, fannkuch, 2to3, regex_compile, meteor_contest, chaos, async_tree_cpu_io_mixed, coroutines, tomli_loads, pprint_pformat, pycparser, asyncio_tcp_ssl, pprint_safe_repr, pathlib, thrift, async_generators, sqlglot_parse, telco, json_loads, async_tree_io, richards_super, regex_v8, hexiom, deepcopy_reduce, async_tree_memoization, sqlglot_transpile, pickle, scimark_lu, scimark_sparse_mat_mult, async_tree_cpu_io_mixed_tg, json, genshi_text, pylint, scimark_monte_carlo, unpickle, generators, unpickle_pure_python, django_template, pickle_dict

# HPT report

- Reliability score: 99.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x