# Results vs. 3.13.0rc2

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.075x faster
- HPT reliability: 85.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 378 ms: 1.18x faster                                                  |
| docutils       | 4.01 sec                                                     | 3.61 sec: 1.11x faster                                                |
| html5lib       | 92.6 ms                                                      | 82.8 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 667 ms: 2.10x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 713 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 291 ms: 1.73x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 389 ms: 1.72x faster                                                  |
| async_tree_none            | 572 ms                                                       | 338 ms: 1.69x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 432 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 580 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 628 ms: 1.41x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 671 ms: 1.14x faster                                                  |
| async_generators           | 567 ms                                                       | 536 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.50x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 91.7 ms: 1.26x faster                                                 |
| pidigits       | 251 ms                                                       | 219 ms: 1.15x faster                                                  |
| nbody          | 119 ms                                                       | 159 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.95 ms: 1.20x faster                                                 |
| regex_v8       | 32.8 ms                                                      | 27.3 ms: 1.20x faster                                                 |
| regex_dna      | 282 ms                                                       | 253 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.13x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 117 ms: 1.51x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 173 ms: 1.34x faster                                                  |
| unpickle_pure_python | 290 us                                                       | 300 us: 1.03x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 130 ms: 1.06x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 92.1 ms: 1.07x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                 |
| json_loads           | 34.3 us                                                      | 41.6 us: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (2): tomli_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 13.8 ms: 1.11x faster                                                 |
| Geometric mean         | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 33.3 ms: 1.05x slower                                                 |
| django_template | 44.3 ms                                                      | 49.4 ms: 1.12x slower                                                 |
| mako            | 15.9 ms                                                      | 20.7 ms: 1.30x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.11x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 667 ms: 2.10x faster                                                  |
| gc_traversal               | 5.70 ms                                                      | 2.85 ms: 2.00x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 713 ms: 1.95x faster                                                  |
| mdp                        | 3.80 sec                                                     | 2.07 sec: 1.84x faster                                                |
| async_tree_none_tg         | 504 ms                                                       | 291 ms: 1.73x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 389 ms: 1.72x faster                                                  |
| async_tree_none            | 572 ms                                                       | 338 ms: 1.69x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 432 ms: 1.64x faster                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 1.89 ms: 1.53x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 117 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 580 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 628 ms: 1.41x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 2.95 us: 1.35x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 173 ms: 1.34x faster                                                  |
| deepcopy                   | 498 us                                                       | 375 us: 1.33x faster                                                  |
| float                      | 116 ms                                                       | 91.7 ms: 1.26x faster                                                 |
| dulwich_log                | 93.7 ms                                                      | 77.1 ms: 1.22x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 3.95 ms: 1.20x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 27.3 ms: 1.20x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 25.0 ms: 1.20x faster                                                 |
| go                         | 191 ms                                                       | 161 ms: 1.19x faster                                                  |
| 2to3                       | 445 ms                                                       | 378 ms: 1.18x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.5 ms: 1.16x faster                                                 |
| pylint                     | 470 ms                                                       | 408 ms: 1.15x faster                                                  |
| pidigits                   | 251 ms                                                       | 219 ms: 1.15x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 671 ms: 1.14x faster                                                  |
| scimark_sor                | 179 ms                                                       | 159 ms: 1.12x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 82.8 ms: 1.12x faster                                                 |
| pycparser                  | 1.57 sec                                                     | 1.41 sec: 1.11x faster                                                |
| regex_dna                  | 282 ms                                                       | 253 ms: 1.11x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.61 sec: 1.11x faster                                                |
| python_startup_no_site     | 15.3 ms                                                      | 13.8 ms: 1.11x faster                                                 |
| spectral_norm              | 157 ms                                                       | 142 ms: 1.10x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 45.6 us: 1.10x faster                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 2.20 ms: 1.10x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.83 us: 1.07x faster                                                 |
| sympy_integrate            | 30.2 ms                                                      | 28.5 ms: 1.06x faster                                                 |
| async_generators           | 567 ms                                                       | 536 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 6.16 sec: 1.02x faster                                                |
| scimark_fft                | 473 ms                                                       | 481 ms: 1.02x slower                                                  |
| generators                 | 40.0 ms                                                      | 41.1 ms: 1.03x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.01 sec: 1.03x slower                                                |
| unpickle_pure_python       | 290 us                                                       | 300 us: 1.03x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 219 ms: 1.04x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 33.3 ms: 1.05x slower                                                 |
| meteor_contest             | 150 ms                                                       | 159 ms: 1.06x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 130 ms: 1.06x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 8.67 ms: 1.07x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 92.1 ms: 1.07x slower                                                 |
| sympy_expand               | 601 ms                                                       | 646 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.10 sec: 1.08x slower                                                |
| json_dumps                 | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.41 ms: 1.10x slower                                                 |
| comprehensions             | 22.2 us                                                      | 24.4 us: 1.10x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 100 ms: 1.10x slower                                                  |
| json                       | 6.51 ms                                                      | 7.20 ms: 1.11x slower                                                 |
| crypto_pyaes               | 100 ms                                                       | 111 ms: 1.11x slower                                                  |
| fannkuch                   | 547 ms                                                       | 608 ms: 1.11x slower                                                  |
| django_template            | 44.3 ms                                                      | 49.4 ms: 1.12x slower                                                 |
| raytrace                   | 344 ms                                                       | 386 ms: 1.12x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 166 ms: 1.14x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 257 us: 1.14x slower                                                  |
| logging_format             | 9.24 us                                                      | 10.6 us: 1.14x slower                                                 |
| logging_simple             | 8.56 us                                                      | 10.0 us: 1.17x slower                                                 |
| json_loads                 | 34.3 us                                                      | 41.6 us: 1.22x slower                                                 |
| mako                       | 15.9 ms                                                      | 20.7 ms: 1.30x slower                                                 |
| coverage                   | 107 ms                                                       | 143 ms: 1.33x slower                                                  |
| nbody                      | 119 ms                                                       | 159 ms: 1.34x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 74.7 ms: 4.00x slower                                                 |
| logging_silent             | 130 ns                                                       | 699 ns: 5.37x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (14): chaos, coroutines, regex_compile, richards, thrift, pyflate, tomli_loads, genshi_xml, nqueens, python_startup, deltablue, pickle_pure_python, sympy_str, richards_super
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 85.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.41x