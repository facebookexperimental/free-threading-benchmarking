# Results vs. 3.13.0rc2

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.036x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 494 ms: 1.11x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.82 sec: 1.05x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 373 ms: 1.54x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 921 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 963 ms: 1.46x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 523 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 389 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 528 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 712 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 717 ms: 1.19x faster                                                   |
| async_generators           | 567 ms                                                       | 531 ms: 1.07x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 740 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 136 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.88 ms: 1.22x faster                                                  |
| regex_compile  | 182 ms                                                       | 161 ms: 1.13x faster                                                   |
| Geometric mean | (ref)                                                        | 1.09x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 208 ms: 1.11x faster                                                   |
| xml_etree_iterparse | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.55 sec: 1.09x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 15.5 ms: 1.10x slower                                                  |
| json_loads          | 34.3 us                                                      | 40.2 us: 1.17x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_generate, xml_etree_process, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.7 ms: 1.28x slower                                                  |
| python_startup         | 22.4 ms                                                      | 32.1 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 28.6 ms: 1.11x faster                                                  |
| genshi_xml      | 72.1 ms                                                      | 67.8 ms: 1.06x faster                                                  |
| django_template | 44.3 ms                                                      | 48.2 ms: 1.09x slower                                                  |
| mako            | 15.9 ms                                                      | 18.9 ms: 1.18x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 373 ms: 1.54x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 921 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 963 ms: 1.46x faster                                                   |
| deepcopy                   | 498 us                                                       | 354 us: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 523 ms: 1.36x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 37.9 us: 1.32x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 389 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 528 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 712 ms: 1.25x faster                                                   |
| telco                      | 12.2 ms                                                      | 9.88 ms: 1.23x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 3.88 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.37 us: 1.22x faster                                                  |
| spectral_norm              | 157 ms                                                       | 130 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 717 ms: 1.19x faster                                                   |
| go                         | 191 ms                                                       | 162 ms: 1.18x faster                                                   |
| scimark_sor                | 179 ms                                                       | 152 ms: 1.17x faster                                                   |
| dulwich_log                | 93.7 ms                                                      | 81.5 ms: 1.15x faster                                                  |
| regex_compile              | 182 ms                                                       | 161 ms: 1.13x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 208 ms: 1.11x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 28.6 ms: 1.11x faster                                                  |
| pylint                     | 470 ms                                                       | 428 ms: 1.10x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 27.3 ms: 1.10x faster                                                  |
| richards                   | 65.5 ms                                                      | 59.9 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.55 sec: 1.09x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.67 us: 1.09x faster                                                  |
| sympy_str                  | 379 ms                                                       | 351 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.31 ms: 1.07x faster                                                  |
| async_generators           | 567 ms                                                       | 531 ms: 1.07x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 67.8 ms: 1.06x faster                                                  |
| scimark_fft                | 473 ms                                                       | 445 ms: 1.06x faster                                                   |
| nqueens                    | 112 ms                                                       | 105 ms: 1.06x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 200 ms: 1.05x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.82 sec: 1.05x faster                                                 |
| pprint_safe_repr           | 987 ms                                                       | 952 ms: 1.04x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 740 ms: 1.04x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.70 sec: 1.03x faster                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 6.46 sec: 1.03x slower                                                 |
| sqlglot_parse              | 1.76 ms                                                      | 1.84 ms: 1.05x slower                                                  |
| raytrace                   | 344 ms                                                       | 362 ms: 1.05x slower                                                   |
| chaos                      | 83.6 ms                                                      | 89.1 ms: 1.07x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 8.66 ms: 1.07x slower                                                  |
| django_template            | 44.3 ms                                                      | 48.2 ms: 1.09x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.5 ms: 1.10x slower                                                  |
| 2to3                       | 445 ms                                                       | 494 ms: 1.11x slower                                                   |
| coverage                   | 107 ms                                                       | 119 ms: 1.11x slower                                                   |
| json                       | 6.51 ms                                                      | 7.36 ms: 1.13x slower                                                  |
| nbody                      | 119 ms                                                       | 136 ms: 1.14x slower                                                   |
| json_loads                 | 34.3 us                                                      | 40.2 us: 1.17x slower                                                  |
| mako                       | 15.9 ms                                                      | 18.9 ms: 1.18x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 19.7 ms: 1.28x slower                                                  |
| python_startup             | 22.4 ms                                                      | 32.1 ms: 1.43x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.39 ms: 1.52x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.00 ms: 1.58x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.91 ms: 2.03x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 109 ms: 5.82x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (31): thrift, typing_runtime_protocols, float, xml_etree_generate, richards_super, xml_etree_process, pidigits, sympy_integrate, unpickle_pure_python, scimark_monte_carlo, pycparser, comprehensions, regex_v8, sqlglot_transpile, regex_dna, sqlglot_optimize, scimark_lu, fannkuch, sympy_expand, pprint_pformat, crypto_pyaes, meteor_contest, pickle_pure_python, deltablue, generators, logging_silent, pyflate, coroutines, sqlglot_normalize, logging_format, logging_simple
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x