# Results vs. 3.13.0rc2

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.132x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 567 ms: 1.27x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.15 sec: 1.04x slower                                                 |
| html5lib       | 92.6 ms                                                      | 115 ms: 1.25x slower                                                   |
| Geometric mean | (ref)                                                        | 1.18x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 830 ms: 1.69x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 988 ms: 1.40x faster                                                   |
| async_tree_none            | 572 ms                                                       | 438 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 396 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 544 ms: 1.23x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 587 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 786 ms: 1.08x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 807 ms: 1.05x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 37.4 ms: 1.21x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.16x faster                                                           |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| nbody          | 119 ms                                                       | 206 ms: 1.74x slower                                                   |
| Geometric mean | (ref)                                                        | 1.15x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.22 ms: 1.12x faster                                                  |
| regex_dna      | 282 ms                                                       | 300 ms: 1.06x slower                                                   |
| regex_compile  | 182 ms                                                       | 222 ms: 1.22x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 152 ms: 1.16x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.22 sec: 1.16x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 16.4 ms: 1.16x slower                                                  |
| json_loads           | 34.3 us                                                      | 40.8 us: 1.19x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 110 ms: 1.28x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 392 us: 1.35x slower                                                   |
| xml_etree_generate   | 122 ms                                                       | 167 ms: 1.37x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 668 us: 1.60x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.20x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.3 ms: 1.39x slower                                                  |
| python_startup         | 22.4 ms                                                      | 34.9 ms: 1.56x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.3 ms                                                      | 55.1 ms: 1.24x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 43.2 ms: 1.36x slower                                                  |
| mako            | 15.9 ms                                                      | 22.8 ms: 1.43x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 104 ms: 1.45x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.37x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 830 ms: 1.69x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 988 ms: 1.40x faster                                                   |
| async_tree_none            | 572 ms                                                       | 438 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 396 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 544 ms: 1.23x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 587 ms: 1.21x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 152 ms: 1.16x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.22 ms: 1.12x faster                                                  |
| float                      | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 786 ms: 1.08x faster                                                   |
| docutils                   | 4.01 sec                                                     | 4.15 sec: 1.04x slower                                                 |
| pycparser                  | 1.57 sec                                                     | 1.63 sec: 1.04x slower                                                 |
| asyncio_websockets         | 766 ms                                                       | 807 ms: 1.05x slower                                                   |
| regex_dna                  | 282 ms                                                       | 300 ms: 1.06x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 53.6 us: 1.07x slower                                                  |
| pathlib                    | 29.9 ms                                                      | 32.0 ms: 1.07x slower                                                  |
| deepcopy                   | 498 us                                                       | 533 us: 1.07x slower                                                   |
| richards                   | 65.5 ms                                                      | 72.1 ms: 1.10x slower                                                  |
| mdp                        | 3.80 sec                                                     | 4.19 sec: 1.10x slower                                                 |
| telco                      | 12.2 ms                                                      | 13.6 ms: 1.12x slower                                                  |
| logging_silent             | 130 ns                                                       | 146 ns: 1.12x slower                                                   |
| sympy_expand               | 601 ms                                                       | 686 ms: 1.14x slower                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 4.70 us: 1.15x slower                                                  |
| richards_super             | 73.2 ms                                                      | 84.5 ms: 1.15x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.22 sec: 1.16x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 16.4 ms: 1.16x slower                                                  |
| go                         | 191 ms                                                       | 227 ms: 1.19x slower                                                   |
| json                       | 6.51 ms                                                      | 7.74 ms: 1.19x slower                                                  |
| json_loads                 | 34.3 us                                                      | 40.8 us: 1.19x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.18 sec: 1.19x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 36.1 ms: 1.19x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 89.5 ms: 1.20x slower                                                  |
| fannkuch                   | 547 ms                                                       | 659 ms: 1.20x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 169 ms: 1.21x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 37.4 ms: 1.21x slower                                                  |
| regex_compile              | 182 ms                                                       | 222 ms: 1.22x slower                                                   |
| scimark_fft                | 473 ms                                                       | 578 ms: 1.22x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 2.95 ms: 1.22x slower                                                  |
| nqueens                    | 112 ms                                                       | 137 ms: 1.22x slower                                                   |
| meteor_contest             | 150 ms                                                       | 185 ms: 1.23x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.77 sec: 1.24x slower                                                 |
| generators                 | 40.0 ms                                                      | 49.6 ms: 1.24x slower                                                  |
| django_template            | 44.3 ms                                                      | 55.1 ms: 1.24x slower                                                  |
| logging_simple             | 8.56 us                                                      | 10.6 us: 1.24x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 115 ms: 1.25x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.44 sec: 1.25x slower                                                 |
| sympy_str                  | 379 ms                                                       | 480 ms: 1.27x slower                                                   |
| 2to3                       | 445 ms                                                       | 567 ms: 1.27x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 110 ms: 1.28x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 129 ms: 1.28x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.9 us: 1.29x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 123 ms: 1.31x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 119 ms: 1.32x slower                                                   |
| chaos                      | 83.6 ms                                                      | 110 ms: 1.32x slower                                                   |
| comprehensions             | 22.2 us                                                      | 29.5 us: 1.33x slower                                                  |
| raytrace                   | 344 ms                                                       | 463 ms: 1.34x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.10 ms: 1.35x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.48 ms: 1.35x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 392 us: 1.35x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.98 ms: 1.36x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 11.0 ms: 1.36x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 43.2 ms: 1.36x slower                                                  |
| pyflate                    | 664 ms                                                       | 906 ms: 1.37x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 167 ms: 1.37x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 288 ms: 1.37x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 21.3 ms: 1.39x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.04 ms: 1.40x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 206 ms: 1.41x slower                                                   |
| mako                       | 15.9 ms                                                      | 22.8 ms: 1.43x slower                                                  |
| coverage                   | 107 ms                                                       | 155 ms: 1.44x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 104 ms: 1.45x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 327 us: 1.45x slower                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 2.55 ms: 1.45x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.35 ms: 1.46x slower                                                  |
| python_startup             | 22.4 ms                                                      | 34.9 ms: 1.56x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 7.05 ms: 1.59x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 668 us: 1.60x slower                                                   |
| nbody                      | 119 ms                                                       | 206 ms: 1.74x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 92.5 ms: 4.95x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.19x slower                                                           |

Benchmark hidden because not significant (9): async_tree_cpu_io_mixed, pidigits, regex_v8, scimark_sor, xml_etree_parse, spectral_norm, pylint, sqlite_synth, async_generators
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.132x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.34x