# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8145ebe
- commit date: 2024-09-12
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 669 ms: 1.50x slower                                  |
| docutils       | 4.01 sec                                                     | 4.89 sec: 1.22x slower                                |
| html5lib       | 92.6 ms                                                      | 133 ms: 1.44x slower                                  |
| tornado_http   | 251 ms                                                       | 374 ms: 1.49x slower                                  |
| Geometric mean | (ref)                                                        | 1.41x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| async_tree_io           | 1.39 sec                                                     | 1.24 sec: 1.12x faster                                |
| asyncio_websockets      | 766 ms                                                       | 802 ms: 1.05x slower                                  |
| async_tree_memoization  | 709 ms                                                       | 751 ms: 1.06x slower                                  |
| async_tree_none         | 572 ms                                                       | 609 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed | 889 ms                                                       | 948 ms: 1.07x slower                                  |
| asyncio_tcp             | 948 ms                                                       | 1.10 sec: 1.16x slower                                |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.36 sec: 1.21x slower                                |
| async_generators        | 567 ms                                                       | 742 ms: 1.31x slower                                  |
| coroutines              | 30.9 ms                                                      | 44.4 ms: 1.44x slower                                 |
| Geometric mean          | (ref)                                                        | 1.07x slower                                          |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 196 ms: 1.69x slower                                  |
| nbody          | 119 ms                                                       | 281 ms: 2.37x slower                                  |
| Geometric mean | (ref)                                                        | 1.58x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.42 ms: 1.07x faster                                 |
| regex_v8       | 32.8 ms                                                      | 37.2 ms: 1.13x slower                                 |
| regex_compile  | 182 ms                                                       | 288 ms: 1.58x slower                                  |
| Geometric mean | (ref)                                                        | 1.14x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle             | 20.5 us                                                      | 22.3 us: 1.09x slower                                 |
| unpickle_list        | 6.68 us                                                      | 7.64 us: 1.14x slower                                 |
| json_loads           | 34.3 us                                                      | 41.7 us: 1.22x slower                                 |
| json_dumps           | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 170 ms: 1.39x slower                                  |
| xml_etree_process    | 85.9 ms                                                      | 126 ms: 1.47x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.34 sec: 1.56x slower                                |
| unpickle_pure_python | 290 us                                                       | 516 us: 1.78x slower                                  |
| pickle_pure_python   | 416 us                                                       | 847 us: 2.03x slower                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                          |

