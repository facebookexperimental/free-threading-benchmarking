# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d343f97
- commit date: 2024-09-06
- overall geometric mean: 1.02x faster
- HPT reliability: 55.22%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| docutils       | 3.94 sec                                                              | 4.12 sec: 1.05x slower                                |
| tornado_http   | 253 ms                                                                | 270 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization | 775 ms                                                                | 686 ms: 1.13x faster                                  |
| coroutines             | 29.3 ms                                                               | 30.8 ms: 1.05x slower                                 |
| asyncio_tcp_ssl        | 2.83 sec                                                              | 2.99 sec: 1.06x slower                                |
| asyncio_websockets     | 728 ms                                                                | 786 ms: 1.08x slower                                  |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (9): async_tree_none, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_generators, async_tree_io, async_tree_cpu_io_mixed_tg, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 247 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 32.1 ms: 1.15x faster                                 |
| regex_dna      | 284 ms                                                                | 297 ms: 1.05x slower                                  |
| regex_effbot   | 4.63 ms                                                               | 4.96 ms: 1.07x slower                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|--------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle           | 22.2 us                                                               | 19.9 us: 1.11x faster                                 |
| xml_etree_generate | 120 ms                                                                | 125 ms: 1.05x slower                                  |
| pickle_dict        | 46.5 us                                                               | 49.2 us: 1.06x slower                                 |
| xml_etree_parse    | 216 ms                                                                | 233 ms: 1.08x slower                                  |
| unpickle_list      | 6.78 us                                                               | 7.33 us: 1.08x slower                                 |
| json_loads         | 37.9 us                                                               | 41.2 us: 1.09x slower                                 |
| pickle             | 15.2 us                                                               | 16.6 us: 1.09x slower                                 |
| Geometric mean     | (ref)                                                                 | 1.04x slower                                          |

Benchmark hidden because not significant (7): tomli_loads, xml_etree_process, pickle_list, unpickle_pure_python, json_dumps, xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 25.6 ms: 1.09x slower                                 |
| python_startup_no_site | 16.0 ms                                                               | 17.8 ms: 1.12x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.10x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.1 ms                                                               | 48.4 ms: 1.05x slower                                 |
| genshi_text     | 31.6 ms                                                               | 34.1 ms: 1.08x slower                                 |
| mako            | 16.7 ms                                                               | 19.0 ms: 1.14x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.08x slower                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                  | 229 ms                                                                | 11.9 ms: 19.31x faster                                |
| deepcopy               | 498 us                                                                | 341 us: 1.46x faster                                  |
| deepcopy_memo          | 50.9 us                                                               | 39.8 us: 1.28x faster                                 |
| deepcopy_reduce        | 4.31 us                                                               | 3.61 us: 1.19x faster                                 |
| regex_v8               | 37.1 ms                                                               | 32.1 ms: 1.15x faster                                 |
| go                     | 193 ms                                                                | 171 ms: 1.13x faster                                  |
| async_tree_memoization | 775 ms                                                                | 686 ms: 1.13x faster                                  |
| unpickle               | 22.2 us                                                               | 19.9 us: 1.11x faster                                 |
| richards               | 68.8 ms                                                               | 63.3 ms: 1.09x faster                                 |
| crypto_pyaes           | 102 ms                                                                | 93.8 ms: 1.08x faster                                 |
| pathlib                | 31.8 ms                                                               | 30.0 ms: 1.06x faster                                 |
| pidigits               | 256 ms                                                                | 247 ms: 1.04x faster                                  |
| pprint_pformat         | 2.04 sec                                                              | 1.98 sec: 1.03x faster                                |
| scimark_lu             | 150 ms                                                                | 156 ms: 1.04x slower                                  |
| xml_etree_generate     | 120 ms                                                                | 125 ms: 1.05x slower                                  |
| docutils               | 3.94 sec                                                              | 4.12 sec: 1.05x slower                                |
| regex_dna              | 284 ms                                                                | 297 ms: 1.05x slower                                  |
| coroutines             | 29.3 ms                                                               | 30.8 ms: 1.05x slower                                 |
| django_template        | 46.1 ms                                                               | 48.4 ms: 1.05x slower                                 |
| pickle_dict            | 46.5 us                                                               | 49.2 us: 1.06x slower                                 |
| asyncio_tcp_ssl        | 2.83 sec                                                              | 2.99 sec: 1.06x slower                                |
| spectral_norm          | 151 ms                                                                | 160 ms: 1.06x slower                                  |
| scimark_fft            | 469 ms                                                                | 499 ms: 1.06x slower                                  |
| tornado_http           | 253 ms                                                                | 270 ms: 1.07x slower                                  |
| nqueens                | 108 ms                                                                | 116 ms: 1.07x slower                                  |
| logging_silent         | 137 ns                                                                | 146 ns: 1.07x slower                                  |
| regex_effbot           | 4.63 ms                                                               | 4.96 ms: 1.07x slower                                 |
| json                   | 6.79 ms                                                               | 7.28 ms: 1.07x slower                                 |
| genshi_text            | 31.6 ms                                                               | 34.1 ms: 1.08x slower                                 |
| xml_etree_parse        | 216 ms                                                                | 233 ms: 1.08x slower                                  |
| asyncio_websockets     | 728 ms                                                                | 786 ms: 1.08x slower                                  |
| unpickle_list          | 6.78 us                                                               | 7.33 us: 1.08x slower                                 |
| create_gc_cycles       | 2.49 ms                                                               | 2.70 ms: 1.09x slower                                 |
| python_startup         | 23.5 ms                                                               | 25.6 ms: 1.09x slower                                 |
| json_loads             | 37.9 us                                                               | 41.2 us: 1.09x slower                                 |
| pickle                 | 15.2 us                                                               | 16.6 us: 1.09x slower                                 |
| gc_traversal           | 5.80 ms                                                               | 6.35 ms: 1.09x slower                                 |
| python_startup_no_site | 16.0 ms                                                               | 17.8 ms: 1.12x slower                                 |
| mako                   | 16.7 ms                                                               | 19.0 ms: 1.14x slower                                 |
| unpack_sequence        | 54.6 ns                                                               | 62.2 ns: 1.14x slower                                 |
| logging_format         | 9.36 us                                                               | 10.7 us: 1.15x slower                                 |
| bench_mp_pool          | 19.7 ms                                                               | 22.8 ms: 1.16x slower                                 |
| bench_thread_pool      | 3.01 ms                                                               | 3.86 ms: 1.28x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (54): async_tree_none, logging_simple, async_tree_memoization_tg, html5lib, coverage, async_tree_io_tg, pyflate, nbody, meteor_contest, sqlglot_optimize, sympy_expand, pycparser, sqlglot_normalize, sympy_sum, sqlglot_transpile, async_tree_none_tg, scimark_sor, async_tree_cpu_io_mixed, sympy_str, bpe_tokeniser, typing_runtime_protocols, async_generators, tomli_loads, thrift, async_tree_io, richards_super, deltablue, xml_etree_process, async_tree_cpu_io_mixed_tg, pickle_list, scimark_sparse_mat_mult, comprehensions, 2to3, chaos, regex_compile, pprint_safe_repr, hexiom, asyncio_tcp, mdp, sqlite_synth, generators, raytrace, scimark_monte_carlo, unpickle_pure_python, fannkuch, dulwich_log, json_dumps, sympy_integrate, float, xml_etree_iterparse, genshi_xml, sqlglot_parse, pickle_pure_python, pylint
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 55.22% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x