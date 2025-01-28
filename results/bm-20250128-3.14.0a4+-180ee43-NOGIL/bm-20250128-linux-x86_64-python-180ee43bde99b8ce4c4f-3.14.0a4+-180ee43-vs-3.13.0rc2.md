# Results vs. 3.13.0rc2

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.129x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 620 ms: 1.39x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.25 sec: 1.06x slower                                                 |
| html5lib       | 92.6 ms                                                      | 102 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.18x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 838 ms: 1.67x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 963 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 517 ms: 1.30x faster                                                   |
| async_tree_none            | 572 ms                                                       | 449 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 690 ms: 1.23x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 429 ms: 1.17x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 632 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 822 ms: 1.08x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 811 ms: 1.06x slower                                                   |
| async_generators           | 567 ms                                                       | 610 ms: 1.07x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.17x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 264 ms: 1.05x slower                                                   |
| nbody          | 119 ms                                                       | 192 ms: 1.62x slower                                                   |
| Geometric mean | (ref)                                                        | 1.20x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 301 ms: 1.07x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                  |
| regex_compile  | 182 ms                                                       | 224 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 156 ms: 1.14x faster                                                   |
| xml_etree_process    | 85.9 ms                                                      | 98.7 ms: 1.15x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 143 ms: 1.17x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.28 sec: 1.18x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 532 us: 1.28x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 371 us: 1.28x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 18.2 ms: 1.29x slower                                                  |
| json_loads           | 34.3 us                                                      | 52.2 us: 1.52x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.18x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 22.7 ms: 1.48x slower                                                  |
| python_startup         | 22.4 ms                                                      | 36.2 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.55x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 39.2 ms: 1.24x slower                                                  |
| django_template | 44.3 ms                                                      | 56.0 ms: 1.26x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 95.0 ms: 1.32x slower                                                  |
| mako            | 15.9 ms                                                      | 27.3 ms: 1.71x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.37x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 838 ms: 1.67x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 963 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 517 ms: 1.30x faster                                                   |
| async_tree_none            | 572 ms                                                       | 449 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 690 ms: 1.23x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 429 ms: 1.17x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 156 ms: 1.14x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 632 ms: 1.12x faster                                                   |
| deepcopy                   | 498 us                                                       | 450 us: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 822 ms: 1.08x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.73 us: 1.07x faster                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 77.5 ms: 1.04x slower                                                  |
| pidigits                   | 251 ms                                                       | 264 ms: 1.05x slower                                                   |
| asyncio_websockets         | 766 ms                                                       | 811 ms: 1.06x slower                                                   |
| docutils                   | 4.01 sec                                                     | 4.25 sec: 1.06x slower                                                 |
| regex_dna                  | 282 ms                                                       | 301 ms: 1.07x slower                                                   |
| scimark_sor                | 179 ms                                                       | 191 ms: 1.07x slower                                                   |
| async_generators           | 567 ms                                                       | 610 ms: 1.07x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                  |
| pylint                     | 470 ms                                                       | 512 ms: 1.09x slower                                                   |
| richards                   | 65.5 ms                                                      | 71.9 ms: 1.10x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 102 ms: 1.10x slower                                                   |
| telco                      | 12.2 ms                                                      | 13.5 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.51 ms: 1.11x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 114 ms: 1.13x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 34.3 ms: 1.14x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 98.7 ms: 1.15x slower                                                  |
| go                         | 191 ms                                                       | 221 ms: 1.16x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.42 sec: 1.16x slower                                                 |
| pathlib                    | 29.9 ms                                                      | 34.9 ms: 1.17x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 143 ms: 1.17x slower                                                   |
| sympy_str                  | 379 ms                                                       | 443 ms: 1.17x slower                                                   |
| sympy_expand               | 601 ms                                                       | 707 ms: 1.18x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.28 sec: 1.18x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.18 sec: 1.19x slower                                                 |
| chaos                      | 83.6 ms                                                      | 101 ms: 1.21x slower                                                   |
| nqueens                    | 112 ms                                                       | 135 ms: 1.21x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.33 ms: 1.21x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 5.01 us: 1.22x slower                                                  |
| json                       | 6.51 ms                                                      | 8.02 ms: 1.23x slower                                                  |
| regex_compile              | 182 ms                                                       | 224 ms: 1.23x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 116 ms: 1.23x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.40 sec: 1.24x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 39.2 ms: 1.24x slower                                                  |
| coverage                   | 107 ms                                                       | 133 ms: 1.24x slower                                                   |
| pyflate                    | 664 ms                                                       | 825 ms: 1.24x slower                                                   |
| scimark_fft                | 473 ms                                                       | 597 ms: 1.26x slower                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 2.22 ms: 1.26x slower                                                  |
| django_template            | 44.3 ms                                                      | 56.0 ms: 1.26x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 268 ms: 1.27x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 532 us: 1.28x slower                                                   |
| generators                 | 40.0 ms                                                      | 51.2 ms: 1.28x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 371 us: 1.28x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.09 ms: 1.28x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 18.2 ms: 1.29x slower                                                  |
| comprehensions             | 22.2 us                                                      | 28.8 us: 1.30x slower                                                  |
| fannkuch                   | 547 ms                                                       | 712 ms: 1.30x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 95.0 ms: 1.32x slower                                                  |
| richards_super             | 73.2 ms                                                      | 97.2 ms: 1.33x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 8.35 sec: 1.33x slower                                                 |
| logging_format             | 9.24 us                                                      | 12.4 us: 1.34x slower                                                  |
| raytrace                   | 344 ms                                                       | 462 ms: 1.34x slower                                                   |
| meteor_contest             | 150 ms                                                       | 203 ms: 1.35x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 190 ms: 1.36x slower                                                   |
| 2to3                       | 445 ms                                                       | 620 ms: 1.39x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 315 us: 1.40x slower                                                   |
| logging_silent             | 130 ns                                                       | 182 ns: 1.40x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 206 ms: 1.41x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 129 ms: 1.42x slower                                                   |
| logging_simple             | 8.56 us                                                      | 12.3 us: 1.43x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 6.42 ms: 1.45x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 22.7 ms: 1.48x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 12.1 ms: 1.49x slower                                                  |
| json_loads                 | 34.3 us                                                      | 52.2 us: 1.52x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 3.40 ms: 1.55x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.84 ms: 1.55x slower                                                  |
| python_startup             | 22.4 ms                                                      | 36.2 ms: 1.61x slower                                                  |
| nbody                      | 119 ms                                                       | 192 ms: 1.62x slower                                                   |
| mako                       | 15.9 ms                                                      | 27.3 ms: 1.71x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 5.05 ms: 1.75x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 99.4 ms: 5.32x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.20x slower                                                           |

Benchmark hidden because not significant (7): regex_effbot, deepcopy_memo, float, xml_etree_parse, spectral_norm, pycparser, coroutines
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.129x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.34x