# Results vs. 3.13.0b1

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.05x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization | 775 ms                                                                | 709 ms: 1.09x faster                                         |
| async_generators       | 588 ms                                                                | 567 ms: 1.04x faster                                         |
| coroutines             | 29.3 ms                                                               | 30.9 ms: 1.05x slower                                        |
| asyncio_websockets     | 728 ms                                                                | 766 ms: 1.05x slower                                         |
| async_tree_none        | 523 ms                                                                | 572 ms: 1.09x slower                                         |
| Geometric mean         | (ref)                                                                 | 1.01x faster                                                 |

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, asyncio_tcp, async_tree_io_tg, asyncio_tcp_ssl, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 126 ms                                                                | 119 ms: 1.06x faster                                         |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                 |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 32.8 ms: 1.13x faster                                        |
| Geometric mean | (ref)                                                                 | 1.04x faster                                                 |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|---------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_loads          | 37.9 us                                                               | 34.3 us: 1.10x faster                                        |
| pickle_list         | 7.48 us                                                               | 6.86 us: 1.09x faster                                        |
| unpickle            | 22.2 us                                                               | 20.5 us: 1.08x faster                                        |
| xml_etree_process   | 82.2 ms                                                               | 85.9 ms: 1.04x slower                                        |
| xml_etree_parse     | 216 ms                                                                | 231 ms: 1.07x slower                                         |
| xml_etree_iterparse | 163 ms                                                                | 177 ms: 1.09x slower                                         |
| Geometric mean      | (ref)                                                                 | 1.01x faster                                                 |

Benchmark hidden because not significant (8): pickle_pure_python, tomli_loads, unpickle_list, pickle, json_dumps, pickle_dict, unpickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 22.4 ms: 1.05x faster                                        |
| python_startup_no_site | 16.0 ms                                                               | 15.3 ms: 1.04x faster                                        |
| Geometric mean         | (ref)                                                                 | 1.05x faster                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 46.1 ms                                                               | 44.3 ms: 1.04x faster                                        |
| Geometric mean  | (ref)                                                                 | 1.02x faster                                                 |

Benchmark hidden because not significant (3): mako, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| telco                  | 229 ms                                                                | 12.2 ms: 18.82x faster                                       |
| regex_v8               | 37.1 ms                                                               | 32.8 ms: 1.13x faster                                        |
| coverage               | 121 ms                                                                | 107 ms: 1.12x faster                                         |
| json_loads             | 37.9 us                                                               | 34.3 us: 1.10x faster                                        |
| aiohttp                | 2.24 ms                                                               | 2.03 ms: 1.10x faster                                        |
| async_tree_memoization | 775 ms                                                                | 709 ms: 1.09x faster                                         |
| sqlglot_parse          | 1.92 ms                                                               | 1.76 ms: 1.09x faster                                        |
| pickle_list            | 7.48 us                                                               | 6.86 us: 1.09x faster                                        |
| pycparser              | 1.71 sec                                                              | 1.57 sec: 1.09x faster                                       |
| unpickle               | 22.2 us                                                               | 20.5 us: 1.08x faster                                        |
| sympy_sum              | 226 ms                                                                | 210 ms: 1.08x faster                                         |
| sqlglot_normalize      | 150 ms                                                                | 140 ms: 1.08x faster                                         |
| pyflate                | 710 ms                                                                | 664 ms: 1.07x faster                                         |
| logging_simple         | 9.16 us                                                               | 8.56 us: 1.07x faster                                        |
| sympy_expand           | 638 ms                                                                | 601 ms: 1.06x faster                                         |
| pathlib                | 31.8 ms                                                               | 29.9 ms: 1.06x faster                                        |
| nbody                  | 126 ms                                                                | 119 ms: 1.06x faster                                         |
| mdp                    | 4.01 sec                                                              | 3.80 sec: 1.05x faster                                       |
| logging_silent         | 137 ns                                                                | 130 ns: 1.05x faster                                         |
| deepcopy_reduce        | 4.31 us                                                               | 4.10 us: 1.05x faster                                        |
| richards               | 68.8 ms                                                               | 65.5 ms: 1.05x faster                                        |
| python_startup         | 23.5 ms                                                               | 22.4 ms: 1.05x faster                                        |
| pprint_pformat         | 2.04 sec                                                              | 1.94 sec: 1.05x faster                                       |
| python_startup_no_site | 16.0 ms                                                               | 15.3 ms: 1.04x faster                                        |
| json                   | 6.79 ms                                                               | 6.51 ms: 1.04x faster                                        |
| django_template        | 46.1 ms                                                               | 44.3 ms: 1.04x faster                                        |
| dulwich_log            | 97.5 ms                                                               | 93.7 ms: 1.04x faster                                        |
| bpe_tokeniser          | 6.53 sec                                                              | 6.28 sec: 1.04x faster                                       |
| async_generators       | 588 ms                                                                | 567 ms: 1.04x faster                                         |
| xml_etree_process      | 82.2 ms                                                               | 85.9 ms: 1.04x slower                                        |
| coroutines             | 29.3 ms                                                               | 30.9 ms: 1.05x slower                                        |
| sympy_integrate        | 28.7 ms                                                               | 30.2 ms: 1.05x slower                                        |
| asyncio_websockets     | 728 ms                                                                | 766 ms: 1.05x slower                                         |
| xml_etree_parse        | 216 ms                                                                | 231 ms: 1.07x slower                                         |
| xml_etree_iterparse    | 163 ms                                                                | 177 ms: 1.09x slower                                         |
| async_tree_none        | 523 ms                                                                | 572 ms: 1.09x slower                                         |
| unpack_sequence        | 54.6 ns                                                               | 74.3 ns: 1.36x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (65): bench_mp_pool, flaskblogging, async_tree_none_tg, mako, bench_thread_pool, sqlglot_optimize, meteor_contest, regex_compile, hexiom, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, create_gc_cycles, pickle_pure_python, chameleon, asyncio_tcp, deltablue, scimark_lu, sqlglot_transpile, async_tree_io_tg, tomli_loads, raytrace, comprehensions, pidigits, asyncio_tcp_ssl, gc_traversal, generators, crypto_pyaes, deepcopy_memo, unpickle_list, logging_format, scimark_sparse_mat_mult, go, async_tree_cpu_io_mixed, tornado_http, regex_dna, pickle, pprint_safe_repr, richards_super, async_tree_io, deepcopy, genshi_text, genshi_xml, html5lib, float, sympy_str, pylint, scimark_fft, 2to3, gunicorn, sqlite_synth, thrift, scimark_sor, json_dumps, pickle_dict, typing_runtime_protocols, unpickle_pure_python, docutils, scimark_monte_carlo, xml_etree_generate, fannkuch, regex_effbot, chaos, dask, nqueens, spectral_norm

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x