# Results vs. 3.13.0b1

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.01x faster
- HPT reliability: 73.38%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 3.94 sec                                                              | 4.22 sec: 1.07x slower                                                |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization    | 775 ms                                                                | 647 ms: 1.20x faster                                                  |
| async_tree_io_tg          | 1.43 sec                                                              | 1.33 sec: 1.08x faster                                                |
| async_tree_memoization_tg | 692 ms                                                                | 643 ms: 1.08x faster                                                  |
| async_tree_none_tg        | 526 ms                                                                | 494 ms: 1.07x faster                                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 2.90 sec: 1.03x slower                                                |
| asyncio_websockets        | 728 ms                                                                | 781 ms: 1.07x slower                                                  |
| Geometric mean            | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_tcp, async_tree_none, async_generators, coroutines, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                                | 125 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                          |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 310 ms: 1.09x slower                                                  |
| regex_effbot   | 4.63 ms                                                               | 5.19 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle             | 22.2 us                                                               | 20.6 us: 1.08x faster                                                 |
| tomli_loads          | 2.84 sec                                                              | 2.72 sec: 1.04x faster                                                |
| unpickle_pure_python | 285 us                                                                | 299 us: 1.05x slower                                                  |
| xml_etree_process    | 82.2 ms                                                               | 86.8 ms: 1.06x slower                                                 |
| unpickle_list        | 6.78 us                                                               | 7.18 us: 1.06x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 128 ms: 1.07x slower                                                  |
| json_dumps           | 13.9 ms                                                               | 15.4 ms: 1.11x slower                                                 |
| xml_etree_iterparse  | 163 ms                                                                | 182 ms: 1.12x slower                                                  |
| xml_etree_parse      | 216 ms                                                                | 253 ms: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.03x slower                                                          |

Benchmark hidden because not significant (5): pickle_list, pickle_pure_python, pickle_dict, json_loads, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 26.1 ms: 1.11x slower                                                 |
| python_startup_no_site | 16.0 ms                                                               | 17.7 ms: 1.11x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 16.7 ms                                                               | 18.5 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                          |

Benchmark hidden because not significant (3): genshi_text, genshi_xml, django_template

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                     | 229 ms                                                                | 11.5 ms: 19.86x faster                                                |
| deepcopy                  | 498 us                                                                | 362 us: 1.38x faster                                                  |
| deepcopy_memo             | 50.9 us                                                               | 39.5 us: 1.29x faster                                                 |
| async_tree_memoization    | 775 ms                                                                | 647 ms: 1.20x faster                                                  |
| go                        | 193 ms                                                                | 168 ms: 1.15x faster                                                  |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 6.13 ms: 1.11x faster                                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.33 sec: 1.08x faster                                                |
| async_tree_memoization_tg | 692 ms                                                                | 643 ms: 1.08x faster                                                  |
| unpickle                  | 22.2 us                                                               | 20.6 us: 1.08x faster                                                 |
| sympy_sum                 | 226 ms                                                                | 211 ms: 1.07x faster                                                  |
| logging_simple            | 9.16 us                                                               | 8.60 us: 1.07x faster                                                 |
| async_tree_none_tg        | 526 ms                                                                | 494 ms: 1.07x faster                                                  |
| crypto_pyaes              | 102 ms                                                                | 95.7 ms: 1.06x faster                                                 |
| deepcopy_reduce           | 4.31 us                                                               | 4.09 us: 1.05x faster                                                 |
| tomli_loads               | 2.84 sec                                                              | 2.72 sec: 1.04x faster                                                |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 2.90 sec: 1.03x slower                                                |
| pycparser                 | 1.71 sec                                                              | 1.79 sec: 1.05x slower                                                |
| unpickle_pure_python      | 285 us                                                                | 299 us: 1.05x slower                                                  |
| logging_silent            | 137 ns                                                                | 143 ns: 1.05x slower                                                  |
| nqueens                   | 108 ms                                                                | 114 ms: 1.05x slower                                                  |
| xml_etree_process         | 82.2 ms                                                               | 86.8 ms: 1.06x slower                                                 |
| fannkuch                  | 535 ms                                                                | 565 ms: 1.06x slower                                                  |
| json                      | 6.79 ms                                                               | 7.18 ms: 1.06x slower                                                 |
| unpickle_list             | 6.78 us                                                               | 7.18 us: 1.06x slower                                                 |
| spectral_norm             | 151 ms                                                                | 161 ms: 1.06x slower                                                  |
| gc_traversal              | 5.80 ms                                                               | 6.19 ms: 1.07x slower                                                 |
| sympy_str                 | 376 ms                                                                | 402 ms: 1.07x slower                                                  |
| xml_etree_generate        | 120 ms                                                                | 128 ms: 1.07x slower                                                  |
| docutils                  | 3.94 sec                                                              | 4.22 sec: 1.07x slower                                                |
| asyncio_websockets        | 728 ms                                                                | 781 ms: 1.07x slower                                                  |
| thrift                    | 1.09 ms                                                               | 1.17 ms: 1.08x slower                                                 |
| create_gc_cycles          | 2.49 ms                                                               | 2.70 ms: 1.09x slower                                                 |
| float                     | 115 ms                                                                | 125 ms: 1.09x slower                                                  |
| hexiom                    | 8.42 ms                                                               | 9.21 ms: 1.09x slower                                                 |
| regex_dna                 | 284 ms                                                                | 310 ms: 1.09x slower                                                  |
| dulwich_log               | 97.5 ms                                                               | 108 ms: 1.10x slower                                                  |
| json_dumps                | 13.9 ms                                                               | 15.4 ms: 1.11x slower                                                 |
| python_startup            | 23.5 ms                                                               | 26.1 ms: 1.11x slower                                                 |
| python_startup_no_site    | 16.0 ms                                                               | 17.7 ms: 1.11x slower                                                 |
| mako                      | 16.7 ms                                                               | 18.5 ms: 1.11x slower                                                 |
| xml_etree_iterparse       | 163 ms                                                                | 182 ms: 1.12x slower                                                  |
| regex_effbot              | 4.63 ms                                                               | 5.19 ms: 1.12x slower                                                 |
| xml_etree_parse           | 216 ms                                                                | 253 ms: 1.17x slower                                                  |
| bench_thread_pool         | 3.01 ms                                                               | 3.89 ms: 1.29x slower                                                 |
| unpack_sequence           | 54.6 ns                                                               | 72.4 ns: 1.33x slower                                                 |
| bench_mp_pool             | 19.7 ms                                                               | 26.6 ms: 1.35x slower                                                 |
| Geometric mean            | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (51): richards, pathlib, richards_super, pickle_list, comprehensions, sqlglot_parse, meteor_contest, scimark_sor, regex_v8, pprint_pformat, pickle_pure_python, mdp, bpe_tokeniser, pickle_dict, sqlglot_optimize, genshi_text, pidigits, scimark_lu, sympy_expand, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, regex_compile, json_loads, asyncio_tcp, scimark_fft, async_tree_none, scimark_monte_carlo, genshi_xml, async_generators, coverage, generators, pprint_safe_repr, sqlglot_normalize, django_template, sqlglot_transpile, coroutines, pickle, raytrace, 2to3, sqlite_synth, async_tree_io, chaos, html5lib, nbody, pyflate, logging_format, sympy_integrate, typing_runtime_protocols, tornado_http, deltablue, pylint
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 73.38% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x