# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.070x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 526 ms: 1.18x slower                                                  |
| docutils       | 4.01 sec                                                     | 4.13 sec: 1.03x slower                                                |
| html5lib       | 92.6 ms                                                      | 104 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 742 ms: 1.89x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 837 ms: 1.66x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 321 ms: 1.57x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 447 ms: 1.50x faster                                                  |
| async_tree_none            | 572 ms                                                       | 393 ms: 1.46x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 514 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 635 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 724 ms: 1.23x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 736 ms: 1.04x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 32.4 ms: 1.05x slower                                                 |
| async_generators           | 567 ms                                                       | 624 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 233 ms: 1.08x faster                                                  |
| float          | 116 ms                                                       | 111 ms: 1.05x faster                                                  |
| nbody          | 119 ms                                                       | 177 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.36 ms: 1.09x faster                                                 |
| regex_v8       | 32.8 ms                                                      | 33.9 ms: 1.03x slower                                                 |
| regex_compile  | 182 ms                                                       | 198 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 131 ms: 1.35x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 198 ms: 1.16x faster                                                  |
| xml_etree_process    | 85.9 ms                                                      | 92.1 ms: 1.07x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 132 ms: 1.08x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 3.04 sec: 1.09x slower                                                |
| pickle_pure_python   | 416 us                                                       | 482 us: 1.16x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 340 us: 1.17x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 17.4 ms: 1.23x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.6 ms: 1.28x slower                                                 |
| python_startup         | 22.4 ms                                                      | 31.8 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 77.4 ms: 1.07x slower                                                 |
| genshi_text     | 31.7 ms                                                      | 36.6 ms: 1.16x slower                                                 |
| django_template | 44.3 ms                                                      | 51.9 ms: 1.17x slower                                                 |
| mako            | 15.9 ms                                                      | 24.5 ms: 1.53x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 742 ms: 1.89x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 837 ms: 1.66x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 321 ms: 1.57x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 447 ms: 1.50x faster                                                  |
| async_tree_none            | 572 ms                                                       | 393 ms: 1.46x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 514 ms: 1.38x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 131 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 635 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 724 ms: 1.23x faster                                                  |
| deepcopy                   | 498 us                                                       | 422 us: 1.18x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 198 ms: 1.16x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.61 us: 1.11x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 4.36 ms: 1.09x faster                                                 |
| pidigits                   | 251 ms                                                       | 233 ms: 1.08x faster                                                  |
| go                         | 191 ms                                                       | 178 ms: 1.08x faster                                                  |
| telco                      | 12.2 ms                                                      | 11.5 ms: 1.06x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 28.6 ms: 1.05x faster                                                 |
| float                      | 116 ms                                                       | 111 ms: 1.05x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 736 ms: 1.04x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 48.5 us: 1.03x faster                                                 |
| docutils                   | 4.01 sec                                                     | 4.13 sec: 1.03x slower                                                |
| regex_v8                   | 32.8 ms                                                      | 33.9 ms: 1.03x slower                                                 |
| spectral_norm              | 157 ms                                                       | 163 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 4.28 us: 1.05x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 32.4 ms: 1.05x slower                                                 |
| generators                 | 40.0 ms                                                      | 42.4 ms: 1.06x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 92.1 ms: 1.07x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 77.4 ms: 1.07x slower                                                 |
| xml_etree_generate         | 122 ms                                                       | 132 ms: 1.08x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 101 ms: 1.08x slower                                                  |
| regex_compile              | 182 ms                                                       | 198 ms: 1.09x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.04 sec: 1.09x slower                                                |
| pyflate                    | 664 ms                                                       | 726 ms: 1.09x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 153 ms: 1.10x slower                                                  |
| scimark_sor                | 179 ms                                                       | 196 ms: 1.10x slower                                                  |
| scimark_fft                | 473 ms                                                       | 520 ms: 1.10x slower                                                  |
| async_generators           | 567 ms                                                       | 624 ms: 1.10x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.47 us: 1.11x slower                                                 |
| meteor_contest             | 150 ms                                                       | 166 ms: 1.11x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 83.2 ms: 1.11x slower                                                 |
| nqueens                    | 112 ms                                                       | 125 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.10 sec: 1.12x slower                                                |
| logging_silent             | 130 ns                                                       | 146 ns: 1.12x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 104 ms: 1.12x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.1 us: 1.13x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 7.11 sec: 1.13x slower                                                |
| thrift                     | 1.10 ms                                                      | 1.25 ms: 1.14x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 6.53 ms: 1.15x slower                                                 |
| richards                   | 65.5 ms                                                      | 75.5 ms: 1.15x slower                                                 |
| mdp                        | 3.80 sec                                                     | 4.39 sec: 1.15x slower                                                |
| richards_super             | 73.2 ms                                                      | 84.6 ms: 1.16x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 36.6 ms: 1.16x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 482 us: 1.16x slower                                                  |
| logging_format             | 9.24 us                                                      | 10.7 us: 1.16x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 263 us: 1.17x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 340 us: 1.17x slower                                                  |
| django_template            | 44.3 ms                                                      | 51.9 ms: 1.17x slower                                                 |
| 2to3                       | 445 ms                                                       | 526 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.30 sec: 1.18x slower                                                |
| hexiom                     | 8.11 ms                                                      | 9.62 ms: 1.19x slower                                                 |
| fannkuch                   | 547 ms                                                       | 663 ms: 1.21x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.50 ms: 1.21x slower                                                 |
| sqlglot_parse              | 1.76 ms                                                      | 2.15 ms: 1.23x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 17.4 ms: 1.23x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 37.4 ms: 1.24x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 112 ms: 1.24x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 124 ms: 1.24x slower                                                  |
| chaos                      | 83.6 ms                                                      | 104 ms: 1.24x slower                                                  |
| coverage                   | 107 ms                                                       | 136 ms: 1.27x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.78 ms: 1.27x slower                                                 |
| raytrace                   | 344 ms                                                       | 437 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.58 ms: 1.27x slower                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 19.6 ms: 1.28x slower                                                 |
| deltablue                  | 4.44 ms                                                      | 5.91 ms: 1.33x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 201 ms: 1.37x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.42 ms: 1.42x slower                                                 |
| python_startup             | 22.4 ms                                                      | 31.8 ms: 1.42x slower                                                 |
| sympy_str                  | 379 ms                                                       | 548 ms: 1.45x slower                                                  |
| nbody                      | 119 ms                                                       | 177 ms: 1.49x slower                                                  |
| mako                       | 15.9 ms                                                      | 24.5 ms: 1.53x slower                                                 |
| sympy_expand               | 601 ms                                                       | 1.10 sec: 1.83x slower                                                |
| sympy_sum                  | 210 ms                                                       | 392 ms: 1.86x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 88.4 ms: 4.73x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                          |

Benchmark hidden because not significant (5): pycparser, json_loads, regex_dna, pylint, json
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241215-3.14.0a2+-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.070x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x