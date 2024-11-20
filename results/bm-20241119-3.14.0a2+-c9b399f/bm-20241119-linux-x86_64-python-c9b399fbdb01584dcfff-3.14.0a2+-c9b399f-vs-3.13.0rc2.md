# Results vs. 3.13.0rc2

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.00x slower
- HPT reliability: 94.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 410 ms: 1.09x faster                                                   |
| docutils       | 4.01 sec                                                     | 3.66 sec: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp        | 948 ms                                                       | 901 ms: 1.05x faster                                                   |
| asyncio_websockets | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| async_generators   | 567 ms                                                       | 586 ms: 1.03x slower                                                   |
| Geometric mean     | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, coroutines

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 155 ms: 1.14x faster                                                   |
| unpickle            | 20.5 us                                                      | 18.9 us: 1.09x faster                                                  |
| xml_etree_parse     | 231 ms                                                       | 215 ms: 1.08x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.62 sec: 1.06x faster                                                 |
| xml_etree_process   | 85.9 ms                                                      | 82.2 ms: 1.05x faster                                                  |
| pickle_dict         | 47.2 us                                                      | 45.8 us: 1.03x faster                                                  |
| pickle_pure_python  | 416 us                                                       | 436 us: 1.05x slower                                                   |
| unpickle_list       | 6.68 us                                                      | 7.03 us: 1.05x slower                                                  |
| pickle_list         | 6.86 us                                                      | 7.49 us: 1.09x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 15.5 ms: 1.10x slower                                                  |
| json_loads          | 34.3 us                                                      | 38.7 us: 1.13x slower                                                  |
| pickle              | 15.1 us                                                      | 17.5 us: 1.16x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 19.9 ms: 1.13x faster                                                  |
| python_startup_no_site | 15.3 ms                                                      | 14.0 ms: 1.09x faster                                                  |
| Geometric mean         | (ref)                                                        | 1.11x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                  |
| mako            | 15.9 ms                                                      | 16.7 ms: 1.05x slower                                                  |
| django_template | 44.3 ms                                                      | 46.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy               | 498 us                                                       | 352 us: 1.41x faster                                                   |
| deepcopy_memo          | 50.1 us                                                      | 41.4 us: 1.21x faster                                                  |
| telco                  | 12.2 ms                                                      | 10.6 ms: 1.15x faster                                                  |
| xml_etree_iterparse    | 177 ms                                                       | 155 ms: 1.14x faster                                                   |
| unpack_sequence        | 74.3 ns                                                      | 65.7 ns: 1.13x faster                                                  |
| python_startup         | 22.4 ms                                                      | 19.9 ms: 1.13x faster                                                  |
| go                     | 191 ms                                                       | 173 ms: 1.11x faster                                                   |
| genshi_text            | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                  |
| gc_traversal           | 5.70 ms                                                      | 5.16 ms: 1.10x faster                                                  |
| docutils               | 4.01 sec                                                     | 3.66 sec: 1.10x faster                                                 |
| python_startup_no_site | 15.3 ms                                                      | 14.0 ms: 1.09x faster                                                  |
| deepcopy_reduce        | 4.10 us                                                      | 3.76 us: 1.09x faster                                                  |
| pathlib                | 29.9 ms                                                      | 27.5 ms: 1.09x faster                                                  |
| 2to3                   | 445 ms                                                       | 410 ms: 1.09x faster                                                   |
| unpickle               | 20.5 us                                                      | 18.9 us: 1.09x faster                                                  |
| xml_etree_parse        | 231 ms                                                       | 215 ms: 1.08x faster                                                   |
| sympy_str              | 379 ms                                                       | 353 ms: 1.07x faster                                                   |
| mdp                    | 3.80 sec                                                     | 3.55 sec: 1.07x faster                                                 |
| tomli_loads            | 2.78 sec                                                     | 2.62 sec: 1.06x faster                                                 |
| bpe_tokeniser          | 6.28 sec                                                     | 5.93 sec: 1.06x faster                                                 |
| sympy_integrate        | 30.2 ms                                                      | 28.6 ms: 1.06x faster                                                  |
| fannkuch               | 547 ms                                                       | 518 ms: 1.06x faster                                                   |
| pprint_safe_repr       | 987 ms                                                       | 936 ms: 1.05x faster                                                   |
| asyncio_tcp            | 948 ms                                                       | 901 ms: 1.05x faster                                                   |
| spectral_norm          | 157 ms                                                       | 150 ms: 1.05x faster                                                   |
| xml_etree_process      | 85.9 ms                                                      | 82.2 ms: 1.05x faster                                                  |
| asyncio_websockets     | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| sqlglot_normalize      | 140 ms                                                       | 134 ms: 1.04x faster                                                   |
| sqlite_synth           | 3.99 us                                                      | 3.84 us: 1.04x faster                                                  |
| pickle_dict            | 47.2 us                                                      | 45.8 us: 1.03x faster                                                  |
| scimark_fft            | 473 ms                                                       | 485 ms: 1.02x slower                                                   |
| async_generators       | 567 ms                                                       | 586 ms: 1.03x slower                                                   |
| pickle_pure_python     | 416 us                                                       | 436 us: 1.05x slower                                                   |
| mako                   | 15.9 ms                                                      | 16.7 ms: 1.05x slower                                                  |
| logging_format         | 9.24 us                                                      | 9.73 us: 1.05x slower                                                  |
| unpickle_list          | 6.68 us                                                      | 7.03 us: 1.05x slower                                                  |
| django_template        | 44.3 ms                                                      | 46.7 ms: 1.06x slower                                                  |
| coverage               | 107 ms                                                       | 113 ms: 1.06x slower                                                   |
| dulwich_log            | 93.7 ms                                                      | 99.4 ms: 1.06x slower                                                  |
| sqlglot_transpile      | 2.20 ms                                                      | 2.34 ms: 1.06x slower                                                  |
| sympy_expand           | 601 ms                                                       | 641 ms: 1.07x slower                                                   |
| chaos                  | 83.6 ms                                                      | 89.2 ms: 1.07x slower                                                  |
| json                   | 6.51 ms                                                      | 6.96 ms: 1.07x slower                                                  |
| scimark_lu             | 146 ms                                                       | 157 ms: 1.07x slower                                                   |
| regex_v8               | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                  |
| pickle_list            | 6.86 us                                                      | 7.49 us: 1.09x slower                                                  |
| raytrace               | 344 ms                                                       | 376 ms: 1.09x slower                                                   |
| json_dumps             | 14.1 ms                                                      | 15.5 ms: 1.10x slower                                                  |
| hexiom                 | 8.11 ms                                                      | 8.93 ms: 1.10x slower                                                  |
| deltablue              | 4.44 ms                                                      | 4.90 ms: 1.10x slower                                                  |
| json_loads             | 34.3 us                                                      | 38.7 us: 1.13x slower                                                  |
| logging_silent         | 130 ns                                                       | 150 ns: 1.16x slower                                                   |
| pickle                 | 15.1 us                                                      | 17.5 us: 1.16x slower                                                  |
| bench_mp_pool          | 18.7 ms                                                      | 68.3 ms: 3.66x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (34): typing_runtime_protocols, scimark_monte_carlo, xml_etree_generate, create_gc_cycles, html5lib, sympy_sum, crypto_pyaes, scimark_sparse_mat_mult, regex_effbot, regex_dna, pylint, asyncio_tcp_ssl, pidigits, generators, regex_compile, nqueens, scimark_sor, richards, pprint_pformat, genshi_xml, pyflate, thrift, richards_super, comprehensions, sqlglot_optimize, meteor_contest, unpickle_pure_python, sqlglot_parse, coroutines, float, pycparser, bench_thread_pool, logging_simple, nbody
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 94.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x