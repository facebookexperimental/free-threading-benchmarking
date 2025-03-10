# Results vs. 3.13.0rc2

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.058x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 553 ms: 1.24x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.18 sec: 1.04x slower                                                 |
| html5lib       | 92.6 ms                                                      | 98.4 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 772 ms: 1.82x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 826 ms: 1.68x faster                                                   |
| async_tree_none            | 572 ms                                                       | 396 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 474 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 356 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 509 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 644 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 712 ms: 1.25x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, coroutines, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 103 ms: 1.13x faster                                                   |
| nbody          | 119 ms                                                       | 181 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| regex_compile  | 182 ms                                                       | 198 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 132 ms: 1.34x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 205 ms: 1.12x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 132 ms: 1.08x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.05 sec: 1.10x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 96.3 ms: 1.12x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 338 us: 1.17x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 500 us: 1.20x slower                                                   |
| json_loads           | 34.3 us                                                      | 42.8 us: 1.25x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 19.4 ms: 1.37x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 23.9 ms: 1.56x slower                                                  |
| python_startup         | 22.4 ms                                                      | 35.5 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.57x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 86.9 ms: 1.21x slower                                                  |
| django_template | 44.3 ms                                                      | 54.7 ms: 1.24x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 39.5 ms: 1.25x slower                                                  |
| mako            | 15.9 ms                                                      | 23.6 ms: 1.48x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 772 ms: 1.82x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 826 ms: 1.68x faster                                                   |
| async_tree_none            | 572 ms                                                       | 396 ms: 1.44x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 4.03 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 474 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 356 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 509 ms: 1.39x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 132 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 644 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 712 ms: 1.25x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.43 us: 1.16x faster                                                  |
| deepcopy                   | 498 us                                                       | 430 us: 1.16x faster                                                   |
| float                      | 116 ms                                                       | 103 ms: 1.13x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 205 ms: 1.12x faster                                                   |
| go                         | 191 ms                                                       | 178 ms: 1.07x faster                                                   |
| scimark_sor                | 179 ms                                                       | 168 ms: 1.06x faster                                                   |
| spectral_norm              | 157 ms                                                       | 150 ms: 1.04x faster                                                   |
| docutils                   | 4.01 sec                                                     | 4.18 sec: 1.04x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.28 us: 1.05x slower                                                  |
| regex_dna                  | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 148 ms: 1.06x slower                                                   |
| html5lib                   | 92.6 ms                                                      | 98.4 ms: 1.06x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 99.6 ms: 1.06x slower                                                  |
| richards                   | 65.5 ms                                                      | 70.4 ms: 1.08x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 132 ms: 1.08x slower                                                   |
| json                       | 6.51 ms                                                      | 7.04 ms: 1.08x slower                                                  |
| regex_compile              | 182 ms                                                       | 198 ms: 1.09x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.20 ms: 1.09x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.05 sec: 1.10x slower                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 83.0 ms: 1.11x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.51 us: 1.11x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 96.3 ms: 1.12x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 34.0 ms: 1.12x slower                                                  |
| logging_format             | 9.24 us                                                      | 10.4 us: 1.13x slower                                                  |
| mdp                        | 3.80 sec                                                     | 4.30 sec: 1.13x slower                                                 |
| generators                 | 40.0 ms                                                      | 45.6 ms: 1.14x slower                                                  |
| logging_silent             | 130 ns                                                       | 148 ns: 1.14x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.13 sec: 1.15x slower                                                 |
| sympy_str                  | 379 ms                                                       | 435 ms: 1.15x slower                                                   |
| chaos                      | 83.6 ms                                                      | 96.8 ms: 1.16x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 338 us: 1.17x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.28 sec: 1.17x slower                                                 |
| sympy_sum                  | 210 ms                                                       | 247 ms: 1.17x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 118 ms: 1.18x slower                                                   |
| pyflate                    | 664 ms                                                       | 780 ms: 1.18x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 267 us: 1.18x slower                                                   |
| scimark_fft                | 473 ms                                                       | 565 ms: 1.19x slower                                                   |
| sympy_expand               | 601 ms                                                       | 717 ms: 1.19x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 5.31 ms: 1.20x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 500 us: 1.20x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.55 sec: 1.20x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 86.9 ms: 1.21x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.68 ms: 1.22x slower                                                  |
| fannkuch                   | 547 ms                                                       | 669 ms: 1.22x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 9.93 ms: 1.22x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 180 ms: 1.23x slower                                                   |
| meteor_contest             | 150 ms                                                       | 185 ms: 1.23x slower                                                   |
| django_template            | 44.3 ms                                                      | 54.7 ms: 1.24x slower                                                  |
| 2to3                       | 445 ms                                                       | 553 ms: 1.24x slower                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 2.18 ms: 1.24x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 39.5 ms: 1.25x slower                                                  |
| json_loads                 | 34.3 us                                                      | 42.8 us: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.54 ms: 1.26x slower                                                  |
| richards_super             | 73.2 ms                                                      | 92.8 ms: 1.27x slower                                                  |
| comprehensions             | 22.2 us                                                      | 28.2 us: 1.27x slower                                                  |
| nqueens                    | 112 ms                                                       | 142 ms: 1.27x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 116 ms: 1.28x slower                                                   |
| raytrace                   | 344 ms                                                       | 446 ms: 1.30x slower                                                   |
| coverage                   | 107 ms                                                       | 147 ms: 1.37x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 19.4 ms: 1.37x slower                                                  |
| mako                       | 15.9 ms                                                      | 23.6 ms: 1.48x slower                                                  |
| nbody                      | 119 ms                                                       | 181 ms: 1.52x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 4.46 ms: 1.54x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 23.9 ms: 1.56x slower                                                  |
| python_startup             | 22.4 ms                                                      | 35.5 ms: 1.58x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 87.1 ms: 4.66x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (12): regex_effbot, pylint, pycparser, deepcopy_memo, asyncio_websockets, coroutines, regex_v8, pidigits, async_generators, pathlib, telco, create_gc_cycles
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.058x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x