# Results vs. 3.13.0rc2

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.065x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.67 sec: 1.09x faster                                                 |
| html5lib       | 92.6 ms                                                      | 84.6 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 859 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 904 ms: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 472 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 389 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 462 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 366 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 644 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 677 ms: 1.31x faster                                                   |
| async_generators           | 567 ms                                                       | 505 ms: 1.12x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 719 ms: 1.07x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 97.8 ms: 1.18x faster                                                  |
| nbody          | 119 ms                                                       | 130 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 170 ms: 1.07x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.53 ms: 1.05x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.60 sec: 1.07x faster                                                 |
| pickle_pure_python  | 416 us                                                       | 460 us: 1.10x slower                                                   |
| json_dumps          | 14.1 ms                                                      | 16.3 ms: 1.16x slower                                                  |
| json_loads          | 34.3 us                                                      | 39.8 us: 1.16x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_generate, xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.0 ms: 1.24x slower                                                  |
| python_startup         | 22.4 ms                                                      | 29.0 ms: 1.29x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 66.9 ms: 1.08x faster                                                  |
| genshi_text    | 31.7 ms                                                      | 29.9 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 859 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 904 ms: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 472 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 389 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 462 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 366 ms: 1.38x faster                                                   |
| deepcopy                   | 498 us                                                       | 372 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 644 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 677 ms: 1.31x faster                                                   |
| spectral_norm              | 157 ms                                                       | 121 ms: 1.29x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 38.9 us: 1.29x faster                                                  |
| go                         | 191 ms                                                       | 150 ms: 1.27x faster                                                   |
| pylint                     | 470 ms                                                       | 388 ms: 1.21x faster                                                   |
| float                      | 116 ms                                                       | 97.8 ms: 1.18x faster                                                  |
| richards                   | 65.5 ms                                                      | 55.8 ms: 1.17x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 151 ms: 1.17x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.44 us: 1.16x faster                                                  |
| scimark_sor                | 179 ms                                                       | 155 ms: 1.15x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.58 us: 1.14x faster                                                  |
| chaos                      | 83.6 ms                                                      | 73.8 ms: 1.13x faster                                                  |
| async_generators           | 567 ms                                                       | 505 ms: 1.12x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.28 us: 1.12x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 202 us: 1.11x faster                                                   |
| logging_simple             | 8.56 us                                                      | 7.71 us: 1.11x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.69 sec: 1.10x faster                                                 |
| meteor_contest             | 150 ms                                                       | 136 ms: 1.10x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 901 ms: 1.10x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 84.6 ms: 1.09x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.67 sec: 1.09x faster                                                 |
| pyflate                    | 664 ms                                                       | 612 ms: 1.08x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.51 sec: 1.08x faster                                                 |
| telco                      | 12.2 ms                                                      | 11.3 ms: 1.08x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 66.9 ms: 1.08x faster                                                  |
| regex_compile              | 182 ms                                                       | 170 ms: 1.07x faster                                                   |
| sympy_str                  | 379 ms                                                       | 353 ms: 1.07x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.60 sec: 1.07x faster                                                 |
| scimark_fft                | 473 ms                                                       | 442 ms: 1.07x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 719 ms: 1.07x faster                                                   |
| deltablue                  | 4.44 ms                                                      | 4.17 ms: 1.07x faster                                                  |
| dulwich_log                | 93.7 ms                                                      | 88.3 ms: 1.06x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 94.6 ms: 1.06x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 29.9 ms: 1.06x faster                                                  |
| thrift                     | 1.10 ms                                                      | 1.04 ms: 1.06x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.53 ms: 1.05x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 34.2 ms: 1.04x slower                                                  |
| sympy_expand               | 601 ms                                                       | 631 ms: 1.05x slower                                                   |
| pycparser                  | 1.57 sec                                                     | 1.68 sec: 1.07x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 157 ms: 1.07x slower                                                   |
| coverage                   | 107 ms                                                       | 116 ms: 1.08x slower                                                   |
| nbody                      | 119 ms                                                       | 130 ms: 1.10x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 460 us: 1.10x slower                                                   |
| json                       | 6.51 ms                                                      | 7.51 ms: 1.15x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.3 ms: 1.16x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.34 ms: 1.16x slower                                                  |
| json_loads                 | 34.3 us                                                      | 39.8 us: 1.16x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 19.0 ms: 1.24x slower                                                  |
| python_startup             | 22.4 ms                                                      | 29.0 ms: 1.29x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.12 ms: 1.42x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.64 ms: 1.51x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 93.1 ms: 4.98x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (28): sqlglot_transpile, sqlglot_optimize, scimark_monte_carlo, sympy_integrate, xml_etree_parse, nqueens, generators, pprint_pformat, comprehensions, xml_etree_generate, richards_super, 2to3, scimark_sparse_mat_mult, hexiom, logging_silent, sqlglot_parse, fannkuch, xml_etree_process, mako, pidigits, coroutines, raytrace, regex_dna, unpickle_pure_python, sympy_sum, sqlglot_normalize, pathlib, django_template
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x