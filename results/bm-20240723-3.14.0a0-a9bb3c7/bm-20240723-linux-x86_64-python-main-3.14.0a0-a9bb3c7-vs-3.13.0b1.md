# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 410 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 692 ms                                                                | 584 ms: 1.18x faster                                  |
| async_tree_memoization     | 775 ms                                                                | 671 ms: 1.16x faster                                  |
| async_tree_io_tg           | 1.43 sec                                                              | 1.24 sec: 1.15x faster                                |
| async_tree_none_tg         | 526 ms                                                                | 464 ms: 1.13x faster                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 821 ms: 1.09x faster                                  |
| async_tree_io              | 1.39 sec                                                              | 1.28 sec: 1.08x faster                                |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 818 ms: 1.07x faster                                  |
| asyncio_websockets         | 728 ms                                                                | 755 ms: 1.04x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.06x faster                                          |

Benchmark hidden because not significant (5): async_generators, asyncio_tcp, asyncio_tcp_ssl, async_tree_none, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 126 ms                                                                | 114 ms: 1.10x faster                                  |
| pidigits       | 256 ms                                                                | 240 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                                 | 1.05x faster                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 32.9 ms: 1.13x faster                                 |
| regex_effbot   | 4.63 ms                                                               | 4.86 ms: 1.05x slower                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|--------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list        | 7.48 us                                                               | 6.29 us: 1.19x faster                                 |
| unpickle           | 22.2 us                                                               | 20.1 us: 1.11x faster                                 |
| tomli_loads        | 2.84 sec                                                              | 2.68 sec: 1.06x faster                                |
| xml_etree_generate | 120 ms                                                                | 116 ms: 1.03x faster                                  |
| pickle             | 15.2 us                                                               | 15.8 us: 1.04x slower                                 |
| json_dumps         | 13.9 ms                                                               | 14.8 ms: 1.06x slower                                 |
| Geometric mean     | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (8): pickle_dict, pickle_pure_python, xml_etree_iterparse, xml_etree_parse, unpickle_list, json_loads, xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 21.4 ms: 1.10x faster                                 |
| python_startup_no_site | 16.0 ms                                                               | 14.8 ms: 1.08x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.09x faster                                          |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_xml, django_template, genshi_text, mako

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                      | 229 ms                                                                | 11.1 ms: 20.56x faster                                |
| deepcopy                   | 498 us                                                                | 361 us: 1.38x faster                                  |
| deepcopy_memo              | 50.9 us                                                               | 38.7 us: 1.32x faster                                 |
| pickle_list                | 7.48 us                                                               | 6.29 us: 1.19x faster                                 |
| async_tree_memoization_tg  | 692 ms                                                                | 584 ms: 1.18x faster                                  |
| deepcopy_reduce            | 4.31 us                                                               | 3.71 us: 1.16x faster                                 |
| async_tree_memoization     | 775 ms                                                                | 671 ms: 1.16x faster                                  |
| async_tree_io_tg           | 1.43 sec                                                              | 1.24 sec: 1.15x faster                                |
| richards                   | 68.8 ms                                                               | 60.4 ms: 1.14x faster                                 |
| async_tree_none_tg         | 526 ms                                                                | 464 ms: 1.13x faster                                  |
| regex_v8                   | 37.1 ms                                                               | 32.9 ms: 1.13x faster                                 |
| sqlglot_parse              | 1.92 ms                                                               | 1.72 ms: 1.11x faster                                 |
| pathlib                    | 31.8 ms                                                               | 28.6 ms: 1.11x faster                                 |
| mdp                        | 4.01 sec                                                              | 3.61 sec: 1.11x faster                                |
| unpickle                   | 22.2 us                                                               | 20.1 us: 1.11x faster                                 |
| logging_simple             | 9.16 us                                                               | 8.31 us: 1.10x faster                                 |
| nbody                      | 126 ms                                                                | 114 ms: 1.10x faster                                  |
| python_startup             | 23.5 ms                                                               | 21.4 ms: 1.10x faster                                 |
| create_gc_cycles           | 2.49 ms                                                               | 2.27 ms: 1.10x faster                                 |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 821 ms: 1.09x faster                                  |
| pycparser                  | 1.71 sec                                                              | 1.57 sec: 1.09x faster                                |
| async_tree_io              | 1.39 sec                                                              | 1.28 sec: 1.08x faster                                |
| logging_silent             | 137 ns                                                                | 126 ns: 1.08x faster                                  |
| python_startup_no_site     | 16.0 ms                                                               | 14.8 ms: 1.08x faster                                 |
| 2to3                       | 441 ms                                                                | 410 ms: 1.08x faster                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 818 ms: 1.07x faster                                  |
| richards_super             | 73.5 ms                                                               | 68.7 ms: 1.07x faster                                 |
| meteor_contest             | 156 ms                                                                | 146 ms: 1.07x faster                                  |
| pidigits                   | 256 ms                                                                | 240 ms: 1.07x faster                                  |
| comprehensions             | 22.6 us                                                               | 21.3 us: 1.07x faster                                 |
| sqlglot_optimize           | 77.9 ms                                                               | 73.2 ms: 1.06x faster                                 |
| generators                 | 40.7 ms                                                               | 38.3 ms: 1.06x faster                                 |
| pyflate                    | 710 ms                                                                | 669 ms: 1.06x faster                                  |
| sqlite_synth               | 3.94 us                                                               | 3.71 us: 1.06x faster                                 |
| tomli_loads                | 2.84 sec                                                              | 2.68 sec: 1.06x faster                                |
| sympy_sum                  | 226 ms                                                                | 214 ms: 1.06x faster                                  |
| bpe_tokeniser              | 6.53 sec                                                              | 6.17 sec: 1.06x faster                                |
| typing_runtime_protocols   | 222 us                                                                | 210 us: 1.06x faster                                  |
| thrift                     | 1.09 ms                                                               | 1.03 ms: 1.06x faster                                 |
| pprint_pformat             | 2.04 sec                                                              | 1.92 sec: 1.06x faster                                |
| sympy_expand               | 638 ms                                                                | 605 ms: 1.05x faster                                  |
| deltablue                  | 4.55 ms                                                               | 4.31 ms: 1.05x faster                                 |
| sqlglot_transpile          | 2.24 ms                                                               | 2.13 ms: 1.05x faster                                 |
| sympy_str                  | 376 ms                                                                | 360 ms: 1.05x faster                                  |
| pprint_safe_repr           | 991 ms                                                                | 952 ms: 1.04x faster                                  |
| xml_etree_generate         | 120 ms                                                                | 116 ms: 1.03x faster                                  |
| asyncio_websockets         | 728 ms                                                                | 755 ms: 1.04x slower                                  |
| pickle                     | 15.2 us                                                               | 15.8 us: 1.04x slower                                 |
| coverage                   | 121 ms                                                                | 126 ms: 1.05x slower                                  |
| regex_effbot               | 4.63 ms                                                               | 4.86 ms: 1.05x slower                                 |
| json_dumps                 | 13.9 ms                                                               | 14.8 ms: 1.06x slower                                 |
| spectral_norm              | 151 ms                                                                | 164 ms: 1.08x slower                                  |
| bench_thread_pool          | 3.01 ms                                                               | 3.42 ms: 1.13x slower                                 |
| json                       | 6.79 ms                                                               | 7.74 ms: 1.14x slower                                 |
| unpack_sequence            | 54.6 ns                                                               | 78.4 ns: 1.44x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.07x faster                                          |

Benchmark hidden because not significant (43): regex_compile, html5lib, raytrace, genshi_xml, async_generators, scimark_sparse_mat_mult, gc_traversal, pickle_dict, tornado_http, pickle_pure_python, scimark_sor, asyncio_tcp, dulwich_log, django_template, hexiom, go, genshi_text, xml_etree_iterparse, nqueens, mako, scimark_monte_carlo, sqlglot_normalize, docutils, xml_etree_parse, crypto_pyaes, logging_format, chaos, unpickle_list, json_loads, float, asyncio_tcp_ssl, fannkuch, regex_dna, dask, async_tree_none, sympy_integrate, scimark_fft, xml_etree_process, pylint, coroutines, bench_mp_pool, scimark_lu, unpickle_pure_python
Ignored benchmarks (4) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x