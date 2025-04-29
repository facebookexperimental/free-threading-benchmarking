# Results vs. 3.13.0rc2

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: linux-x86_64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.151x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 358 ms: 1.24x faster                                                   |
| docutils       | 4.01 sec                                                     | 3.57 sec: 1.12x faster                                                 |
| html5lib       | 92.6 ms                                                      | 76.3 ms: 1.21x faster                                                  |
| Geometric mean | (ref)                                                        | 1.19x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 829 ms: 1.69x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 820 ms: 1.69x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 424 ms: 1.67x faster                                                   |
| async_tree_none            | 572 ms                                                       | 359 ms: 1.59x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 443 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 341 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 640 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 638 ms: 1.34x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 660 ms: 1.16x faster                                                   |
| async_generators           | 567 ms                                                       | 498 ms: 1.14x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 29.2 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.41x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 93.7 ms: 1.24x faster                                                  |
| pidigits       | 251 ms                                                       | 225 ms: 1.12x faster                                                   |
| Geometric mean | (ref)                                                        | 1.11x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.86 ms: 1.23x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 26.9 ms: 1.22x faster                                                  |
| regex_compile  | 182 ms                                                       | 155 ms: 1.17x faster                                                   |
| regex_dna      | 282 ms                                                       | 253 ms: 1.11x faster                                                   |
| Geometric mean | (ref)                                                        | 1.18x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 191 ms: 1.21x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.45 sec: 1.13x faster                                                 |
| xml_etree_process    | 85.9 ms                                                      | 79.6 ms: 1.08x faster                                                  |
| pickle_pure_python   | 416 us                                                       | 391 us: 1.07x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 274 us: 1.06x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| json_dumps           | 14.1 ms                                                      | 14.5 ms: 1.03x slower                                                  |
| json_loads           | 34.3 us                                                      | 38.0 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 11.6 ms: 1.32x faster                                                  |
| python_startup         | 22.4 ms                                                      | 19.2 ms: 1.17x faster                                                  |
| Geometric mean         | (ref)                                                        | 1.24x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 26.3 ms: 1.20x faster                                                  |
| genshi_xml     | 72.1 ms                                                      | 61.9 ms: 1.16x faster                                                  |
| mako           | 15.9 ms                                                      | 16.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.84 sec: 2.06x faster                                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 829 ms: 1.69x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 820 ms: 1.69x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 424 ms: 1.67x faster                                                   |
| async_tree_none            | 572 ms                                                       | 359 ms: 1.59x faster                                                   |
| deepcopy                   | 498 us                                                       | 324 us: 1.54x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 443 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 341 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 640 ms: 1.39x faster                                                   |
| go                         | 191 ms                                                       | 140 ms: 1.36x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 36.9 us: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 638 ms: 1.34x faster                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 11.6 ms: 1.32x faster                                                  |
| telco                      | 12.2 ms                                                      | 9.25 ms: 1.32x faster                                                  |
| dulwich_log                | 93.7 ms                                                      | 74.1 ms: 1.26x faster                                                  |
| spectral_norm              | 157 ms                                                       | 125 ms: 1.26x faster                                                   |
| 2to3                       | 445 ms                                                       | 358 ms: 1.24x faster                                                   |
| scimark_sor                | 179 ms                                                       | 144 ms: 1.24x faster                                                   |
| float                      | 116 ms                                                       | 93.7 ms: 1.24x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 3.86 ms: 1.23x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 24.7 ms: 1.22x faster                                                  |
| pylint                     | 470 ms                                                       | 386 ms: 1.22x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 26.9 ms: 1.22x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.27 us: 1.22x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 76.3 ms: 1.21x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 191 ms: 1.21x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 26.3 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.41 us: 1.20x faster                                                  |
| richards                   | 65.5 ms                                                      | 54.6 ms: 1.20x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 25.1 ms: 1.19x faster                                                  |
| meteor_contest             | 150 ms                                                       | 127 ms: 1.18x faster                                                   |
| chaos                      | 83.6 ms                                                      | 70.7 ms: 1.18x faster                                                  |
| regex_compile              | 182 ms                                                       | 155 ms: 1.17x faster                                                   |
| python_startup             | 22.4 ms                                                      | 19.2 ms: 1.17x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 61.9 ms: 1.16x faster                                                  |
| richards_super             | 73.2 ms                                                      | 63.0 ms: 1.16x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 660 ms: 1.16x faster                                                   |
| thrift                     | 1.10 ms                                                      | 949 us: 1.16x faster                                                   |
| pyflate                    | 664 ms                                                       | 573 ms: 1.16x faster                                                   |
| sympy_str                  | 379 ms                                                       | 330 ms: 1.15x faster                                                   |
| nqueens                    | 112 ms                                                       | 97.7 ms: 1.14x faster                                                  |
| async_generators           | 567 ms                                                       | 498 ms: 1.14x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.45 sec: 1.13x faster                                                 |
| bench_thread_pool          | 2.89 ms                                                      | 2.55 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.55 sec: 1.13x faster                                                 |
| typing_runtime_protocols   | 226 us                                                       | 200 us: 1.13x faster                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 80.3 ms: 1.13x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.57 sec: 1.12x faster                                                 |
| sympy_sum                  | 210 ms                                                       | 187 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.03 ms: 1.12x faster                                                  |
| logging_simple             | 8.56 us                                                      | 7.64 us: 1.12x faster                                                  |
| pidigits                   | 251 ms                                                       | 225 ms: 1.12x faster                                                   |
| scimark_fft                | 473 ms                                                       | 424 ms: 1.12x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 89.8 ms: 1.12x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 886 ms: 1.11x faster                                                   |
| regex_dna                  | 282 ms                                                       | 253 ms: 1.11x faster                                                   |
| fannkuch                   | 547 ms                                                       | 495 ms: 1.11x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.49 us: 1.09x faster                                                  |
| hexiom                     | 8.11 ms                                                      | 7.49 ms: 1.08x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 79.6 ms: 1.08x faster                                                  |
| sympy_expand               | 601 ms                                                       | 558 ms: 1.08x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.81 sec: 1.07x faster                                                 |
| pickle_pure_python         | 416 us                                                       | 391 us: 1.07x faster                                                   |
| unpickle_pure_python       | 290 us                                                       | 274 us: 1.06x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 29.2 ms: 1.06x faster                                                  |
| comprehensions             | 22.2 us                                                      | 21.1 us: 1.05x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.50 sec: 1.05x faster                                                 |
| raytrace                   | 344 ms                                                       | 330 ms: 1.04x faster                                                   |
| logging_silent             | 130 ns                                                       | 126 ns: 1.03x faster                                                   |
| json_dumps                 | 14.1 ms                                                      | 14.5 ms: 1.03x slower                                                  |
| json                       | 6.51 ms                                                      | 6.81 ms: 1.05x slower                                                  |
| mako                       | 15.9 ms                                                      | 16.8 ms: 1.05x slower                                                  |
| json_loads                 | 34.3 us                                                      | 38.0 us: 1.11x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.85 ms: 1.38x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.53 ms: 1.46x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 75.9 ms: 4.06x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                           |

Benchmark hidden because not significant (6): deltablue, coverage, generators, nbody, scimark_lu, django_template
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.151x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.13x