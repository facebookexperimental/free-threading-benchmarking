# Results vs. 3.13.0rc2

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.089x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 411 ms: 1.08x faster                                                   |
| docutils       | 4.01 sec                                                     | 3.58 sec: 1.12x faster                                                 |
| html5lib       | 92.6 ms                                                      | 82.5 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 839 ms: 1.65x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 855 ms: 1.64x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 481 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 479 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 366 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 668 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 681 ms: 1.25x faster                                                   |
| async_generators           | 567 ms                                                       | 523 ms: 1.09x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 707 ms: 1.08x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 230 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.20 ms: 1.13x faster                                                  |
| regex_compile  | 182 ms                                                       | 164 ms: 1.11x faster                                                   |
| regex_dna      | 282 ms                                                       | 270 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 138 ms: 1.29x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 199 ms: 1.16x faster                                                   |
| xml_etree_process    | 85.9 ms                                                      | 78.3 ms: 1.10x faster                                                  |
| xml_etree_generate   | 122 ms                                                       | 113 ms: 1.08x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 281 us: 1.03x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.70 sec: 1.03x faster                                                 |
| json_dumps           | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (2): json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                  |
| python_startup         | 22.4 ms                                                      | 24.0 ms: 1.07x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 64.8 ms: 1.11x faster                                                  |
| genshi_text    | 31.7 ms                                                      | 29.1 ms: 1.09x faster                                                  |
| mako           | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 839 ms: 1.65x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 855 ms: 1.64x faster                                                   |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 481 ms: 1.48x faster                                                   |
| deepcopy                   | 498 us                                                       | 344 us: 1.45x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 479 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 366 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 668 ms: 1.33x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 38.2 us: 1.31x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 138 ms: 1.29x faster                                                   |
| go                         | 191 ms                                                       | 151 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 681 ms: 1.25x faster                                                   |
| pylint                     | 470 ms                                                       | 377 ms: 1.25x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.5 ms: 1.16x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 199 ms: 1.16x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 25.8 ms: 1.16x faster                                                  |
| richards                   | 65.5 ms                                                      | 57.7 ms: 1.14x faster                                                  |
| scimark_sor                | 179 ms                                                       | 158 ms: 1.13x faster                                                   |
| fannkuch                   | 547 ms                                                       | 484 ms: 1.13x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.20 ms: 1.13x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.64 us: 1.13x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 82.5 ms: 1.12x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.58 sec: 1.12x faster                                                 |
| thrift                     | 1.10 ms                                                      | 985 us: 1.12x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 64.8 ms: 1.11x faster                                                  |
| regex_compile              | 182 ms                                                       | 164 ms: 1.11x faster                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                  |
| nqueens                    | 112 ms                                                       | 101 ms: 1.10x faster                                                   |
| xml_etree_process          | 85.9 ms                                                      | 78.3 ms: 1.10x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.73 sec: 1.10x faster                                                 |
| sympy_integrate            | 30.2 ms                                                      | 27.6 ms: 1.10x faster                                                  |
| richards_super             | 73.2 ms                                                      | 66.9 ms: 1.09x faster                                                  |
| pidigits                   | 251 ms                                                       | 230 ms: 1.09x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 192 ms: 1.09x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 29.1 ms: 1.09x faster                                                  |
| async_generators           | 567 ms                                                       | 523 ms: 1.09x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 707 ms: 1.08x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.45 sec: 1.08x faster                                                 |
| 2to3                       | 445 ms                                                       | 411 ms: 1.08x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 113 ms: 1.08x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 92.9 ms: 1.08x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.71 us: 1.08x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.54 sec: 1.07x faster                                                 |
| typing_runtime_protocols   | 226 us                                                       | 211 us: 1.07x faster                                                   |
| deltablue                  | 4.44 ms                                                      | 4.17 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.36 ms: 1.06x faster                                                  |
| sympy_str                  | 379 ms                                                       | 359 ms: 1.06x faster                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 1.66 ms: 1.05x faster                                                  |
| logging_format             | 9.24 us                                                      | 8.77 us: 1.05x faster                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 71.0 ms: 1.05x faster                                                  |
| sympy_expand               | 601 ms                                                       | 571 ms: 1.05x faster                                                   |
| comprehensions             | 22.2 us                                                      | 21.2 us: 1.05x faster                                                  |
| regex_dna                  | 282 ms                                                       | 270 ms: 1.04x faster                                                   |
| generators                 | 40.0 ms                                                      | 38.4 ms: 1.04x faster                                                  |
| json                       | 6.51 ms                                                      | 6.28 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 954 ms: 1.03x faster                                                   |
| unpickle_pure_python       | 290 us                                                       | 281 us: 1.03x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.70 sec: 1.03x faster                                                 |
| coverage                   | 107 ms                                                       | 112 ms: 1.04x slower                                                   |
| mako                       | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| python_startup             | 22.4 ms                                                      | 24.0 ms: 1.07x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.38 ms: 1.29x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.43 ms: 1.42x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 85.0 ms: 4.55x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (22): bench_thread_pool, logging_simple, float, json_loads, chaos, spectral_norm, pprint_pformat, regex_v8, scimark_fft, sqlglot_transpile, sqlglot_normalize, dulwich_log, pyflate, raytrace, coroutines, hexiom, meteor_contest, scimark_monte_carlo, django_template, nbody, pickle_pure_python, scimark_lu
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x