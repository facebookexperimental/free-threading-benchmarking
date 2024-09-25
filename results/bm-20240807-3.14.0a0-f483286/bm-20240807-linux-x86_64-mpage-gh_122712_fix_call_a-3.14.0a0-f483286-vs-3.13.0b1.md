# Results vs. 3.13.0b1

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_memoization     | 775 ms                                                                | 643 ms: 1.21x faster                                                 |
| async_tree_none_tg         | 526 ms                                                                | 456 ms: 1.15x faster                                                 |
| async_tree_memoization_tg  | 692 ms                                                                | 609 ms: 1.13x faster                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.29 sec: 1.11x faster                                               |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 819 ms: 1.10x faster                                                 |
| async_tree_io              | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                               |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 826 ms: 1.06x faster                                                 |
| asyncio_tcp                | 972 ms                                                                | 925 ms: 1.05x faster                                                 |
| asyncio_websockets         | 728 ms                                                                | 758 ms: 1.04x slower                                                 |
| coroutines                 | 29.3 ms                                                               | 31.1 ms: 1.06x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.06x faster                                                         |

Benchmark hidden because not significant (3): async_tree_none, asyncio_tcp_ssl, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 126 ms                                                                | 111 ms: 1.13x faster                                                 |
| pidigits       | 256 ms                                                                | 245 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.05x faster                                                         |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 34.2 ms: 1.08x faster                                                |
| regex_compile  | 189 ms                                                                | 178 ms: 1.06x faster                                                 |
| regex_effbot   | 4.63 ms                                                               | 4.96 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark         | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle          | 22.2 us                                                               | 20.4 us: 1.09x faster                                                |
| xml_etree_process | 82.2 ms                                                               | 76.7 ms: 1.07x faster                                                |
| pickle_list       | 7.48 us                                                               | 6.99 us: 1.07x faster                                                |
| tomli_loads       | 2.84 sec                                                              | 2.74 sec: 1.04x faster                                               |
| json_loads        | 37.9 us                                                               | 36.7 us: 1.03x faster                                                |
| unpickle_list     | 6.78 us                                                               | 7.43 us: 1.10x slower                                                |
| json_dumps        | 13.9 ms                                                               | 15.7 ms: 1.13x slower                                                |
| Geometric mean    | (ref)                                                                 | 1.01x faster                                                         |

Benchmark hidden because not significant (7): pickle_dict, pickle_pure_python, unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 21.6 ms: 1.09x faster                                                |
| python_startup_no_site | 16.0 ms                                                               | 14.9 ms: 1.07x faster                                                |
| Geometric mean         | (ref)                                                                 | 1.08x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml     | 71.9 ms                                                               | 68.1 ms: 1.06x faster                                                |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                         |

