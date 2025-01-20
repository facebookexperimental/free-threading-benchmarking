# Results vs. 3.13.0rc2

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.107x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 558 ms: 1.25x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.18 sec: 1.04x slower                                                 |
| html5lib       | 92.6 ms                                                      | 107 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                        | 1.15x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 758 ms: 1.85x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 929 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 342 ms: 1.47x faster                                                   |
| async_tree_none            | 572 ms                                                       | 393 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 482 ms: 1.39x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 534 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 677 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 810 ms: 1.10x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 34.2 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 185 ms: 1.55x slower                                                   |
| Geometric mean | (ref)                                                        | 1.15x slower                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.06 ms: 1.17x faster                                                  |
| regex_dna      | 282 ms                                                       | 299 ms: 1.06x slower                                                   |
| regex_compile  | 182 ms                                                       | 204 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 148 ms: 1.20x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 243 ms: 1.05x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.11 sec: 1.12x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 138 ms: 1.13x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 486 us: 1.17x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 343 us: 1.18x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 102 ms: 1.19x slower                                                   |
| json_loads           | 34.3 us                                                      | 46.7 us: 1.36x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 22.5 ms: 1.59x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 22.0 ms: 1.44x slower                                                  |
| python_startup         | 22.4 ms                                                      | 34.2 ms: 1.53x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 87.3 ms: 1.21x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 40.5 ms: 1.28x slower                                                  |
| django_template | 44.3 ms                                                      | 64.6 ms: 1.46x slower                                                  |
| mako            | 15.9 ms                                                      | 25.0 ms: 1.57x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.37x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 758 ms: 1.85x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 929 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 342 ms: 1.47x faster                                                   |
| async_tree_none            | 572 ms                                                       | 393 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 482 ms: 1.39x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 534 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 677 ms: 1.26x faster                                                   |
| deepcopy                   | 498 us                                                       | 397 us: 1.25x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 148 ms: 1.20x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.06 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 810 ms: 1.10x faster                                                   |
| docutils                   | 4.01 sec                                                     | 4.18 sec: 1.04x slower                                                 |
| xml_etree_parse            | 231 ms                                                       | 243 ms: 1.05x slower                                                   |
| scimark_sor                | 179 ms                                                       | 189 ms: 1.06x slower                                                   |
| regex_dna                  | 282 ms                                                       | 299 ms: 1.06x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 53.7 us: 1.07x slower                                                  |
| sqlite_synth               | 3.99 us                                                      | 4.28 us: 1.07x slower                                                  |
| mdp                        | 3.80 sec                                                     | 4.17 sec: 1.10x slower                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 82.3 ms: 1.10x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 34.2 ms: 1.11x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.11 sec: 1.12x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.10 sec: 1.12x slower                                                 |
| regex_compile              | 182 ms                                                       | 204 ms: 1.12x slower                                                   |
| logging_silent             | 130 ns                                                       | 147 ns: 1.13x slower                                                   |
| chaos                      | 83.6 ms                                                      | 94.3 ms: 1.13x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 138 ms: 1.13x slower                                                   |
| sympy_expand               | 601 ms                                                       | 682 ms: 1.14x slower                                                   |
| telco                      | 12.2 ms                                                      | 13.9 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.25 sec: 1.16x slower                                                 |
| html5lib                   | 92.6 ms                                                      | 107 ms: 1.16x slower                                                   |
| nqueens                    | 112 ms                                                       | 130 ms: 1.16x slower                                                   |
| meteor_contest             | 150 ms                                                       | 175 ms: 1.16x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 109 ms: 1.17x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 486 us: 1.17x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 2.83 ms: 1.17x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 343 us: 1.18x slower                                                   |
| scimark_fft                | 473 ms                                                       | 559 ms: 1.18x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 102 ms: 1.19x slower                                                   |
| fannkuch                   | 547 ms                                                       | 652 ms: 1.19x slower                                                   |
| json                       | 6.51 ms                                                      | 7.80 ms: 1.20x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 176 ms: 1.20x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 121 ms: 1.21x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 87.3 ms: 1.21x slower                                                  |
| comprehensions             | 22.2 us                                                      | 26.9 us: 1.21x slower                                                  |
| pyflate                    | 664 ms                                                       | 807 ms: 1.22x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 170 ms: 1.22x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.77 sec: 1.24x slower                                                 |
| richards                   | 65.5 ms                                                      | 81.5 ms: 1.24x slower                                                  |
| 2to3                       | 445 ms                                                       | 558 ms: 1.25x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 37.9 ms: 1.25x slower                                                  |
| generators                 | 40.0 ms                                                      | 50.2 ms: 1.25x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 264 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.51 ms: 1.26x slower                                                  |
| richards_super             | 73.2 ms                                                      | 92.3 ms: 1.26x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.80 ms: 1.27x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 40.5 ms: 1.28x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 118 ms: 1.30x slower                                                   |
| coverage                   | 107 ms                                                       | 141 ms: 1.32x slower                                                   |
| logging_format             | 9.24 us                                                      | 12.2 us: 1.32x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.34 ms: 1.33x slower                                                  |
| json_loads                 | 34.3 us                                                      | 46.7 us: 1.36x slower                                                  |
| sympy_str                  | 379 ms                                                       | 516 ms: 1.36x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 315 us: 1.40x slower                                                   |
| logging_simple             | 8.56 us                                                      | 12.0 us: 1.40x slower                                                  |
| raytrace                   | 344 ms                                                       | 484 ms: 1.41x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.55 ms: 1.41x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 11.5 ms: 1.42x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 22.0 ms: 1.44x slower                                                  |
| django_template            | 44.3 ms                                                      | 64.6 ms: 1.46x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.60 ms: 1.51x slower                                                  |
| python_startup             | 22.4 ms                                                      | 34.2 ms: 1.53x slower                                                  |
| nbody                      | 119 ms                                                       | 185 ms: 1.55x slower                                                   |
| mako                       | 15.9 ms                                                      | 25.0 ms: 1.57x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 22.5 ms: 1.59x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 7.35 ms: 1.66x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 5.00 ms: 1.73x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.1 ms: 5.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                           |

Benchmark hidden because not significant (11): pidigits, go, regex_v8, pylint, asyncio_websockets, pycparser, async_generators, deepcopy_reduce, spectral_norm, float, pathlib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x