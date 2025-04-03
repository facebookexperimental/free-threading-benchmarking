# Results vs. 3.13.0rc2

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 474 ms: 1.07x slower                                                  |
| docutils       | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 909 ms: 1.54x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 901 ms: 1.54x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 465 ms: 1.53x faster                                                  |
| async_tree_none            | 572 ms                                                       | 379 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 366 ms: 1.38x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 508 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 682 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 691 ms: 1.23x faster                                                  |
| async_generators           | 567 ms                                                       | 519 ms: 1.09x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 725 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 96.4 ms: 1.20x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.13 ms: 1.15x faster                                                 |
| regex_v8       | 32.8 ms                                                      | 30.2 ms: 1.09x faster                                                 |
| regex_compile  | 182 ms                                                       | 171 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 205 ms: 1.13x faster                                                  |
| xml_etree_iterparse | 177 ms                                                       | 158 ms: 1.12x faster                                                  |
| tomli_loads         | 2.78 sec                                                     | 2.58 sec: 1.08x faster                                                |
| xml_etree_process   | 85.9 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                                 |
| json_loads          | 34.3 us                                                      | 41.1 us: 1.20x slower                                                 |
| Geometric mean      | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_generate, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 17.9 ms: 1.17x slower                                                 |
| python_startup         | 22.4 ms                                                      | 32.6 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 64.4 ms: 1.12x faster                                                 |
| genshi_text     | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                 |
| django_template | 44.3 ms                                                      | 46.1 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.87 sec: 2.03x faster                                                |
| async_tree_io_tg           | 1.40 sec                                                     | 909 ms: 1.54x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 901 ms: 1.54x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 465 ms: 1.53x faster                                                  |
| async_tree_none            | 572 ms                                                       | 379 ms: 1.51x faster                                                  |
| deepcopy                   | 498 us                                                       | 337 us: 1.48x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 366 ms: 1.38x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 37.7 us: 1.33x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 508 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 682 ms: 1.30x faster                                                  |
| go                         | 191 ms                                                       | 151 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 691 ms: 1.23x faster                                                  |
| float                      | 116 ms                                                       | 96.4 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.43 us: 1.20x faster                                                 |
| scimark_sor                | 179 ms                                                       | 151 ms: 1.18x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.4 ms: 1.17x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 4.13 ms: 1.15x faster                                                 |
| pylint                     | 470 ms                                                       | 412 ms: 1.14x faster                                                  |
| spectral_norm              | 157 ms                                                       | 138 ms: 1.13x faster                                                  |
| dulwich_log                | 93.7 ms                                                      | 82.9 ms: 1.13x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 205 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 158 ms: 1.12x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 64.4 ms: 1.12x faster                                                 |
| genshi_text                | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                 |
| richards                   | 65.5 ms                                                      | 59.6 ms: 1.10x faster                                                 |
| pyflate                    | 664 ms                                                       | 606 ms: 1.10x faster                                                  |
| async_generators           | 567 ms                                                       | 519 ms: 1.09x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                |
| regex_v8                   | 32.8 ms                                                      | 30.2 ms: 1.09x faster                                                 |
| typing_runtime_protocols   | 226 us                                                       | 209 us: 1.08x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.58 sec: 1.08x faster                                                |
| sqlite_synth               | 3.99 us                                                      | 3.70 us: 1.08x faster                                                 |
| chaos                      | 83.6 ms                                                      | 77.9 ms: 1.07x faster                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.30 ms: 1.07x faster                                                 |
| crypto_pyaes               | 100 ms                                                       | 93.8 ms: 1.07x faster                                                 |
| scimark_fft                | 473 ms                                                       | 444 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 85.0 ms: 1.07x faster                                                 |
| regex_compile              | 182 ms                                                       | 171 ms: 1.06x faster                                                  |
| logging_simple             | 8.56 us                                                      | 8.09 us: 1.06x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 725 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.96 sec: 1.05x faster                                                |
| sympy_str                  | 379 ms                                                       | 361 ms: 1.05x faster                                                  |
| nqueens                    | 112 ms                                                       | 106 ms: 1.05x faster                                                  |
| comprehensions             | 22.2 us                                                      | 21.3 us: 1.05x faster                                                 |
| xml_etree_process          | 85.9 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| raytrace                   | 344 ms                                                       | 334 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.00 sec: 1.03x slower                                                |
| coverage                   | 107 ms                                                       | 111 ms: 1.03x slower                                                  |
| django_template            | 44.3 ms                                                      | 46.1 ms: 1.04x slower                                                 |
| generators                 | 40.0 ms                                                      | 42.5 ms: 1.06x slower                                                 |
| 2to3                       | 445 ms                                                       | 474 ms: 1.07x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 157 ms: 1.07x slower                                                  |
| json                       | 6.51 ms                                                      | 6.97 ms: 1.07x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 17.9 ms: 1.17x slower                                                 |
| json_loads                 | 34.3 us                                                      | 41.1 us: 1.20x slower                                                 |
| bench_thread_pool          | 2.89 ms                                                      | 3.62 ms: 1.25x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 8.14 ms: 1.43x slower                                                 |
| python_startup             | 22.4 ms                                                      | 32.6 ms: 1.46x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 3.69 ms: 1.53x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 95.9 ms: 5.13x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (21): sympy_integrate, meteor_contest, pathlib, richards_super, fannkuch, sympy_sum, mako, nbody, pprint_safe_repr, pidigits, logging_silent, coroutines, regex_dna, xml_etree_generate, unpickle_pure_python, pycparser, sympy_expand, logging_format, hexiom, pickle_pure_python, deltablue
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250402-3.14.0a6+-ccaa69a/bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x