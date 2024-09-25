# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.02x faster
- HPT reliability: 99.31%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| tornado_http   | 251 ms                                                       | 268 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                         |

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none           | 572 ms                                                       | 512 ms: 1.12x faster                                                 |
| async_tree_none_tg        | 504 ms                                                       | 456 ms: 1.10x faster                                                 |
| async_tree_memoization    | 709 ms                                                       | 643 ms: 1.10x faster                                                 |
| async_tree_memoization_tg | 670 ms                                                       | 609 ms: 1.10x faster                                                 |
| async_tree_io_tg          | 1.40 sec                                                     | 1.29 sec: 1.09x faster                                               |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 819 ms: 1.08x faster                                                 |
| async_tree_io             | 1.39 sec                                                     | 1.30 sec: 1.07x faster                                               |
| async_generators          | 567 ms                                                       | 588 ms: 1.04x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.05x faster                                                         |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 111 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                         |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                |
| regex_effbot   | 4.74 ms                                                      | 4.96 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                        | 1.02x slower                                                         |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_process    | 85.9 ms                                                      | 76.7 ms: 1.12x faster                                                |
| xml_etree_iterparse  | 177 ms                                                       | 165 ms: 1.07x faster                                                 |
| pickle_dict          | 47.2 us                                                      | 45.2 us: 1.04x faster                                                |
| unpickle_pure_python | 290 us                                                       | 282 us: 1.03x faster                                                 |
| json_loads           | 34.3 us                                                      | 36.7 us: 1.07x slower                                                |
| unpickle_list        | 6.68 us                                                      | 7.43 us: 1.11x slower                                                |
| json_dumps           | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                                |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                         |

Benchmark hidden because not significant (7): xml_etree_parse, xml_etree_generate, tomli_loads, unpickle, pickle_pure_python, pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 21.6 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.03x faster                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 68.1 ms: 1.06x faster                                                |
| Geometric mean | (ref)                                                        | 1.00x faster                                                         |

Benchmark hidden because not significant (3): mako, django_template, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|---------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy                  | 498 us                                                       | 346 us: 1.44x faster                                                 |
| deepcopy_memo             | 50.1 us                                                      | 40.8 us: 1.23x faster                                                |
| deepcopy_reduce           | 4.10 us                                                      | 3.50 us: 1.17x faster                                                |
| telco                     | 12.2 ms                                                      | 10.8 ms: 1.13x faster                                                |
| create_gc_cycles          | 2.41 ms                                                      | 2.14 ms: 1.13x faster                                                |
| xml_etree_process         | 85.9 ms                                                      | 76.7 ms: 1.12x faster                                                |
| async_tree_none           | 572 ms                                                       | 512 ms: 1.12x faster                                                 |
| async_tree_none_tg        | 504 ms                                                       | 456 ms: 1.10x faster                                                 |
| async_tree_memoization    | 709 ms                                                       | 643 ms: 1.10x faster                                                 |
| async_tree_memoization_tg | 670 ms                                                       | 609 ms: 1.10x faster                                                 |
| scimark_sor               | 179 ms                                                       | 163 ms: 1.09x faster                                                 |
| richards                  | 65.5 ms                                                      | 60.2 ms: 1.09x faster                                                |
| async_tree_io_tg          | 1.40 sec                                                     | 1.29 sec: 1.09x faster                                               |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 819 ms: 1.08x faster                                                 |
| xml_etree_iterparse       | 177 ms                                                       | 165 ms: 1.07x faster                                                 |
| nbody                     | 119 ms                                                       | 111 ms: 1.07x faster                                                 |
| async_tree_io             | 1.39 sec                                                     | 1.30 sec: 1.07x faster                                               |
| meteor_contest            | 150 ms                                                       | 140 ms: 1.07x faster                                                 |
| sqlglot_optimize          | 74.7 ms                                                      | 70.4 ms: 1.06x faster                                                |
| genshi_xml                | 72.1 ms                                                      | 68.1 ms: 1.06x faster                                                |
| sqlite_synth              | 3.99 us                                                      | 3.80 us: 1.05x faster                                                |
| mdp                       | 3.80 sec                                                     | 3.62 sec: 1.05x faster                                               |
| pickle_dict               | 47.2 us                                                      | 45.2 us: 1.04x faster                                                |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 6.49 ms: 1.04x faster                                                |
| raytrace                  | 344 ms                                                       | 331 ms: 1.04x faster                                                 |
| fannkuch                  | 547 ms                                                       | 528 ms: 1.04x faster                                                 |
| python_startup            | 22.4 ms                                                      | 21.6 ms: 1.03x faster                                                |
| scimark_lu                | 146 ms                                                       | 142 ms: 1.03x faster                                                 |
| unpickle_pure_python      | 290 us                                                       | 282 us: 1.03x faster                                                 |
| coverage                  | 107 ms                                                       | 111 ms: 1.03x slower                                                 |
| async_generators          | 567 ms                                                       | 588 ms: 1.04x slower                                                 |
| regex_v8                  | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                |
| regex_effbot              | 4.74 ms                                                      | 4.96 ms: 1.05x slower                                                |
| sympy_sum                 | 210 ms                                                       | 221 ms: 1.05x slower                                                 |
| tornado_http              | 251 ms                                                       | 268 ms: 1.07x slower                                                 |
| json_loads                | 34.3 us                                                      | 36.7 us: 1.07x slower                                                |
| json                      | 6.51 ms                                                      | 7.01 ms: 1.08x slower                                                |
| crypto_pyaes              | 100 ms                                                       | 108 ms: 1.08x slower                                                 |
| unpickle_list             | 6.68 us                                                      | 7.43 us: 1.11x slower                                                |
| json_dumps                | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                                |
| bench_thread_pool         | 2.89 ms                                                      | 3.31 ms: 1.15x slower                                                |
| bench_mp_pool             | 18.7 ms                                                      | 22.7 ms: 1.21x slower                                                |
| Geometric mean            | (ref)                                                        | 1.02x faster                                                         |

Benchmark hidden because not significant (54): gc_traversal, xml_etree_parse, pathlib, typing_runtime_protocols, sympy_str, async_tree_cpu_io_mixed_tg, nqueens, python_startup_no_site, spectral_norm, comprehensions, asyncio_tcp, pidigits, regex_compile, xml_etree_generate, logging_simple, pprint_safe_repr, richards_super, html5lib, tomli_loads, docutils, sqlglot_parse, scimark_monte_carlo, logging_silent, 2to3, asyncio_websockets, unpickle, pprint_pformat, sympy_integrate, chaos, pylint, bpe_tokeniser, generators, regex_dna, pickle_pure_python, pycparser, asyncio_tcp_ssl, coroutines, mako, pyflate, float, scimark_fft, sqlglot_transpile, pickle_list, django_template, genshi_text, pickle, go, thrift, logging_format, unpack_sequence, deltablue, sympy_expand, sqlglot_normalize, hexiom
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 99.31% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x