Benchmark hidden because not significant (3): mako, django_template, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 10.8 ms: 21.30x faster                                               |
| deepcopy                   | 498 us                                                                | 346 us: 1.44x faster                                                 |
| deepcopy_memo              | 50.9 us                                                               | 40.8 us: 1.25x faster                                                |
| deepcopy_reduce            | 4.31 us                                                               | 3.50 us: 1.23x faster                                                |
| async_tree_memoization     | 775 ms                                                                | 643 ms: 1.21x faster                                                 |
| create_gc_cycles           | 2.49 ms                                                               | 2.14 ms: 1.16x faster                                                |
| async_tree_none_tg         | 526 ms                                                                | 456 ms: 1.15x faster                                                 |
| richards                   | 68.8 ms                                                               | 60.2 ms: 1.14x faster                                                |
| async_tree_memoization_tg  | 692 ms                                                                | 609 ms: 1.13x faster                                                 |
| nbody                      | 126 ms                                                                | 111 ms: 1.13x faster                                                 |
| meteor_contest             | 156 ms                                                                | 140 ms: 1.11x faster                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.29 sec: 1.11x faster                                               |
| sqlglot_parse              | 1.92 ms                                                               | 1.73 ms: 1.11x faster                                                |
| sqlglot_optimize           | 77.9 ms                                                               | 70.4 ms: 1.11x faster                                                |
| mdp                        | 4.01 sec                                                              | 3.62 sec: 1.11x faster                                               |
| pathlib                    | 31.8 ms                                                               | 28.8 ms: 1.10x faster                                                |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 819 ms: 1.10x faster                                                 |
| logging_simple             | 9.16 us                                                               | 8.40 us: 1.09x faster                                                |
| unpickle                   | 22.2 us                                                               | 20.4 us: 1.09x faster                                                |
| coverage                   | 121 ms                                                                | 111 ms: 1.09x faster                                                 |
| python_startup             | 23.5 ms                                                               | 21.6 ms: 1.09x faster                                                |
| regex_v8                   | 37.1 ms                                                               | 34.2 ms: 1.08x faster                                                |
| scimark_sor                | 176 ms                                                                | 163 ms: 1.08x faster                                                 |
| pycparser                  | 1.71 sec                                                              | 1.58 sec: 1.08x faster                                               |
| python_startup_no_site     | 16.0 ms                                                               | 14.9 ms: 1.07x faster                                                |
| xml_etree_process          | 82.2 ms                                                               | 76.7 ms: 1.07x faster                                                |
| pickle_list                | 7.48 us                                                               | 6.99 us: 1.07x faster                                                |
| async_tree_io              | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                               |
| logging_silent             | 137 ns                                                                | 128 ns: 1.07x faster                                                 |
| regex_compile              | 189 ms                                                                | 178 ms: 1.06x faster                                                 |
| gc_traversal               | 5.80 ms                                                               | 5.46 ms: 1.06x faster                                                |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 826 ms: 1.06x faster                                                 |
| raytrace                   | 351 ms                                                                | 331 ms: 1.06x faster                                                 |
| pyflate                    | 710 ms                                                                | 671 ms: 1.06x faster                                                 |
| scimark_lu                 | 150 ms                                                                | 142 ms: 1.06x faster                                                 |
| genshi_xml                 | 71.9 ms                                                               | 68.1 ms: 1.06x faster                                                |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 6.49 ms: 1.05x faster                                                |
| pprint_pformat             | 2.04 sec                                                              | 1.93 sec: 1.05x faster                                               |
| asyncio_tcp                | 972 ms                                                                | 925 ms: 1.05x faster                                                 |
| comprehensions             | 22.6 us                                                               | 21.7 us: 1.05x faster                                                |
| pidigits                   | 256 ms                                                                | 245 ms: 1.04x faster                                                 |
| sqlglot_normalize          | 150 ms                                                                | 144 ms: 1.04x faster                                                 |
| bpe_tokeniser              | 6.53 sec                                                              | 6.28 sec: 1.04x faster                                               |
| tomli_loads                | 2.84 sec                                                              | 2.74 sec: 1.04x faster                                               |
| json_loads                 | 37.9 us                                                               | 36.7 us: 1.03x faster                                                |
| asyncio_websockets         | 728 ms                                                                | 758 ms: 1.04x slower                                                 |
| sympy_integrate            | 28.7 ms                                                               | 30.1 ms: 1.05x slower                                                |
| coroutines                 | 29.3 ms                                                               | 31.1 ms: 1.06x slower                                                |
| regex_effbot               | 4.63 ms                                                               | 4.96 ms: 1.07x slower                                                |
| unpickle_list              | 6.78 us                                                               | 7.43 us: 1.10x slower                                                |
| bench_thread_pool          | 3.01 ms                                                               | 3.31 ms: 1.10x slower                                                |
| json_dumps                 | 13.9 ms                                                               | 15.7 ms: 1.13x slower                                                |
| bench_mp_pool              | 19.7 ms                                                               | 22.7 ms: 1.15x slower                                                |
| unpack_sequence            | 54.6 ns                                                               | 76.4 ns: 1.40x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.07x faster                                                         |

Benchmark hidden because not significant (42): sqlite_synth, mako, sympy_expand, pickle_dict, sympy_str, pprint_safe_repr, sympy_sum, richards_super, django_template, async_tree_none, typing_runtime_protocols, pickle_pure_python, generators, fannkuch, unpickle_pure_python, asyncio_tcp_ssl, html5lib, sqlglot_transpile, 2to3, hexiom, regex_dna, nqueens, xml_etree_generate, async_generators, docutils, deltablue, scimark_monte_carlo, pylint, spectral_norm, go, xml_etree_iterparse, logging_format, pickle, float, genshi_text, chaos, scimark_fft, xml_etree_parse, json, thrift, tornado_http, crypto_pyaes
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x