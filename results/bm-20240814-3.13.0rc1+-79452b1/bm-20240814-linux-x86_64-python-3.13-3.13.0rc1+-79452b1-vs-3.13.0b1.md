# Results vs. 3.13.0b1

- fork: python
- ref: 3.13
- machine: linux-x86_64
- commit hash: 79452b1
- commit date: 2024-08-14
- overall geometric mean: 1.03x faster
- HPT reliability: 97.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| html5lib       | 92.0 ms                                                               | 98.1 ms: 1.07x slower                                   |
| Geometric mean | (ref)                                                                 | 1.02x slower                                            |

Benchmark hidden because not significant (4): 2to3, chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|--------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| asyncio_websockets | 728 ms                                                                | 772 ms: 1.06x slower                                    |
| async_tree_none    | 523 ms                                                                | 576 ms: 1.10x slower                                    |
| Geometric mean     | (ref)                                                                 | 1.00x slower                                            |

Benchmark hidden because not significant (11): async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, asyncio_tcp_ssl, async_tree_none_tg, async_tree_io, coroutines, async_tree_cpu_io_mixed, async_generators, asyncio_tcp, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| pidigits       | 256 ms                                                                | 248 ms: 1.03x faster                                    |
| Geometric mean | (ref)                                                                 | 1.02x faster                                            |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 32.4 ms: 1.14x faster                                   |
| regex_compile  | 189 ms                                                                | 177 ms: 1.07x faster                                    |
| regex_effbot   | 4.63 ms                                                               | 4.84 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                                 | 1.04x faster                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.82 us: 1.10x faster                                   |
| json_loads           | 37.9 us                                                               | 36.1 us: 1.05x faster                                   |
| unpickle_pure_python | 285 us                                                                | 296 us: 1.04x slower                                    |
| xml_etree_process    | 82.2 ms                                                               | 86.5 ms: 1.05x slower                                   |
| json_dumps           | 13.9 ms                                                               | 14.9 ms: 1.07x slower                                   |
| xml_etree_generate   | 120 ms                                                                | 129 ms: 1.08x slower                                    |
| xml_etree_iterparse  | 163 ms                                                                | 176 ms: 1.08x slower                                    |
| xml_etree_parse      | 216 ms                                                                | 236 ms: 1.09x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                            |

Benchmark hidden because not significant (6): unpickle, pickle_pure_python, unpickle_list, tomli_loads, pickle_dict, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 14.6 ms: 1.09x faster                                   |
| python_startup         | 23.5 ms                                                               | 22.0 ms: 1.07x faster                                   |
| Geometric mean         | (ref)                                                                 | 1.08x faster                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| genshi_xml     | 71.9 ms                                                               | 68.3 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                                 | 1.02x faster                                            |

Benchmark hidden because not significant (3): mako, genshi_text, django_template

All benchmarks:
===============

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| telco                  | 229 ms                                                                | 11.4 ms: 20.09x faster                                  |
| regex_v8               | 37.1 ms                                                               | 32.4 ms: 1.14x faster                                   |
| pickle_list            | 7.48 us                                                               | 6.82 us: 1.10x faster                                   |
| coverage               | 121 ms                                                                | 110 ms: 1.10x faster                                    |
| python_startup_no_site | 16.0 ms                                                               | 14.6 ms: 1.09x faster                                   |
| pycparser              | 1.71 sec                                                              | 1.57 sec: 1.09x faster                                  |
| pathlib                | 31.8 ms                                                               | 29.3 ms: 1.08x faster                                   |
| comprehensions         | 22.6 us                                                               | 20.9 us: 1.08x faster                                   |
| pyflate                | 710 ms                                                                | 661 ms: 1.07x faster                                    |
| regex_compile          | 189 ms                                                                | 177 ms: 1.07x faster                                    |
| python_startup         | 23.5 ms                                                               | 22.0 ms: 1.07x faster                                   |
| sqlglot_parse          | 1.92 ms                                                               | 1.80 ms: 1.07x faster                                   |
| sympy_sum              | 226 ms                                                                | 213 ms: 1.06x faster                                    |
| mdp                    | 4.01 sec                                                              | 3.80 sec: 1.06x faster                                  |
| genshi_xml             | 71.9 ms                                                               | 68.3 ms: 1.05x faster                                   |
| logging_silent         | 137 ns                                                                | 130 ns: 1.05x faster                                    |
| json_loads             | 37.9 us                                                               | 36.1 us: 1.05x faster                                   |
| bpe_tokeniser          | 6.53 sec                                                              | 6.25 sec: 1.05x faster                                  |
| generators             | 40.7 ms                                                               | 39.2 ms: 1.04x faster                                   |
| json                   | 6.79 ms                                                               | 6.55 ms: 1.04x faster                                   |
| pprint_safe_repr       | 991 ms                                                                | 959 ms: 1.03x faster                                    |
| pidigits               | 256 ms                                                                | 248 ms: 1.03x faster                                    |
| unpickle_pure_python   | 285 us                                                                | 296 us: 1.04x slower                                    |
| regex_effbot           | 4.63 ms                                                               | 4.84 ms: 1.04x slower                                   |
| xml_etree_process      | 82.2 ms                                                               | 86.5 ms: 1.05x slower                                   |
| spectral_norm          | 151 ms                                                                | 159 ms: 1.05x slower                                    |
| asyncio_websockets     | 728 ms                                                                | 772 ms: 1.06x slower                                    |
| html5lib               | 92.0 ms                                                               | 98.1 ms: 1.07x slower                                   |
| json_dumps             | 13.9 ms                                                               | 14.9 ms: 1.07x slower                                   |
| xml_etree_generate     | 120 ms                                                                | 129 ms: 1.08x slower                                    |
| xml_etree_iterparse    | 163 ms                                                                | 176 ms: 1.08x slower                                    |
| flaskblogging          | 8.08 ms                                                               | 8.78 ms: 1.09x slower                                   |
| xml_etree_parse        | 216 ms                                                                | 236 ms: 1.09x slower                                    |
| async_tree_none        | 523 ms                                                                | 576 ms: 1.10x slower                                    |
| gunicorn               | 1.89 ms                                                               | 2.25 ms: 1.19x slower                                   |
| unpack_sequence        | 54.6 ns                                                               | 73.9 ns: 1.35x slower                                   |
| Geometric mean         | (ref)                                                                 | 1.03x faster                                            |

Benchmark hidden because not significant (66): richards, async_tree_memoization, unpickle, mako, async_tree_cpu_io_mixed_tg, sqlglot_normalize, deepcopy, async_tree_memoization_tg, pickle_pure_python, typing_runtime_protocols, sympy_str, scimark_sor, sqlglot_optimize, logging_simple, crypto_pyaes, pprint_pformat, tornado_http, bench_mp_pool, unpickle_list, nbody, tomli_loads, sympy_expand, asyncio_tcp_ssl, create_gc_cycles, async_tree_none_tg, deepcopy_reduce, hexiom, async_tree_io, coroutines, aiohttp, raytrace, nqueens, float, async_tree_cpu_io_mixed, pickle_dict, 2to3, deltablue, genshi_text, meteor_contest, async_generators, pickle, scimark_monte_carlo, go, pylint, logging_format, asyncio_tcp, fannkuch, scimark_fft, regex_dna, deepcopy_memo, docutils, async_tree_io_tg, django_template, bench_thread_pool, dask, gc_traversal, scimark_sparse_mat_mult, sqlglot_transpile, dulwich_log, thrift, chameleon, scimark_lu, sympy_integrate, sqlite_synth, richards_super, chaos

# HPT report

- Reliability score: 97.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x