# Results vs. 3.12.6

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.110x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.67 sec: 1.09x faster                                                 |
| html5lib       | 88.9 ms                                                | 84.6 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 859 ms: 2.15x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 904 ms: 2.14x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 472 ms: 2.07x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 462 ms: 2.01x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 366 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 389 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 644 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 677 ms: 1.59x faster                                                   |
| async_generators           | 589 ms                                                 | 505 ms: 1.17x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 719 ms: 1.04x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.2 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.63x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 97.8 ms: 1.26x faster                                                  |
| nbody          | 119 ms                                                 | 130 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.53 ms: 1.13x faster                                                  |
| regex_compile  | 187 ms                                                 | 170 ms: 1.10x faster                                                   |
| regex_dna      | 278 ms                                                 | 288 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.60 sec: 1.11x faster                                                 |
| xml_etree_parse     | 241 ms                                                 | 224 ms: 1.07x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 120 ms: 1.06x faster                                                   |
| json_loads          | 37.9 us                                                | 39.8 us: 1.05x slower                                                  |
| pickle_pure_python  | 436 us                                                 | 460 us: 1.06x slower                                                   |
| json_dumps          | 14.3 ms                                                | 16.3 ms: 1.14x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.0 ms: 1.08x slower                                                  |
| python_startup         | 23.7 ms                                                | 29.0 ms: 1.22x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_xml, genshi_text, mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 859 ms: 2.15x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 904 ms: 2.14x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 472 ms: 2.07x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 462 ms: 2.01x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 366 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 389 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 644 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 677 ms: 1.59x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 38.9 us: 1.35x faster                                                  |
| spectral_norm              | 156 ms                                                 | 121 ms: 1.28x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 170 ms: 1.28x faster                                                   |
| float                      | 123 ms                                                 | 97.8 ms: 1.26x faster                                                  |
| deepcopy                   | 468 us                                                 | 372 us: 1.26x faster                                                   |
| comprehensions             | 27.1 us                                                | 21.7 us: 1.25x faster                                                  |
| logging_simple             | 9.45 us                                                | 7.71 us: 1.22x faster                                                  |
| pylint                     | 465 ms                                                 | 388 ms: 1.20x faster                                                   |
| pyflate                    | 727 ms                                                 | 612 ms: 1.19x faster                                                   |
| async_generators           | 589 ms                                                 | 505 ms: 1.17x faster                                                   |
| raytrace                   | 408 ms                                                 | 350 ms: 1.17x faster                                                   |
| logging_format             | 9.59 us                                                | 8.28 us: 1.16x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.69 sec: 1.16x faster                                                 |
| chaos                      | 84.9 ms                                                | 73.8 ms: 1.15x faster                                                  |
| go                         | 172 ms                                                 | 150 ms: 1.15x faster                                                   |
| dulwich_log                | 100 ms                                                 | 88.3 ms: 1.14x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 94.6 ms: 1.13x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.53 ms: 1.13x faster                                                  |
| scimark_fft                | 500 ms                                                 | 442 ms: 1.13x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.51 sec: 1.13x faster                                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.58 us: 1.13x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.44 us: 1.13x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.60 sec: 1.11x faster                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.10 ms: 1.11x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 202 us: 1.11x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 87.4 ms: 1.10x faster                                                  |
| regex_compile              | 187 ms                                                 | 170 ms: 1.10x faster                                                   |
| sympy_str                  | 385 ms                                                 | 353 ms: 1.09x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.67 sec: 1.09x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 144 ms: 1.09x faster                                                   |
| richards                   | 60.3 ms                                                | 55.8 ms: 1.08x faster                                                  |
| logging_silent             | 139 ns                                                 | 129 ns: 1.08x faster                                                   |
| scimark_sor                | 167 ms                                                 | 155 ms: 1.08x faster                                                   |
| meteor_contest             | 146 ms                                                 | 136 ms: 1.08x faster                                                   |
| nqueens                    | 117 ms                                                 | 109 ms: 1.07x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 224 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 901 ms: 1.07x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.68 sec: 1.07x faster                                                 |
| xml_etree_generate         | 127 ms                                                 | 120 ms: 1.06x faster                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 71.8 ms: 1.06x faster                                                  |
| generators                 | 41.1 ms                                                | 39.0 ms: 1.06x faster                                                  |
| html5lib                   | 88.9 ms                                                | 84.6 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.90 sec: 1.04x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 719 ms: 1.04x faster                                                   |
| regex_dna                  | 278 ms                                                 | 288 ms: 1.04x slower                                                   |
| json_loads                 | 37.9 us                                                | 39.8 us: 1.05x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.2 ms: 1.06x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 460 us: 1.06x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 19.0 ms: 1.08x slower                                                  |
| sympy_expand               | 582 ms                                                 | 631 ms: 1.08x slower                                                   |
| nbody                      | 119 ms                                                 | 130 ms: 1.09x slower                                                   |
| json                       | 6.85 ms                                                | 7.51 ms: 1.10x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.3 ms: 1.14x slower                                                  |
| telco                      | 9.59 ms                                                | 11.3 ms: 1.18x slower                                                  |
| coverage                   | 95.4 ms                                                | 116 ms: 1.21x slower                                                   |
| python_startup             | 23.7 ms                                                | 29.0 ms: 1.22x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.12 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.64 ms: 1.88x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 93.1 ms: 4.50x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (22): bench_thread_pool, 2to3, hexiom, sympy_sum, pathlib, deltablue, sqlglot_parse, thrift, sympy_integrate, richards_super, genshi_xml, genshi_text, unpickle_pure_python, scimark_sparse_mat_mult, pidigits, fannkuch, sqlalchemy_imperative, mako, xml_etree_process, django_template, scimark_lu, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.13x