Benchmark hidden because not significant (5): pickle_dict, xml_etree_parse, pickle, xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.3 ms: 1.39x slower                                 |
| python_startup         | 22.4 ms                                                      | 32.2 ms: 1.44x slower                                 |
| Geometric mean         | (ref)                                                        | 1.41x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 118 ms: 1.64x slower                                  |
| django_template | 44.3 ms                                                      | 85.0 ms: 1.92x slower                                 |
| genshi_text     | 31.7 ms                                                      | 60.8 ms: 1.92x slower                                 |
| mako            | 15.9 ms                                                      | 31.6 ms: 1.98x slower                                 |
| Geometric mean  | (ref)                                                        | 1.86x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg         | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| create_gc_cycles         | 2.41 ms                                                      | 2.04 ms: 1.18x faster                                 |
| gc_traversal             | 5.70 ms                                                      | 4.89 ms: 1.17x faster                                 |
| async_tree_io            | 1.39 sec                                                     | 1.24 sec: 1.12x faster                                |
| regex_effbot             | 4.74 ms                                                      | 4.42 ms: 1.07x faster                                 |
| asyncio_websockets       | 766 ms                                                       | 802 ms: 1.05x slower                                  |
| async_tree_memoization   | 709 ms                                                       | 751 ms: 1.06x slower                                  |
| async_tree_none          | 572 ms                                                       | 609 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 948 ms: 1.07x slower                                  |
| unpickle                 | 20.5 us                                                      | 22.3 us: 1.09x slower                                 |
| sqlite_synth             | 3.99 us                                                      | 4.43 us: 1.11x slower                                 |
| regex_v8                 | 32.8 ms                                                      | 37.2 ms: 1.13x slower                                 |
| telco                    | 12.2 ms                                                      | 13.9 ms: 1.14x slower                                 |
| unpickle_list            | 6.68 us                                                      | 7.64 us: 1.14x slower                                 |
| asyncio_tcp              | 948 ms                                                       | 1.10 sec: 1.16x slower                                |
| deepcopy                 | 498 us                                                       | 581 us: 1.17x slower                                  |
| pathlib                  | 29.9 ms                                                      | 35.3 ms: 1.18x slower                                 |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.36 sec: 1.21x slower                                |
| json_loads               | 34.3 us                                                      | 41.7 us: 1.22x slower                                 |
| docutils                 | 4.01 sec                                                     | 4.89 sec: 1.22x slower                                |
| json                     | 6.51 ms                                                      | 8.00 ms: 1.23x slower                                 |
| json_dumps               | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                 |
| pylint                   | 470 ms                                                       | 610 ms: 1.30x slower                                  |
| async_generators         | 567 ms                                                       | 742 ms: 1.31x slower                                  |
| generators               | 40.0 ms                                                      | 52.8 ms: 1.32x slower                                 |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.92 ms: 1.32x slower                                 |
| scimark_fft              | 473 ms                                                       | 631 ms: 1.33x slower                                  |
| mdp                      | 3.80 sec                                                     | 5.21 sec: 1.37x slower                                |
| deepcopy_memo            | 50.1 us                                                      | 68.8 us: 1.37x slower                                 |
| meteor_contest           | 150 ms                                                       | 208 ms: 1.38x slower                                  |
| xml_etree_generate       | 122 ms                                                       | 170 ms: 1.39x slower                                  |
| nqueens                  | 112 ms                                                       | 155 ms: 1.39x slower                                  |
| python_startup_no_site   | 15.3 ms                                                      | 21.3 ms: 1.39x slower                                 |
| fannkuch                 | 547 ms                                                       | 767 ms: 1.40x slower                                  |
| pycparser                | 1.57 sec                                                     | 2.24 sec: 1.43x slower                                |
| html5lib                 | 92.6 ms                                                      | 133 ms: 1.44x slower                                  |
| python_startup           | 22.4 ms                                                      | 32.2 ms: 1.44x slower                                 |
| coroutines               | 30.9 ms                                                      | 44.4 ms: 1.44x slower                                 |
| deepcopy_reduce          | 4.10 us                                                      | 5.91 us: 1.44x slower                                 |
| coverage                 | 107 ms                                                       | 156 ms: 1.45x slower                                  |
| xml_etree_process        | 85.9 ms                                                      | 126 ms: 1.47x slower                                  |
| typing_runtime_protocols | 226 us                                                       | 334 us: 1.48x slower                                  |
| tornado_http             | 251 ms                                                       | 374 ms: 1.49x slower                                  |
| 2to3                     | 445 ms                                                       | 669 ms: 1.50x slower                                  |
| crypto_pyaes             | 100 ms                                                       | 151 ms: 1.50x slower                                  |
| sympy_integrate          | 30.2 ms                                                      | 46.3 ms: 1.53x slower                                 |
| thrift                   | 1.10 ms                                                      | 1.71 ms: 1.55x slower                                 |
| tomli_loads              | 2.78 sec                                                     | 4.34 sec: 1.56x slower                                |
| pyflate                  | 664 ms                                                       | 1.04 sec: 1.56x slower                                |
| spectral_norm            | 157 ms                                                       | 245 ms: 1.57x slower                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 117 ms: 1.57x slower                                  |
| regex_compile            | 182 ms                                                       | 288 ms: 1.58x slower                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 10.2 sec: 1.63x slower                                |
| genshi_xml               | 72.1 ms                                                      | 118 ms: 1.64x slower                                  |
| bench_thread_pool        | 2.89 ms                                                      | 4.74 ms: 1.64x slower                                 |
| richards                 | 65.5 ms                                                      | 108 ms: 1.65x slower                                  |
| comprehensions           | 22.2 us                                                      | 37.2 us: 1.67x slower                                 |
| richards_super           | 73.2 ms                                                      | 123 ms: 1.68x slower                                  |
| float                    | 116 ms                                                       | 196 ms: 1.69x slower                                  |
| dulwich_log              | 93.7 ms                                                      | 159 ms: 1.69x slower                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.69 sec: 1.71x slower                                |
| logging_format           | 9.24 us                                                      | 16.3 us: 1.77x slower                                 |
| logging_simple           | 8.56 us                                                      | 15.2 us: 1.77x slower                                 |
| unpickle_pure_python     | 290 us                                                       | 516 us: 1.78x slower                                  |
| sqlglot_normalize        | 140 ms                                                       | 250 ms: 1.79x slower                                  |
| pprint_pformat           | 1.94 sec                                                     | 3.52 sec: 1.81x slower                                |
| sympy_str                | 379 ms                                                       | 687 ms: 1.81x slower                                  |
| scimark_monte_carlo      | 90.6 ms                                                      | 166 ms: 1.84x slower                                  |
| go                       | 191 ms                                                       | 361 ms: 1.89x slower                                  |
| chaos                    | 83.6 ms                                                      | 159 ms: 1.91x slower                                  |
| django_template          | 44.3 ms                                                      | 85.0 ms: 1.92x slower                                 |
| genshi_text              | 31.7 ms                                                      | 60.8 ms: 1.92x slower                                 |
| scimark_sor              | 179 ms                                                       | 345 ms: 1.93x slower                                  |
| hexiom                   | 8.11 ms                                                      | 16.0 ms: 1.97x slower                                 |
| logging_silent           | 130 ns                                                       | 256 ns: 1.97x slower                                  |
| mako                     | 15.9 ms                                                      | 31.6 ms: 1.98x slower                                 |
| sqlglot_transpile        | 2.20 ms                                                      | 4.40 ms: 2.01x slower                                 |
| pickle_pure_python       | 416 us                                                       | 847 us: 2.03x slower                                  |
| scimark_lu               | 146 ms                                                       | 307 ms: 2.10x slower                                  |
| sympy_expand             | 601 ms                                                       | 1.33 sec: 2.21x slower                                |
| sqlglot_parse            | 1.76 ms                                                      | 3.90 ms: 2.22x slower                                 |
| raytrace                 | 344 ms                                                       | 766 ms: 2.22x slower                                  |
| sympy_sum                | 210 ms                                                       | 491 ms: 2.34x slower                                  |
| nbody                    | 119 ms                                                       | 281 ms: 2.37x slower                                  |
| deltablue                | 4.44 ms                                                      | 11.6 ms: 2.62x slower                                 |
| unpack_sequence          | 74.3 ns                                                      | 201 ns: 2.70x slower                                  |
| Geometric mean           | (ref)                                                        | 1.43x slower                                          |

Benchmark hidden because not significant (11): bench_mp_pool, pickle_dict, async_tree_memoization_tg, xml_etree_parse, pidigits, pickle, async_tree_none_tg, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, pickle_list, regex_dna
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.15x