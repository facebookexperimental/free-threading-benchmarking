# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5592399
- commit date: 2024-07-24
- overall geometric mean: 1.01x slower
- HPT reliability: 99.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240724-linux-x86_64-python-9ac606080a0074cdf758-3.14.0a0-9ac6060 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| docutils       | 4.83 sec                                                              | 4.97 sec: 1.03x slower                                |
| Geometric mean | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240724-linux-x86_64-python-9ac606080a0074cdf758-3.14.0a0-9ac6060 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|--------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none_tg | 480 ms                                                                | 514 ms: 1.07x slower                                  |
| Geometric mean     | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240724-linux-x86_64-python-9ac606080a0074cdf758-3.14.0a0-9ac6060 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 296 ms                                                                | 278 ms: 1.06x faster                                  |
| pidigits       | 251 ms                                                                | 241 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240724-linux-x86_64-python-9ac606080a0074cdf758-3.14.0a0-9ac6060 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 289 ms                                                                | 307 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                                 | 1.03x slower                                          |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240724-linux-x86_64-python-9ac606080a0074cdf758-3.14.0a0-9ac6060 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| tomli_loads         | 4.23 sec                                                              | 4.32 sec: 1.02x slower                                |
| pickle_pure_python  | 767 us                                                                | 801 us: 1.04x slower                                  |
| unpickle_list       | 7.57 us                                                               | 7.97 us: 1.05x slower                                 |
| json_dumps          | 17.8 ms                                                               | 19.0 ms: 1.06x slower                                 |
| xml_etree_generate  | 152 ms                                                                | 164 ms: 1.08x slower                                  |
| xml_etree_iterparse | 156 ms                                                                | 169 ms: 1.08x slower                                  |
| Geometric mean      | (ref)                                                                 | 1.03x slower                                          |

Benchmark hidden because not significant (8): xml_etree_parse, pickle, unpickle_pure_python, xml_etree_process, unpickle, pickle_dict, pickle_list, json_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_text, mako, django_template, genshi_xml

All benchmarks:
===============

| Benchmark           | bm-20240724-linux-x86_64-python-9ac606080a0074cdf758-3.14.0a0-9ac6060 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy            | 616 us                                                                | 556 us: 1.11x faster                                  |
| coverage            | 158 ms                                                                | 148 ms: 1.07x faster                                  |
| nbody               | 296 ms                                                                | 278 ms: 1.06x faster                                  |
| scimark_fft         | 654 ms                                                                | 616 ms: 1.06x faster                                  |
| sympy_integrate     | 46.6 ms                                                               | 44.1 ms: 1.06x faster                                 |
| unpack_sequence     | 204 ns                                                                | 194 ns: 1.05x faster                                  |
| pidigits            | 251 ms                                                                | 241 ms: 1.04x faster                                  |
| scimark_lu          | 328 ms                                                                | 315 ms: 1.04x faster                                  |
| tomli_loads         | 4.23 sec                                                              | 4.32 sec: 1.02x slower                                |
| docutils            | 4.83 sec                                                              | 4.97 sec: 1.03x slower                                |
| raytrace            | 779 ms                                                                | 803 ms: 1.03x slower                                  |
| asyncio_websockets  | 744 ms                                                                | 768 ms: 1.03x slower                                  |
| pprint_safe_repr    | 1.70 sec                                                              | 1.75 sec: 1.03x slower                                |
| logging_silent      | 256 ns                                                                | 266 ns: 1.04x slower                                  |
| pickle_pure_python  | 767 us                                                                | 801 us: 1.04x slower                                  |
| create_gc_cycles    | 1.84 ms                                                               | 1.93 ms: 1.04x slower                                 |
| sqlglot_optimize    | 117 ms                                                                | 123 ms: 1.05x slower                                  |
| unpickle_list       | 7.57 us                                                               | 7.97 us: 1.05x slower                                 |
| richards_super      | 120 ms                                                                | 127 ms: 1.06x slower                                  |
| pathlib             | 32.3 ms                                                               | 34.2 ms: 1.06x slower                                 |
| chaos               | 166 ms                                                                | 176 ms: 1.06x slower                                  |
| regex_compile       | 289 ms                                                                | 307 ms: 1.06x slower                                  |
| json_dumps          | 17.8 ms                                                               | 19.0 ms: 1.06x slower                                 |
| pyflate             | 1.05 sec                                                              | 1.12 sec: 1.07x slower                                |
| deepcopy_reduce     | 5.99 us                                                               | 6.40 us: 1.07x slower                                 |
| sqlglot_parse       | 3.76 ms                                                               | 4.03 ms: 1.07x slower                                 |
| async_tree_none_tg  | 480 ms                                                                | 514 ms: 1.07x slower                                  |
| xml_etree_generate  | 152 ms                                                                | 164 ms: 1.08x slower                                  |
| xml_etree_iterparse | 156 ms                                                                | 169 ms: 1.08x slower                                  |
| gc_traversal        | 4.07 ms                                                               | 4.51 ms: 1.11x slower                                 |
| bench_thread_pool   | 3.74 ms                                                               | 4.26 ms: 1.14x slower                                 |
| Geometric mean      | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (66): crypto_pyaes, dulwich_log, meteor_contest, genshi_text, scimark_monte_carlo, sympy_str, pprint_pformat, mdp, telco, xml_etree_parse, deepcopy_memo, tornado_http, async_tree_io_tg, fannkuch, scimark_sor, html5lib, asyncio_tcp, pickle, sqlglot_normalize, deltablue, pycparser, spectral_norm, async_tree_none, mako, async_tree_io, async_generators, unpickle_pure_python, logging_format, django_template, sympy_expand, comprehensions, richards, python_startup_no_site, nqueens, asyncio_tcp_ssl, xml_etree_process, logging_simple, bpe_tokeniser, python_startup, float, regex_effbot, unpickle, coroutines, generators, sqlglot_transpile, pickle_dict, hexiom, go, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, regex_dna, 2to3, async_tree_memoization, json, sqlite_synth, async_tree_memoization_tg, pickle_list, sympy_sum, pylint, scimark_sparse_mat_mult, thrift, regex_v8, json_loads, typing_runtime_protocols, genshi_xml, bench_mp_pool

# HPT report

- Reliability score: 99.70% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x