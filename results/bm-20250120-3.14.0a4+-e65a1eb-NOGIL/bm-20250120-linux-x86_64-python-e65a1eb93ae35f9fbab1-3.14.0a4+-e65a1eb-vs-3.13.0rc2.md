# Results vs. 3.13.0rc2

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 580 ms: 1.30x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.47 sec: 1.11x slower                                                 |
| html5lib       | 92.6 ms                                                      | 108 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                        | 1.19x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 753 ms: 1.86x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 864 ms: 1.61x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 335 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 395 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 486 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 683 ms: 1.25x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 586 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 749 ms: 1.19x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 33.7 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 108 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                       | 192 ms: 1.62x slower                                                   |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.5 ms: 1.05x slower                                                  |
| regex_dna      | 282 ms                                                       | 309 ms: 1.10x slower                                                   |
| regex_compile  | 182 ms                                                       | 224 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 140 ms: 1.26x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.04 sec: 1.09x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 135 ms: 1.10x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 492 us: 1.18x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 107 ms: 1.24x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 361 us: 1.24x slower                                                   |
| json_loads           | 34.3 us                                                      | 46.2 us: 1.35x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 19.4 ms: 1.37x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.14x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 22.4 ms: 1.47x slower                                                  |
| python_startup         | 22.4 ms                                                      | 35.1 ms: 1.57x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.52x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 89.2 ms: 1.24x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 40.7 ms: 1.29x slower                                                  |
| django_template | 44.3 ms                                                      | 60.3 ms: 1.36x slower                                                  |
| mako            | 15.9 ms                                                      | 24.8 ms: 1.55x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.35x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 753 ms: 1.86x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 864 ms: 1.61x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 335 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 395 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 486 ms: 1.38x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 140 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 683 ms: 1.25x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 586 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 749 ms: 1.19x faster                                                   |
| deepcopy                   | 498 us                                                       | 449 us: 1.11x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.63 us: 1.10x faster                                                  |
| float                      | 116 ms                                                       | 108 ms: 1.08x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 34.5 ms: 1.05x slower                                                  |
| telco                      | 12.2 ms                                                      | 13.0 ms: 1.07x slower                                                  |
| richards                   | 65.5 ms                                                      | 70.4 ms: 1.07x slower                                                  |
| sympy_str                  | 379 ms                                                       | 408 ms: 1.08x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.04 sec: 1.09x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 33.7 ms: 1.09x slower                                                  |
| regex_dna                  | 282 ms                                                       | 309 ms: 1.10x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 135 ms: 1.10x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 33.6 ms: 1.11x slower                                                  |
| scimark_sor                | 179 ms                                                       | 199 ms: 1.11x slower                                                   |
| docutils                   | 4.01 sec                                                     | 4.47 sec: 1.11x slower                                                 |
| dulwich_log                | 93.7 ms                                                      | 105 ms: 1.12x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.11 sec: 1.13x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.65 us: 1.14x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 85.4 ms: 1.14x slower                                                  |
| sympy_expand               | 601 ms                                                       | 689 ms: 1.15x slower                                                   |
| json                       | 6.51 ms                                                      | 7.50 ms: 1.15x slower                                                  |
| generators                 | 40.0 ms                                                      | 46.4 ms: 1.16x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 108 ms: 1.16x slower                                                   |
| pyflate                    | 664 ms                                                       | 772 ms: 1.16x slower                                                   |
| richards_super             | 73.2 ms                                                      | 85.9 ms: 1.17x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 165 ms: 1.18x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.48 sec: 1.18x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 492 us: 1.18x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 249 ms: 1.18x slower                                                   |
| chaos                      | 83.6 ms                                                      | 99.1 ms: 1.19x slower                                                  |
| comprehensions             | 22.2 us                                                      | 26.4 us: 1.19x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.36 sec: 1.21x slower                                                 |
| scimark_fft                | 473 ms                                                       | 574 ms: 1.21x slower                                                   |
| regex_compile              | 182 ms                                                       | 224 ms: 1.23x slower                                                   |
| logging_silent             | 130 ns                                                       | 161 ns: 1.24x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 89.2 ms: 1.24x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 107 ms: 1.24x slower                                                   |
| fannkuch                   | 547 ms                                                       | 679 ms: 1.24x slower                                                   |
| nqueens                    | 112 ms                                                       | 139 ms: 1.24x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 361 us: 1.24x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.86 sec: 1.25x slower                                                 |
| meteor_contest             | 150 ms                                                       | 188 ms: 1.25x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 40.7 ms: 1.29x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.68 ms: 1.29x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 129 ms: 1.29x slower                                                   |
| 2to3                       | 445 ms                                                       | 580 ms: 1.30x slower                                                   |
| logging_simple             | 8.56 us                                                      | 11.3 us: 1.32x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.20 ms: 1.33x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 195 ms: 1.33x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 121 ms: 1.33x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 302 us: 1.34x slower                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 2.36 ms: 1.35x slower                                                  |
| json_loads                 | 34.3 us                                                      | 46.2 us: 1.35x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.49 ms: 1.35x slower                                                  |
| django_template            | 44.3 ms                                                      | 60.3 ms: 1.36x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 19.4 ms: 1.37x slower                                                  |
| coverage                   | 107 ms                                                       | 150 ms: 1.39x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 11.5 ms: 1.42x slower                                                  |
| logging_format             | 9.24 us                                                      | 13.2 us: 1.43x slower                                                  |
| raytrace                   | 344 ms                                                       | 503 ms: 1.46x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 22.4 ms: 1.47x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.76 ms: 1.54x slower                                                  |
| mako                       | 15.9 ms                                                      | 24.8 ms: 1.55x slower                                                  |
| python_startup             | 22.4 ms                                                      | 35.1 ms: 1.57x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 7.11 ms: 1.60x slower                                                  |
| nbody                      | 119 ms                                                       | 192 ms: 1.62x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 3.59 ms: 1.63x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 5.88 ms: 2.04x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 103 ms: 5.51x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                           |

Benchmark hidden because not significant (11): go, pidigits, regex_effbot, spectral_norm, xml_etree_parse, pycparser, async_generators, asyncio_websockets, pathlib, pylint, deepcopy_memo
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.34x