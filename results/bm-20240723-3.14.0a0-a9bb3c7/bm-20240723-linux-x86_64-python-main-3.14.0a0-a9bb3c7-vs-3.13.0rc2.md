# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 410 ms: 1.09x faster                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                          |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 670 ms                                                       | 584 ms: 1.15x faster                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 1.24 sec: 1.13x faster                                |
| async_tree_none_tg         | 504 ms                                                       | 464 ms: 1.08x faster                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 821 ms: 1.08x faster                                  |
| async_tree_io              | 1.39 sec                                                     | 1.28 sec: 1.08x faster                                |
| async_tree_none            | 572 ms                                                       | 531 ms: 1.08x faster                                  |
| async_tree_memoization     | 709 ms                                                       | 671 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 818 ms: 1.04x faster                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.83 sec: 1.02x slower                                |
| Geometric mean             | (ref)                                                        | 1.05x faster                                          |

Benchmark hidden because not significant (4): coroutines, asyncio_websockets, async_generators, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 251 ms                                                       | 240 ms: 1.05x faster                                  |
| nbody          | 119 ms                                                       | 114 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_compile, regex_v8, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|---------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 161 ms: 1.10x faster                                  |
| pickle_list         | 6.86 us                                                      | 6.29 us: 1.09x faster                                 |
| xml_etree_parse     | 231 ms                                                       | 216 ms: 1.07x faster                                  |
| xml_etree_generate  | 122 ms                                                       | 116 ms: 1.05x faster                                  |
| pickle_dict         | 47.2 us                                                      | 45.4 us: 1.04x faster                                 |
| tomli_loads         | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                |
| pickle              | 15.1 us                                                      | 15.8 us: 1.05x slower                                 |
| json_dumps          | 14.1 ms                                                      | 14.8 ms: 1.05x slower                                 |
| json_loads          | 34.3 us                                                      | 37.9 us: 1.11x slower                                 |
| Geometric mean      | (ref)                                                        | 1.01x faster                                          |

Benchmark hidden because not significant (5): xml_etree_process, unpickle, pickle_pure_python, unpickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 21.4 ms: 1.05x faster                                 |
| python_startup_no_site | 15.3 ms                                                      | 14.8 ms: 1.03x faster                                 |
| Geometric mean         | (ref)                                                        | 1.04x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| mako           | 15.9 ms                                                      | 16.5 ms: 1.04x slower                                 |
| Geometric mean | (ref)                                                        | 1.00x slower                                          |

Benchmark hidden because not significant (3): genshi_xml, genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy                   | 498 us                                                       | 361 us: 1.38x faster                                  |
| deepcopy_memo              | 50.1 us                                                      | 38.7 us: 1.29x faster                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 584 ms: 1.15x faster                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 1.24 sec: 1.13x faster                                |
| deepcopy_reduce            | 4.10 us                                                      | 3.71 us: 1.10x faster                                 |
| xml_etree_iterparse        | 177 ms                                                       | 161 ms: 1.10x faster                                  |
| telco                      | 12.2 ms                                                      | 11.1 ms: 1.09x faster                                 |
| pickle_list                | 6.86 us                                                      | 6.29 us: 1.09x faster                                 |
| 2to3                       | 445 ms                                                       | 410 ms: 1.09x faster                                  |
| async_tree_none_tg         | 504 ms                                                       | 464 ms: 1.08x faster                                  |
| richards                   | 65.5 ms                                                      | 60.4 ms: 1.08x faster                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 821 ms: 1.08x faster                                  |
| async_tree_io              | 1.39 sec                                                     | 1.28 sec: 1.08x faster                                |
| async_tree_none            | 572 ms                                                       | 531 ms: 1.08x faster                                  |
| typing_runtime_protocols   | 226 us                                                       | 210 us: 1.08x faster                                  |
| sqlite_synth               | 3.99 us                                                      | 3.71 us: 1.08x faster                                 |
| thrift                     | 1.10 ms                                                      | 1.03 ms: 1.07x faster                                 |
| xml_etree_parse            | 231 ms                                                       | 216 ms: 1.07x faster                                  |
| richards_super             | 73.2 ms                                                      | 68.7 ms: 1.07x faster                                 |
| create_gc_cycles           | 2.41 ms                                                      | 2.27 ms: 1.06x faster                                 |
| async_tree_memoization     | 709 ms                                                       | 671 ms: 1.06x faster                                  |
| xml_etree_generate         | 122 ms                                                       | 116 ms: 1.05x faster                                  |
| sympy_str                  | 379 ms                                                       | 360 ms: 1.05x faster                                  |
| mdp                        | 3.80 sec                                                     | 3.61 sec: 1.05x faster                                |
| pathlib                    | 29.9 ms                                                      | 28.6 ms: 1.05x faster                                 |
| python_startup             | 22.4 ms                                                      | 21.4 ms: 1.05x faster                                 |
| pidigits                   | 251 ms                                                       | 240 ms: 1.05x faster                                  |
| comprehensions             | 22.2 us                                                      | 21.3 us: 1.05x faster                                 |
| generators                 | 40.0 ms                                                      | 38.3 ms: 1.04x faster                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 818 ms: 1.04x faster                                  |
| nbody                      | 119 ms                                                       | 114 ms: 1.04x faster                                  |
| pickle_dict                | 47.2 us                                                      | 45.4 us: 1.04x faster                                 |
| tomli_loads                | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                |
| pprint_safe_repr           | 987 ms                                                       | 952 ms: 1.04x faster                                  |
| python_startup_no_site     | 15.3 ms                                                      | 14.8 ms: 1.03x faster                                 |
| scimark_sor                | 179 ms                                                       | 173 ms: 1.03x faster                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.83 sec: 1.02x slower                                |
| mako                       | 15.9 ms                                                      | 16.5 ms: 1.04x slower                                 |
| pickle                     | 15.1 us                                                      | 15.8 us: 1.05x slower                                 |
| json_dumps                 | 14.1 ms                                                      | 14.8 ms: 1.05x slower                                 |
| scimark_lu                 | 146 ms                                                       | 154 ms: 1.05x slower                                  |
| unpack_sequence            | 74.3 ns                                                      | 78.4 ns: 1.06x slower                                 |
| sqlglot_normalize          | 140 ms                                                       | 150 ms: 1.07x slower                                  |
| bench_mp_pool              | 18.7 ms                                                      | 20.3 ms: 1.08x slower                                 |
| json_loads                 | 34.3 us                                                      | 37.9 us: 1.11x slower                                 |
| coverage                   | 107 ms                                                       | 126 ms: 1.17x slower                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.42 ms: 1.18x slower                                 |
| json                       | 6.51 ms                                                      | 7.74 ms: 1.19x slower                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                          |

Benchmark hidden because not significant (50): html5lib, nqueens, sympy_integrate, genshi_xml, sqlglot_transpile, logging_silent, logging_simple, deltablue, coroutines, meteor_contest, scimark_monte_carlo, chaos, xml_etree_process, unpickle, sqlglot_optimize, docutils, sqlglot_parse, bpe_tokeniser, fannkuch, tornado_http, scimark_sparse_mat_mult, raytrace, asyncio_websockets, dask, genshi_text, pprint_pformat, gc_traversal, float, go, regex_compile, pycparser, regex_v8, async_generators, pickle_pure_python, sympy_expand, pyflate, asyncio_tcp, scimark_fft, pylint, logging_format, crypto_pyaes, unpickle_pure_python, regex_dna, sympy_sum, unpickle_list, dulwich_log, hexiom, regex_effbot, django_template, spectral_norm
Ignored benchmarks (4) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x