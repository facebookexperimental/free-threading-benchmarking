# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 033510e
- commit date: 2024-09-06
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 415 ms: 1.06x faster                                  |
| docutils       | 3.94 sec                                                              | 3.82 sec: 1.03x faster                                |
| Geometric mean | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization    | 775 ms                                                                | 637 ms: 1.22x faster                                  |
| async_tree_memoization_tg | 692 ms                                                                | 621 ms: 1.11x faster                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 823 ms: 1.09x faster                                  |
| async_tree_none_tg        | 526 ms                                                                | 483 ms: 1.09x faster                                  |
| async_tree_io_tg          | 1.43 sec                                                              | 1.32 sec: 1.09x faster                                |
| asyncio_tcp               | 972 ms                                                                | 901 ms: 1.08x faster                                  |
| async_tree_none           | 523 ms                                                                | 501 ms: 1.04x faster                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 2.73 sec: 1.03x faster                                |
| asyncio_websockets        | 728 ms                                                                | 751 ms: 1.03x slower                                  |
| coroutines                | 29.3 ms                                                               | 32.0 ms: 1.09x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.05x faster                                          |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_generators, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 126 ms                                                                | 116 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 175 ms: 1.08x faster                                  |
| regex_v8       | 37.1 ms                                                               | 34.9 ms: 1.06x faster                                 |
| regex_effbot   | 4.63 ms                                                               | 5.19 ms: 1.12x slower                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark         | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|-------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list       | 7.48 us                                                               | 6.95 us: 1.08x faster                                 |
| unpickle          | 22.2 us                                                               | 20.8 us: 1.07x faster                                 |
| pickle_dict       | 46.5 us                                                               | 44.6 us: 1.04x faster                                 |
| tomli_loads       | 2.84 sec                                                              | 2.75 sec: 1.03x faster                                |
| xml_etree_process | 82.2 ms                                                               | 86.2 ms: 1.05x slower                                 |
| unpickle_list     | 6.78 us                                                               | 7.20 us: 1.06x slower                                 |
| xml_etree_parse   | 216 ms                                                                | 233 ms: 1.08x slower                                  |
| pickle            | 15.2 us                                                               | 16.5 us: 1.09x slower                                 |
| json_dumps        | 13.9 ms                                                               | 15.8 ms: 1.14x slower                                 |
| Geometric mean    | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (5): xml_etree_generate, json_loads, unpickle_pure_python, pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 21.6 ms: 1.09x faster                                 |
| python_startup_no_site | 16.0 ms                                                               | 15.1 ms: 1.06x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.07x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 31.6 ms                                                               | 33.6 ms: 1.06x slower                                 |
| mako           | 16.7 ms                                                               | 18.2 ms: 1.09x slower                                 |
| Geometric mean | (ref)                                                                 | 1.03x slower                                          |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                     | 229 ms                                                                | 11.3 ms: 20.19x faster                                |
| deepcopy                  | 498 us                                                                | 354 us: 1.41x faster                                  |
| async_tree_memoization    | 775 ms                                                                | 637 ms: 1.22x faster                                  |
| go                        | 193 ms                                                                | 161 ms: 1.20x faster                                  |
| deepcopy_reduce           | 4.31 us                                                               | 3.62 us: 1.19x faster                                 |
| deepcopy_memo             | 50.9 us                                                               | 43.0 us: 1.18x faster                                 |
| sqlglot_parse             | 1.92 ms                                                               | 1.69 ms: 1.13x faster                                 |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 6.07 ms: 1.13x faster                                 |
| coverage                  | 121 ms                                                                | 107 ms: 1.12x faster                                  |
| async_tree_memoization_tg | 692 ms                                                                | 621 ms: 1.11x faster                                  |
| pycparser                 | 1.71 sec                                                              | 1.54 sec: 1.11x faster                                |
| sympy_sum                 | 226 ms                                                                | 207 ms: 1.09x faster                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 823 ms: 1.09x faster                                  |
| async_tree_none_tg        | 526 ms                                                                | 483 ms: 1.09x faster                                  |
| python_startup            | 23.5 ms                                                               | 21.6 ms: 1.09x faster                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.32 sec: 1.09x faster                                |
| nbody                     | 126 ms                                                                | 116 ms: 1.08x faster                                  |
| pprint_safe_repr          | 991 ms                                                                | 916 ms: 1.08x faster                                  |
| regex_compile             | 189 ms                                                                | 175 ms: 1.08x faster                                  |
| asyncio_tcp               | 972 ms                                                                | 901 ms: 1.08x faster                                  |
| sqlglot_optimize          | 77.9 ms                                                               | 72.3 ms: 1.08x faster                                 |
| pickle_list               | 7.48 us                                                               | 6.95 us: 1.08x faster                                 |
| pprint_pformat            | 2.04 sec                                                              | 1.89 sec: 1.08x faster                                |
| sqlglot_normalize         | 150 ms                                                                | 140 ms: 1.07x faster                                  |
| pathlib                   | 31.8 ms                                                               | 29.7 ms: 1.07x faster                                 |
| unpickle                  | 22.2 us                                                               | 20.8 us: 1.07x faster                                 |
| bpe_tokeniser             | 6.53 sec                                                              | 6.12 sec: 1.07x faster                                |
| sympy_integrate           | 28.7 ms                                                               | 27.0 ms: 1.06x faster                                 |
| 2to3                      | 441 ms                                                                | 415 ms: 1.06x faster                                  |
| regex_v8                  | 37.1 ms                                                               | 34.9 ms: 1.06x faster                                 |
| python_startup_no_site    | 16.0 ms                                                               | 15.1 ms: 1.06x faster                                 |
| sympy_expand              | 638 ms                                                                | 603 ms: 1.06x faster                                  |
| richards                  | 68.8 ms                                                               | 65.0 ms: 1.06x faster                                 |
| unpack_sequence           | 54.6 ns                                                               | 51.6 ns: 1.06x faster                                 |
| create_gc_cycles          | 2.49 ms                                                               | 2.35 ms: 1.06x faster                                 |
| meteor_contest            | 156 ms                                                                | 148 ms: 1.06x faster                                  |
| sqlglot_transpile         | 2.24 ms                                                               | 2.13 ms: 1.05x faster                                 |
| pyflate                   | 710 ms                                                                | 676 ms: 1.05x faster                                  |
| sympy_str                 | 376 ms                                                                | 358 ms: 1.05x faster                                  |
| scimark_sor               | 176 ms                                                                | 169 ms: 1.04x faster                                  |
| hexiom                    | 8.42 ms                                                               | 8.08 ms: 1.04x faster                                 |
| pickle_dict               | 46.5 us                                                               | 44.6 us: 1.04x faster                                 |
| async_tree_none           | 523 ms                                                                | 501 ms: 1.04x faster                                  |
| spectral_norm             | 151 ms                                                                | 146 ms: 1.04x faster                                  |
| scimark_monte_carlo       | 89.0 ms                                                               | 85.8 ms: 1.04x faster                                 |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 2.73 sec: 1.03x faster                                |
| tomli_loads               | 2.84 sec                                                              | 2.75 sec: 1.03x faster                                |
| docutils                  | 3.94 sec                                                              | 3.82 sec: 1.03x faster                                |
| asyncio_websockets        | 728 ms                                                                | 751 ms: 1.03x slower                                  |
| xml_etree_process         | 82.2 ms                                                               | 86.2 ms: 1.05x slower                                 |
| nqueens                   | 108 ms                                                                | 114 ms: 1.05x slower                                  |
| unpickle_list             | 6.78 us                                                               | 7.20 us: 1.06x slower                                 |
| genshi_text               | 31.6 ms                                                               | 33.6 ms: 1.06x slower                                 |
| generators                | 40.7 ms                                                               | 43.6 ms: 1.07x slower                                 |
| xml_etree_parse           | 216 ms                                                                | 233 ms: 1.08x slower                                  |
| pickle                    | 15.2 us                                                               | 16.5 us: 1.09x slower                                 |
| coroutines                | 29.3 ms                                                               | 32.0 ms: 1.09x slower                                 |
| mako                      | 16.7 ms                                                               | 18.2 ms: 1.09x slower                                 |
| regex_effbot              | 4.63 ms                                                               | 5.19 ms: 1.12x slower                                 |
| json_dumps                | 13.9 ms                                                               | 15.8 ms: 1.14x slower                                 |
| dulwich_log               | 97.5 ms                                                               | 123 ms: 1.26x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.06x faster                                          |

Benchmark hidden because not significant (36): html5lib, thrift, logging_silent, genshi_xml, gc_traversal, crypto_pyaes, raytrace, async_tree_cpu_io_mixed_tg, richards_super, comprehensions, tornado_http, async_generators, sqlite_synth, async_tree_io, xml_etree_generate, django_template, scimark_fft, mdp, float, pidigits, json_loads, deltablue, typing_runtime_protocols, fannkuch, unpickle_pure_python, json, regex_dna, pickle_pure_python, chaos, logging_simple, xml_etree_iterparse, pylint, scimark_lu, bench_mp_pool, logging_format, bench_thread_pool
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x