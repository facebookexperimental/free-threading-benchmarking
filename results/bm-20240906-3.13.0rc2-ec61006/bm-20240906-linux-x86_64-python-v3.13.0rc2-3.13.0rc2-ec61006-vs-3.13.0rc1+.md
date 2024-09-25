# Results vs. 3.13.0rc1+

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.01x faster
- HPT reliability: 56.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| chameleon      | 9.84 ms                                                 | 9.34 ms: 1.05x faster                                        |
| html5lib       | 98.1 ms                                                 | 92.6 ms: 1.06x faster                                        |
| Geometric mean | (ref)                                                   | 1.02x faster                                                 |

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| async_generators | 592 ms                                                  | 567 ms: 1.04x faster                                         |
| coroutines       | 29.2 ms                                                 | 30.9 ms: 1.06x slower                                        |
| Geometric mean   | (ref)                                                   | 1.01x faster                                                 |

Benchmark hidden because not significant (11): async_tree_memoization, asyncio_tcp, async_tree_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_none, asyncio_tcp_ssl, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_dna, regex_effbot, regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|--------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_generate | 129 ms                                                  | 122 ms: 1.06x faster                                         |
| json_loads         | 36.1 us                                                 | 34.3 us: 1.05x faster                                        |
| json_dumps         | 14.9 ms                                                 | 14.1 ms: 1.05x faster                                        |
| Geometric mean     | (ref)                                                   | 1.02x faster                                                 |

Benchmark hidden because not significant (11): unpickle, xml_etree_parse, unpickle_pure_python, pickle, tomli_loads, xml_etree_process, pickle_pure_python, unpickle_list, xml_etree_iterparse, pickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 15.3 ms: 1.05x slower                                        |
| Geometric mean         | (ref)                                                   | 1.03x slower                                                 |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 46.9 ms                                                 | 44.3 ms: 1.06x faster                                        |
| genshi_xml      | 68.3 ms                                                 | 72.1 ms: 1.06x slower                                        |
| Geometric mean  | (ref)                                                   | 1.00x faster                                                 |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:-------------------------------------------------------:|:------------------------------------------------------------:|
| gunicorn               | 2.25 ms                                                 | 1.91 ms: 1.18x faster                                        |
| flaskblogging          | 8.78 ms                                                 | 7.68 ms: 1.14x faster                                        |
| aiohttp                | 2.23 ms                                                 | 2.03 ms: 1.10x faster                                        |
| dulwich_log            | 100.0 ms                                                | 93.7 ms: 1.07x faster                                        |
| html5lib               | 98.1 ms                                                 | 92.6 ms: 1.06x faster                                        |
| django_template        | 46.9 ms                                                 | 44.3 ms: 1.06x faster                                        |
| xml_etree_generate     | 129 ms                                                  | 122 ms: 1.06x faster                                         |
| json_loads             | 36.1 us                                                 | 34.3 us: 1.05x faster                                        |
| json_dumps             | 14.9 ms                                                 | 14.1 ms: 1.05x faster                                        |
| chameleon              | 9.84 ms                                                 | 9.34 ms: 1.05x faster                                        |
| scimark_lu             | 154 ms                                                  | 146 ms: 1.05x faster                                         |
| sympy_expand           | 631 ms                                                  | 601 ms: 1.05x faster                                         |
| meteor_contest         | 157 ms                                                  | 150 ms: 1.05x faster                                         |
| sqlglot_normalize      | 146 ms                                                  | 140 ms: 1.04x faster                                         |
| async_generators       | 592 ms                                                  | 567 ms: 1.04x faster                                         |
| deepcopy_reduce        | 4.27 us                                                 | 4.10 us: 1.04x faster                                        |
| pprint_pformat         | 2.00 sec                                                | 1.94 sec: 1.03x faster                                       |
| pprint_safe_repr       | 959 ms                                                  | 987 ms: 1.03x slower                                         |
| scimark_sor            | 172 ms                                                  | 179 ms: 1.04x slower                                         |
| python_startup_no_site | 14.6 ms                                                 | 15.3 ms: 1.05x slower                                        |
| genshi_xml             | 68.3 ms                                                 | 72.1 ms: 1.06x slower                                        |
| coroutines             | 29.2 ms                                                 | 30.9 ms: 1.06x slower                                        |
| comprehensions         | 20.9 us                                                 | 22.2 us: 1.06x slower                                        |
| telco                  | 11.4 ms                                                 | 12.2 ms: 1.07x slower                                        |
| Geometric mean         | (ref)                                                   | 1.01x faster                                                 |

Benchmark hidden because not significant (78): bench_thread_pool, async_tree_memoization, logging_simple, sqlglot_transpile, nbody, richards_super, unpickle, asyncio_tcp, async_tree_io_tg, gc_traversal, bench_mp_pool, async_tree_none_tg, scimark_sparse_mat_mult, deepcopy_memo, hexiom, deltablue, logging_format, coverage, sqlglot_parse, go, regex_dna, regex_effbot, xml_etree_parse, sqlite_synth, sqlglot_optimize, create_gc_cycles, unpickle_pure_python, raytrace, spectral_norm, sympy_sum, pickle, chaos, thrift, async_tree_cpu_io_mixed, asyncio_websockets, tomli_loads, xml_etree_process, mako, async_tree_none, scimark_fft, asyncio_tcp_ssl, json, richards, pylint, genshi_text, async_tree_memoization_tg, pycparser, pickle_pure_python, logging_silent, docutils, mdp, unpickle_list, async_tree_cpu_io_mixed_tg, crypto_pyaes, xml_etree_iterparse, pyflate, bpe_tokeniser, unpack_sequence, pickle_list, async_tree_io, 2to3, fannkuch, float, scimark_monte_carlo, dask, regex_v8, tornado_http, pidigits, pickle_dict, python_startup, sympy_integrate, pathlib, generators, regex_compile, deepcopy, sympy_str, nqueens, typing_runtime_protocols

# HPT report

- Reliability score: 56.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x