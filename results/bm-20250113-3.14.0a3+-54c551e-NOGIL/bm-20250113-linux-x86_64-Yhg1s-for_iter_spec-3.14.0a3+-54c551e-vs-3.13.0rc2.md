# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: for_iter_spec
- machine: linux-x86_64
- commit hash: 54c551e
- commit date: 2025-01-13
- overall geometric mean: 1.194x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 648 ms: 1.46x slower                                           |
| docutils       | 4.01 sec                                                     | 4.96 sec: 1.24x slower                                         |
| html5lib       | 92.6 ms                                                      | 130 ms: 1.41x slower                                           |
| Geometric mean | (ref)                                                        | 1.36x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 987 ms: 1.42x faster                                           |
| async_tree_io              | 1.39 sec                                                     | 1.07 sec: 1.30x faster                                         |
| async_tree_memoization_tg  | 670 ms                                                       | 564 ms: 1.19x faster                                           |
| async_tree_none_tg         | 504 ms                                                       | 428 ms: 1.18x faster                                           |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 741 ms: 1.15x faster                                           |
| async_tree_memoization     | 709 ms                                                       | 651 ms: 1.09x faster                                           |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 819 ms: 1.08x faster                                           |
| asyncio_websockets         | 766 ms                                                       | 734 ms: 1.04x faster                                           |
| async_tree_none            | 572 ms                                                       | 610 ms: 1.07x slower                                           |
| coroutines                 | 30.9 ms                                                      | 33.8 ms: 1.09x slower                                          |
| async_generators           | 567 ms                                                       | 715 ms: 1.26x slower                                           |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 238 ms: 1.06x faster                                           |
| float          | 116 ms                                                       | 144 ms: 1.24x slower                                           |
| nbody          | 119 ms                                                       | 168 ms: 1.41x slower                                           |
| Geometric mean | (ref)                                                        | 1.18x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 335 ms: 1.19x slower                                           |
| regex_v8       | 32.8 ms                                                      | 40.7 ms: 1.24x slower                                          |
| regex_compile  | 182 ms                                                       | 231 ms: 1.27x slower                                           |
| Geometric mean | (ref)                                                        | 1.18x slower                                                   |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 141 ms: 1.26x faster                                           |
| tomli_loads          | 2.78 sec                                                     | 3.09 sec: 1.11x slower                                         |
| json_loads           | 34.3 us                                                      | 40.1 us: 1.17x slower                                          |
| xml_etree_generate   | 122 ms                                                       | 150 ms: 1.22x slower                                           |
| json_dumps           | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                          |
| xml_etree_process    | 85.9 ms                                                      | 116 ms: 1.35x slower                                           |
| pickle_pure_python   | 416 us                                                       | 611 us: 1.47x slower                                           |
| unpickle_pure_python | 290 us                                                       | 436 us: 1.50x slower                                           |
| Geometric mean       | (ref)                                                        | 1.19x slower                                                   |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 22.3 ms: 1.45x slower                                          |
| python_startup         | 22.4 ms                                                      | 34.5 ms: 1.54x slower                                          |
| Geometric mean         | (ref)                                                        | 1.50x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 85.3 ms: 1.18x slower                                          |
| genshi_text     | 31.7 ms                                                      | 42.8 ms: 1.35x slower                                          |
| django_template | 44.3 ms                                                      | 63.8 ms: 1.44x slower                                          |
| mako            | 15.9 ms                                                      | 29.2 ms: 1.83x slower                                          |
| Geometric mean  | (ref)                                                        | 1.43x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 987 ms: 1.42x faster                                           |
| async_tree_io              | 1.39 sec                                                     | 1.07 sec: 1.30x faster                                         |
| xml_etree_iterparse        | 177 ms                                                       | 141 ms: 1.26x faster                                           |
| async_tree_memoization_tg  | 670 ms                                                       | 564 ms: 1.19x faster                                           |
| async_tree_none_tg         | 504 ms                                                       | 428 ms: 1.18x faster                                           |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 741 ms: 1.15x faster                                           |
| deepcopy                   | 498 us                                                       | 439 us: 1.13x faster                                           |
| async_tree_memoization     | 709 ms                                                       | 651 ms: 1.09x faster                                           |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 819 ms: 1.08x faster                                           |
| pidigits                   | 251 ms                                                       | 238 ms: 1.06x faster                                           |
| asyncio_websockets         | 766 ms                                                       | 734 ms: 1.04x faster                                           |
| deepcopy_reduce            | 4.10 us                                                      | 4.27 us: 1.04x slower                                          |
| async_tree_none            | 572 ms                                                       | 610 ms: 1.07x slower                                           |
| pathlib                    | 29.9 ms                                                      | 32.7 ms: 1.09x slower                                          |
| coroutines                 | 30.9 ms                                                      | 33.8 ms: 1.09x slower                                          |
| sqlglot_optimize           | 74.7 ms                                                      | 82.5 ms: 1.10x slower                                          |
| tomli_loads                | 2.78 sec                                                     | 3.09 sec: 1.11x slower                                         |
| pycparser                  | 1.57 sec                                                     | 1.76 sec: 1.12x slower                                         |
| telco                      | 12.2 ms                                                      | 13.7 ms: 1.13x slower                                          |
| deepcopy_memo              | 50.1 us                                                      | 58.0 us: 1.16x slower                                          |
| pylint                     | 470 ms                                                       | 545 ms: 1.16x slower                                           |
| sqlglot_normalize          | 140 ms                                                       | 162 ms: 1.16x slower                                           |
| json_loads                 | 34.3 us                                                      | 40.1 us: 1.17x slower                                          |
| scimark_fft                | 473 ms                                                       | 555 ms: 1.17x slower                                           |
| meteor_contest             | 150 ms                                                       | 176 ms: 1.17x slower                                           |
| spectral_norm              | 157 ms                                                       | 184 ms: 1.17x slower                                           |
| genshi_xml                 | 72.1 ms                                                      | 85.3 ms: 1.18x slower                                          |
| sympy_str                  | 379 ms                                                       | 450 ms: 1.19x slower                                           |
| sympy_sum                  | 210 ms                                                       | 250 ms: 1.19x slower                                           |
| regex_dna                  | 282 ms                                                       | 335 ms: 1.19x slower                                           |
| json                       | 6.51 ms                                                      | 7.76 ms: 1.19x slower                                          |
| typing_runtime_protocols   | 226 us                                                       | 274 us: 1.21x slower                                           |
| xml_etree_generate         | 122 ms                                                       | 150 ms: 1.22x slower                                           |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.31 ms: 1.23x slower                                          |
| mdp                        | 3.80 sec                                                     | 4.67 sec: 1.23x slower                                         |
| bpe_tokeniser              | 6.28 sec                                                     | 7.75 sec: 1.23x slower                                         |
| docutils                   | 4.01 sec                                                     | 4.96 sec: 1.24x slower                                         |
| float                      | 116 ms                                                       | 144 ms: 1.24x slower                                           |
| regex_v8                   | 32.8 ms                                                      | 40.7 ms: 1.24x slower                                          |
| fannkuch                   | 547 ms                                                       | 685 ms: 1.25x slower                                           |
| async_generators           | 567 ms                                                       | 715 ms: 1.26x slower                                           |
| regex_compile              | 182 ms                                                       | 231 ms: 1.27x slower                                           |
| nqueens                    | 112 ms                                                       | 143 ms: 1.28x slower                                           |
| pprint_safe_repr           | 987 ms                                                       | 1.27 sec: 1.29x slower                                         |
| sympy_integrate            | 30.2 ms                                                      | 39.0 ms: 1.29x slower                                          |
| sympy_expand               | 601 ms                                                       | 793 ms: 1.32x slower                                           |
| coverage                   | 107 ms                                                       | 143 ms: 1.33x slower                                           |
| json_dumps                 | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                          |
| richards_super             | 73.2 ms                                                      | 98.3 ms: 1.34x slower                                          |
| genshi_text                | 31.7 ms                                                      | 42.8 ms: 1.35x slower                                          |
| xml_etree_process          | 85.9 ms                                                      | 116 ms: 1.35x slower                                           |
| pprint_pformat             | 1.94 sec                                                     | 2.67 sec: 1.37x slower                                         |
| gc_traversal               | 5.70 ms                                                      | 7.83 ms: 1.37x slower                                          |
| pyflate                    | 664 ms                                                       | 913 ms: 1.38x slower                                           |
| richards                   | 65.5 ms                                                      | 90.6 ms: 1.38x slower                                          |
| thrift                     | 1.10 ms                                                      | 1.53 ms: 1.39x slower                                          |
| html5lib                   | 92.6 ms                                                      | 130 ms: 1.41x slower                                           |
| nbody                      | 119 ms                                                       | 168 ms: 1.41x slower                                           |
| scimark_sor                | 179 ms                                                       | 253 ms: 1.42x slower                                           |
| dulwich_log                | 93.7 ms                                                      | 133 ms: 1.42x slower                                           |
| scimark_lu                 | 146 ms                                                       | 209 ms: 1.42x slower                                           |
| generators                 | 40.0 ms                                                      | 57.3 ms: 1.43x slower                                          |
| scimark_monte_carlo        | 90.6 ms                                                      | 130 ms: 1.43x slower                                           |
| django_template            | 44.3 ms                                                      | 63.8 ms: 1.44x slower                                          |
| python_startup_no_site     | 15.3 ms                                                      | 22.3 ms: 1.45x slower                                          |
| 2to3                       | 445 ms                                                       | 648 ms: 1.46x slower                                           |
| pickle_pure_python         | 416 us                                                       | 611 us: 1.47x slower                                           |
| bench_thread_pool          | 2.89 ms                                                      | 4.30 ms: 1.49x slower                                          |
| unpickle_pure_python       | 290 us                                                       | 436 us: 1.50x slower                                           |
| logging_format             | 9.24 us                                                      | 13.9 us: 1.50x slower                                          |
| crypto_pyaes               | 100 ms                                                       | 151 ms: 1.51x slower                                           |
| chaos                      | 83.6 ms                                                      | 128 ms: 1.53x slower                                           |
| python_startup             | 22.4 ms                                                      | 34.5 ms: 1.54x slower                                          |
| create_gc_cycles           | 2.41 ms                                                      | 3.73 ms: 1.55x slower                                          |
| go                         | 191 ms                                                       | 296 ms: 1.55x slower                                           |
| logging_simple             | 8.56 us                                                      | 13.3 us: 1.55x slower                                          |
| sqlglot_transpile          | 2.20 ms                                                      | 3.58 ms: 1.63x slower                                          |
| comprehensions             | 22.2 us                                                      | 36.7 us: 1.65x slower                                          |
| hexiom                     | 8.11 ms                                                      | 14.2 ms: 1.75x slower                                          |
| mako                       | 15.9 ms                                                      | 29.2 ms: 1.83x slower                                          |
| raytrace                   | 344 ms                                                       | 633 ms: 1.84x slower                                           |
| logging_silent             | 130 ns                                                       | 253 ns: 1.95x slower                                           |
| sqlglot_parse              | 1.76 ms                                                      | 3.48 ms: 1.98x slower                                          |
| deltablue                  | 4.44 ms                                                      | 10.8 ms: 2.43x slower                                          |
| bench_mp_pool              | 18.7 ms                                                      | 102 ms: 5.47x slower                                           |
| Geometric mean             | (ref)                                                        | 1.28x slower                                                   |

Benchmark hidden because not significant (3): xml_etree_parse, sqlite_synth, regex_effbot
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250113-3.14.0a3+-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.194x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x