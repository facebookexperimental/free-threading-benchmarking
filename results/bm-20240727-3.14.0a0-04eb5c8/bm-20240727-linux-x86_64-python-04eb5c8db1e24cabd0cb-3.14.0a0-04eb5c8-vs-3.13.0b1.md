# Results vs. 3.13.0b1

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tornado_http   | 253 ms                                                                | 228 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                          |

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 775 ms                                                                | 626 ms: 1.24x faster                                                  |
| async_tree_memoization_tg  | 692 ms                                                                | 591 ms: 1.17x faster                                                  |
| async_tree_io_tg           | 1.43 sec                                                              | 1.22 sec: 1.17x faster                                                |
| async_tree_none_tg         | 526 ms                                                                | 451 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 794 ms: 1.13x faster                                                  |
| async_tree_io              | 1.39 sec                                                              | 1.26 sec: 1.10x faster                                                |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 806 ms: 1.09x faster                                                  |
| asyncio_tcp                | 972 ms                                                                | 928 ms: 1.05x faster                                                  |
| async_tree_none            | 523 ms                                                                | 499 ms: 1.05x faster                                                  |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 2.74 sec: 1.03x faster                                                |
| coroutines                 | 29.3 ms                                                               | 31.6 ms: 1.08x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.08x faster                                                          |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 126 ms                                                                | 118 ms: 1.06x faster                                                  |
| pidigits       | 256 ms                                                                | 243 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.05x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 174 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (3): regex_v8, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.33 us: 1.18x faster                                                 |
| unpickle             | 22.2 us                                                               | 19.8 us: 1.12x faster                                                 |
| tomli_loads          | 2.84 sec                                                              | 2.66 sec: 1.07x faster                                                |
| xml_etree_parse      | 216 ms                                                                | 230 ms: 1.06x slower                                                  |
| unpickle_list        | 6.78 us                                                               | 7.22 us: 1.06x slower                                                 |
| unpickle_pure_python | 285 us                                                                | 306 us: 1.07x slower                                                  |
| json_dumps           | 13.9 ms                                                               | 15.5 ms: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (7): xml_etree_iterparse, xml_etree_generate, json_loads, xml_etree_process, pickle_dict, pickle_pure_python, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 22.1 ms: 1.06x faster                                                 |
| python_startup_no_site | 16.0 ms                                                               | 15.0 ms: 1.06x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.06x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 46.1 ms                                                               | 44.0 ms: 1.05x faster                                                 |
| genshi_text     | 31.6 ms                                                               | 30.2 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 10.9 ms: 20.98x faster                                                |
| deepcopy                   | 498 us                                                                | 372 us: 1.34x faster                                                  |
| deepcopy_memo              | 50.9 us                                                               | 38.4 us: 1.33x faster                                                 |
| async_tree_memoization     | 775 ms                                                                | 626 ms: 1.24x faster                                                  |
| pathlib                    | 31.8 ms                                                               | 26.6 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 4.31 us                                                               | 3.64 us: 1.18x faster                                                 |
| pickle_list                | 7.48 us                                                               | 6.33 us: 1.18x faster                                                 |
| async_tree_memoization_tg  | 692 ms                                                                | 591 ms: 1.17x faster                                                  |
| async_tree_io_tg           | 1.43 sec                                                              | 1.22 sec: 1.17x faster                                                |
| async_tree_none_tg         | 526 ms                                                                | 451 ms: 1.17x faster                                                  |
| logging_simple             | 9.16 us                                                               | 7.95 us: 1.15x faster                                                 |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 5.99 ms: 1.14x faster                                                 |
| sqlglot_parse              | 1.92 ms                                                               | 1.69 ms: 1.13x faster                                                 |
| meteor_contest             | 156 ms                                                                | 138 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 794 ms: 1.13x faster                                                  |
| unpickle                   | 22.2 us                                                               | 19.8 us: 1.12x faster                                                 |
| richards_super             | 73.5 ms                                                               | 66.2 ms: 1.11x faster                                                 |
| tornado_http               | 253 ms                                                                | 228 ms: 1.11x faster                                                  |
| deltablue                  | 4.55 ms                                                               | 4.11 ms: 1.11x faster                                                 |
| async_tree_io              | 1.39 sec                                                              | 1.26 sec: 1.10x faster                                                |
| mdp                        | 4.01 sec                                                              | 3.64 sec: 1.10x faster                                                |
| sympy_sum                  | 226 ms                                                                | 207 ms: 1.09x faster                                                  |
| sympy_str                  | 376 ms                                                                | 345 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 806 ms: 1.09x faster                                                  |
| regex_compile              | 189 ms                                                                | 174 ms: 1.09x faster                                                  |
| richards                   | 68.8 ms                                                               | 63.4 ms: 1.09x faster                                                 |
| comprehensions             | 22.6 us                                                               | 20.9 us: 1.08x faster                                                 |
| pyflate                    | 710 ms                                                                | 657 ms: 1.08x faster                                                  |
| sympy_expand               | 638 ms                                                                | 591 ms: 1.08x faster                                                  |
| logging_silent             | 137 ns                                                                | 128 ns: 1.07x faster                                                  |
| create_gc_cycles           | 2.49 ms                                                               | 2.32 ms: 1.07x faster                                                 |
| tomli_loads                | 2.84 sec                                                              | 2.66 sec: 1.07x faster                                                |
| bpe_tokeniser              | 6.53 sec                                                              | 6.13 sec: 1.07x faster                                                |
| nbody                      | 126 ms                                                                | 118 ms: 1.06x faster                                                  |
| python_startup             | 23.5 ms                                                               | 22.1 ms: 1.06x faster                                                 |
| python_startup_no_site     | 16.0 ms                                                               | 15.0 ms: 1.06x faster                                                 |
| sqlglot_transpile          | 2.24 ms                                                               | 2.12 ms: 1.06x faster                                                 |
| gc_traversal               | 5.80 ms                                                               | 5.48 ms: 1.06x faster                                                 |
| pidigits                   | 256 ms                                                                | 243 ms: 1.05x faster                                                  |
| scimark_sor                | 176 ms                                                                | 168 ms: 1.05x faster                                                  |
| django_template            | 46.1 ms                                                               | 44.0 ms: 1.05x faster                                                 |
| pycparser                  | 1.71 sec                                                              | 1.63 sec: 1.05x faster                                                |
| logging_format             | 9.36 us                                                               | 8.93 us: 1.05x faster                                                 |
| pprint_pformat             | 2.04 sec                                                              | 1.94 sec: 1.05x faster                                                |
| asyncio_tcp                | 972 ms                                                                | 928 ms: 1.05x faster                                                  |
| async_tree_none            | 523 ms                                                                | 499 ms: 1.05x faster                                                  |
| genshi_text                | 31.6 ms                                                               | 30.2 ms: 1.05x faster                                                 |
| sqlglot_normalize          | 150 ms                                                                | 144 ms: 1.04x faster                                                  |
| raytrace                   | 351 ms                                                                | 338 ms: 1.04x faster                                                  |
| generators                 | 40.7 ms                                                               | 39.3 ms: 1.04x faster                                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 2.74 sec: 1.03x faster                                                |
| typing_runtime_protocols   | 222 us                                                                | 234 us: 1.06x slower                                                  |
| xml_etree_parse            | 216 ms                                                                | 230 ms: 1.06x slower                                                  |
| unpickle_list              | 6.78 us                                                               | 7.22 us: 1.06x slower                                                 |
| unpickle_pure_python       | 285 us                                                                | 306 us: 1.07x slower                                                  |
| coroutines                 | 29.3 ms                                                               | 31.6 ms: 1.08x slower                                                 |
| nqueens                    | 108 ms                                                                | 117 ms: 1.08x slower                                                  |
| json_dumps                 | 13.9 ms                                                               | 15.5 ms: 1.11x slower                                                 |
| unpack_sequence            | 54.6 ns                                                               | 67.4 ns: 1.23x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.08x faster                                                          |

Benchmark hidden because not significant (38): bench_mp_pool, 2to3, regex_v8, xml_etree_iterparse, chaos, go, float, coverage, xml_etree_generate, sympy_integrate, scimark_monte_carlo, mako, json_loads, pprint_safe_repr, crypto_pyaes, bench_thread_pool, async_generators, xml_etree_process, json, sqlglot_optimize, spectral_norm, regex_dna, docutils, fannkuch, scimark_fft, pickle_dict, pickle_pure_python, hexiom, html5lib, thrift, dask, genshi_xml, pylint, pickle, asyncio_websockets, regex_effbot, scimark_lu, sqlite_synth
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.01x