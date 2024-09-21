# Results vs. 3.13.0rc2

- fork: python
- ref: 3.13
- machine: linux-x86_64
- commit hash: 79452b1
- commit date: 2024-08-14
- overall geometric mean: 1.01x slower
- HPT reliability: 56.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------:|
| chameleon      | 9.34 ms                                                      | 9.84 ms: 1.05x slower                                   |
| html5lib       | 92.6 ms                                                      | 98.1 ms: 1.06x slower                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                            |

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------|:------------------------------------------------------------:|:-------------------------------------------------------:|
| coroutines       | 30.9 ms                                                      | 29.2 ms: 1.06x faster                                   |
| async_generators | 567 ms                                                       | 592 ms: 1.04x slower                                    |
| Geometric mean   | (ref)                                                        | 1.01x slower                                            |

Benchmark hidden because not significant (11): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, asyncio_tcp_ssl, async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io_tg, asyncio_tcp, async_tree_memoization

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, float, nbody

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_compile, regex_v8, regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|--------------------|:------------------------------------------------------------:|:-------------------------------------------------------:|
| json_dumps         | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                   |
| json_loads         | 34.3 us                                                      | 36.1 us: 1.05x slower                                   |
| xml_etree_generate | 122 ms                                                       | 129 ms: 1.06x slower                                    |
| Geometric mean     | (ref)                                                        | 1.02x slower                                            |

Benchmark hidden because not significant (11): pickle_dict, pickle_list, xml_etree_iterparse, unpickle_list, pickle_pure_python, xml_etree_process, tomli_loads, pickle, unpickle_pure_python, xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.6 ms: 1.05x faster                                   |
| Geometric mean         | (ref)                                                        | 1.03x faster                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 68.3 ms: 1.06x faster                                   |
| django_template | 44.3 ms                                                      | 46.9 ms: 1.06x slower                                   |
| Geometric mean  | (ref)                                                        | 1.00x slower                                            |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------:|
| telco                  | 12.2 ms                                                      | 11.4 ms: 1.07x faster                                   |
| comprehensions         | 22.2 us                                                      | 20.9 us: 1.06x faster                                   |
| coroutines             | 30.9 ms                                                      | 29.2 ms: 1.06x faster                                   |
| genshi_xml             | 72.1 ms                                                      | 68.3 ms: 1.06x faster                                   |
| python_startup_no_site | 15.3 ms                                                      | 14.6 ms: 1.05x faster                                   |
| scimark_sor            | 179 ms                                                       | 172 ms: 1.04x faster                                    |
| pprint_safe_repr       | 987 ms                                                       | 959 ms: 1.03x faster                                    |
| pprint_pformat         | 1.94 sec                                                     | 2.00 sec: 1.03x slower                                  |
| deepcopy_reduce        | 4.10 us                                                      | 4.27 us: 1.04x slower                                   |
| async_generators       | 567 ms                                                       | 592 ms: 1.04x slower                                    |
| sqlglot_normalize      | 140 ms                                                       | 146 ms: 1.04x slower                                    |
| meteor_contest         | 150 ms                                                       | 157 ms: 1.05x slower                                    |
| sympy_expand           | 601 ms                                                       | 631 ms: 1.05x slower                                    |
| scimark_lu             | 146 ms                                                       | 154 ms: 1.05x slower                                    |
| chameleon              | 9.34 ms                                                      | 9.84 ms: 1.05x slower                                   |
| json_dumps             | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                   |
| json_loads             | 34.3 us                                                      | 36.1 us: 1.05x slower                                   |
| xml_etree_generate     | 122 ms                                                       | 129 ms: 1.06x slower                                    |
| django_template        | 44.3 ms                                                      | 46.9 ms: 1.06x slower                                   |
| html5lib               | 92.6 ms                                                      | 98.1 ms: 1.06x slower                                   |
| dulwich_log            | 93.7 ms                                                      | 100.0 ms: 1.07x slower                                  |
| aiohttp                | 2.03 ms                                                      | 2.23 ms: 1.10x slower                                   |
| flaskblogging          | 7.68 ms                                                      | 8.78 ms: 1.14x slower                                   |
| gunicorn               | 1.91 ms                                                      | 2.25 ms: 1.18x slower                                   |
| Geometric mean         | (ref)                                                        | 1.01x slower                                            |

Benchmark hidden because not significant (78): typing_runtime_protocols, nqueens, sympy_str, deepcopy, regex_compile, generators, pathlib, sympy_integrate, python_startup, pickle_dict, pidigits, tornado_http, regex_v8, dask, scimark_monte_carlo, float, fannkuch, 2to3, async_tree_io, pickle_list, unpack_sequence, bpe_tokeniser, pyflate, xml_etree_iterparse, crypto_pyaes, async_tree_cpu_io_mixed_tg, unpickle_list, mdp, docutils, logging_silent, pickle_pure_python, pycparser, async_tree_memoization_tg, genshi_text, pylint, richards, json, asyncio_tcp_ssl, scimark_fft, async_tree_none, mako, xml_etree_process, tomli_loads, asyncio_websockets, async_tree_cpu_io_mixed, thrift, chaos, pickle, sympy_sum, spectral_norm, raytrace, unpickle_pure_python, create_gc_cycles, sqlglot_optimize, sqlite_synth, xml_etree_parse, regex_effbot, regex_dna, go, sqlglot_parse, coverage, logging_format, deltablue, hexiom, deepcopy_memo, scimark_sparse_mat_mult, async_tree_none_tg, bench_mp_pool, gc_traversal, async_tree_io_tg, asyncio_tcp, unpickle, richards_super, nbody, sqlglot_transpile, logging_simple, async_tree_memoization, bench_thread_pool

# HPT report

- Reliability score: 56.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x