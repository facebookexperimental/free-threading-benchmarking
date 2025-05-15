# Results vs. 3.13.0rc2

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.171x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 339 ms: 1.31x faster                                                  |
| docutils       | 4.01 sec                                                     | 3.39 sec: 1.18x faster                                                |
| html5lib       | 92.6 ms                                                      | 75.2 ms: 1.23x faster                                                 |
| Geometric mean | (ref)                                                        | 1.24x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 807 ms: 1.72x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 417 ms: 1.70x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 850 ms: 1.65x faster                                                  |
| async_tree_none            | 572 ms                                                       | 351 ms: 1.63x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 421 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 333 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 623 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 625 ms: 1.36x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 649 ms: 1.18x faster                                                  |
| async_generators           | 567 ms                                                       | 506 ms: 1.12x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.43x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 94.3 ms: 1.23x faster                                                 |
| pidigits       | 251 ms                                                       | 223 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.86 ms: 1.23x faster                                                 |
| regex_compile  | 182 ms                                                       | 154 ms: 1.18x faster                                                  |
| regex_dna      | 282 ms                                                       | 246 ms: 1.15x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 29.0 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.17x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 124 ms: 1.42x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 172 ms: 1.34x faster                                                  |
| xml_etree_process    | 85.9 ms                                                      | 74.9 ms: 1.15x faster                                                 |
| xml_etree_generate   | 122 ms                                                       | 109 ms: 1.12x faster                                                  |
| tomli_loads          | 2.78 sec                                                     | 2.49 sec: 1.12x faster                                                |
| pickle_pure_python   | 416 us                                                       | 387 us: 1.08x faster                                                  |
| unpickle_pure_python | 290 us                                                       | 270 us: 1.07x faster                                                  |
| json_dumps           | 14.1 ms                                                      | 13.7 ms: 1.03x faster                                                 |
| json_loads           | 34.3 us                                                      | 37.2 us: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 10.2 ms: 1.50x faster                                                 |
| python_startup         | 22.4 ms                                                      | 17.3 ms: 1.29x faster                                                 |
| Geometric mean         | (ref)                                                        | 1.39x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 25.9 ms: 1.22x faster                                                 |
| genshi_xml      | 72.1 ms                                                      | 60.9 ms: 1.18x faster                                                 |
| django_template | 44.3 ms                                                      | 42.8 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                        | 1.11x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.61 sec: 2.35x faster                                                |
| async_tree_io              | 1.39 sec                                                     | 807 ms: 1.72x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 417 ms: 1.70x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 850 ms: 1.65x faster                                                  |
| async_tree_none            | 572 ms                                                       | 351 ms: 1.63x faster                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 1.77 ms: 1.63x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 421 ms: 1.59x faster                                                  |
| deepcopy                   | 498 us                                                       | 322 us: 1.55x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 333 ms: 1.51x faster                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 10.2 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 623 ms: 1.43x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 124 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 625 ms: 1.36x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 36.8 us: 1.36x faster                                                 |
| go                         | 191 ms                                                       | 141 ms: 1.36x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 172 ms: 1.34x faster                                                  |
| 2to3                       | 445 ms                                                       | 339 ms: 1.31x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 23.3 ms: 1.30x faster                                                 |
| python_startup             | 22.4 ms                                                      | 17.3 ms: 1.29x faster                                                 |
| pylint                     | 470 ms                                                       | 364 ms: 1.29x faster                                                  |
| telco                      | 12.2 ms                                                      | 9.44 ms: 1.29x faster                                                 |
| dulwich_log                | 93.7 ms                                                      | 73.2 ms: 1.28x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 23.4 ms: 1.28x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 75.2 ms: 1.23x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.24 us: 1.23x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 3.86 ms: 1.23x faster                                                 |
| float                      | 116 ms                                                       | 94.3 ms: 1.23x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.34 us: 1.22x faster                                                 |
| richards                   | 65.5 ms                                                      | 53.6 ms: 1.22x faster                                                 |
| genshi_text                | 31.7 ms                                                      | 25.9 ms: 1.22x faster                                                 |
| scimark_sor                | 179 ms                                                       | 146 ms: 1.22x faster                                                  |
| spectral_norm              | 157 ms                                                       | 129 ms: 1.21x faster                                                  |
| richards_super             | 73.2 ms                                                      | 61.6 ms: 1.19x faster                                                 |
| genshi_xml                 | 72.1 ms                                                      | 60.9 ms: 1.18x faster                                                 |
| regex_compile              | 182 ms                                                       | 154 ms: 1.18x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.39 sec: 1.18x faster                                                |
| asyncio_websockets         | 766 ms                                                       | 649 ms: 1.18x faster                                                  |
| sympy_str                  | 379 ms                                                       | 324 ms: 1.17x faster                                                  |
| meteor_contest             | 150 ms                                                       | 128 ms: 1.17x faster                                                  |
| thrift                     | 1.10 ms                                                      | 941 us: 1.17x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.47 sec: 1.15x faster                                                |
| sympy_sum                  | 210 ms                                                       | 183 ms: 1.15x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 74.9 ms: 1.15x faster                                                 |
| regex_dna                  | 282 ms                                                       | 246 ms: 1.15x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 197 us: 1.14x faster                                                  |
| pyflate                    | 664 ms                                                       | 581 ms: 1.14x faster                                                  |
| chaos                      | 83.6 ms                                                      | 73.4 ms: 1.14x faster                                                 |
| nqueens                    | 112 ms                                                       | 98.5 ms: 1.13x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 29.0 ms: 1.13x faster                                                 |
| xml_etree_generate         | 122 ms                                                       | 109 ms: 1.12x faster                                                  |
| pidigits                   | 251 ms                                                       | 223 ms: 1.12x faster                                                  |
| async_generators           | 567 ms                                                       | 506 ms: 1.12x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.49 sec: 1.12x faster                                                |
| pycparser                  | 1.57 sec                                                     | 1.41 sec: 1.12x faster                                                |
| pprint_safe_repr           | 987 ms                                                       | 890 ms: 1.11x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 91.5 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 83.1 ms: 1.09x faster                                                 |
| fannkuch                   | 547 ms                                                       | 502 ms: 1.09x faster                                                  |
| sympy_expand               | 601 ms                                                       | 552 ms: 1.09x faster                                                  |
| pickle_pure_python         | 416 us                                                       | 387 us: 1.08x faster                                                  |
| unpickle_pure_python       | 290 us                                                       | 270 us: 1.07x faster                                                  |
| hexiom                     | 8.11 ms                                                      | 7.55 ms: 1.07x faster                                                 |
| pprint_pformat             | 1.94 sec                                                     | 1.83 sec: 1.06x faster                                                |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.38 ms: 1.06x faster                                                 |
| logging_format             | 9.24 us                                                      | 8.80 us: 1.05x faster                                                 |
| logging_simple             | 8.56 us                                                      | 8.18 us: 1.05x faster                                                 |
| comprehensions             | 22.2 us                                                      | 21.3 us: 1.04x faster                                                 |
| scimark_fft                | 473 ms                                                       | 457 ms: 1.04x faster                                                  |
| django_template            | 44.3 ms                                                      | 42.8 ms: 1.04x faster                                                 |
| json_dumps                 | 14.1 ms                                                      | 13.7 ms: 1.03x faster                                                 |
| raytrace                   | 344 ms                                                       | 336 ms: 1.03x faster                                                  |
| gc_traversal               | 5.70 ms                                                      | 5.91 ms: 1.04x slower                                                 |
| json                       | 6.51 ms                                                      | 6.83 ms: 1.05x slower                                                 |
| json_loads                 | 34.3 us                                                      | 37.2 us: 1.09x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 3.12 ms: 1.29x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 81.3 ms: 4.35x slower                                                 |
| logging_silent             | 130 ns                                                       | 609 ns: 4.69x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.15x faster                                                          |

Benchmark hidden because not significant (7): deltablue, coroutines, mako, generators, coverage, scimark_lu, nbody
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.171x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.16x