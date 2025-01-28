# Results vs. 3.13.0rc2

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.029x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 489 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 392 ms: 1.46x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 954 ms: 1.45x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 969 ms: 1.45x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 509 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 494 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 407 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 708 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 738 ms: 1.20x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 722 ms: 1.06x faster                                                   |
| async_generators           | 567 ms                                                       | 537 ms: 1.06x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 34.9 ms: 1.13x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 110 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.11 ms: 1.15x faster                                                  |
| regex_compile  | 182 ms                                                       | 173 ms: 1.05x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 39.6 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 157 ms: 1.13x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 213 ms: 1.09x faster                                                   |
| json_dumps          | 14.1 ms                                                      | 14.7 ms: 1.04x slower                                                  |
| json_loads          | 34.3 us                                                      | 36.8 us: 1.07x slower                                                  |
| pickle_pure_python  | 416 us                                                       | 467 us: 1.12x slower                                                   |
| Geometric mean      | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_generate, xml_etree_process, tomli_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 16.3 ms: 1.07x slower                                                  |
| python_startup         | 22.4 ms                                                      | 27.4 ms: 1.22x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 27.4 ms: 1.16x faster                                                  |
| genshi_xml      | 72.1 ms                                                      | 66.2 ms: 1.09x faster                                                  |
| django_template | 44.3 ms                                                      | 46.8 ms: 1.06x slower                                                  |
| mako            | 15.9 ms                                                      | 17.9 ms: 1.12x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                   | 498 us                                                       | 327 us: 1.52x faster                                                   |
| async_tree_none            | 572 ms                                                       | 392 ms: 1.46x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 954 ms: 1.45x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 969 ms: 1.45x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 509 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 494 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 407 ms: 1.24x faster                                                   |
| telco                      | 12.2 ms                                                      | 9.90 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 708 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 738 ms: 1.20x faster                                                   |
| pylint                     | 470 ms                                                       | 393 ms: 1.20x faster                                                   |
| go                         | 191 ms                                                       | 162 ms: 1.18x faster                                                   |
| scimark_sor                | 179 ms                                                       | 153 ms: 1.17x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 43.0 us: 1.17x faster                                                  |
| spectral_norm              | 157 ms                                                       | 135 ms: 1.16x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 27.4 ms: 1.16x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.11 ms: 1.15x faster                                                  |
| thrift                     | 1.10 ms                                                      | 975 us: 1.13x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 157 ms: 1.13x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.67 us: 1.12x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.06 ms: 1.11x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 205 us: 1.10x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 191 ms: 1.10x faster                                                   |
| chaos                      | 83.6 ms                                                      | 76.8 ms: 1.09x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 66.2 ms: 1.09x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 213 ms: 1.09x faster                                                   |
| fannkuch                   | 547 ms                                                       | 509 ms: 1.08x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 927 ms: 1.07x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 722 ms: 1.06x faster                                                   |
| async_generators           | 567 ms                                                       | 537 ms: 1.06x faster                                                   |
| float                      | 116 ms                                                       | 110 ms: 1.05x faster                                                   |
| regex_compile              | 182 ms                                                       | 173 ms: 1.05x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 28.6 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 6.02 sec: 1.04x faster                                                 |
| json_dumps                 | 14.1 ms                                                      | 14.7 ms: 1.04x slower                                                  |
| django_template            | 44.3 ms                                                      | 46.8 ms: 1.06x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 8.59 ms: 1.06x slower                                                  |
| scimark_fft                | 473 ms                                                       | 503 ms: 1.06x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 79.3 ms: 1.06x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 16.3 ms: 1.07x slower                                                  |
| sqlite_synth               | 3.99 us                                                      | 4.28 us: 1.07x slower                                                  |
| json_loads                 | 34.3 us                                                      | 36.8 us: 1.07x slower                                                  |
| comprehensions             | 22.2 us                                                      | 24.1 us: 1.08x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 152 ms: 1.08x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 99.0 ms: 1.09x slower                                                  |
| 2to3                       | 445 ms                                                       | 489 ms: 1.10x slower                                                   |
| sympy_str                  | 379 ms                                                       | 419 ms: 1.11x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.44 ms: 1.11x slower                                                  |
| generators                 | 40.0 ms                                                      | 44.8 ms: 1.12x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 467 us: 1.12x slower                                                   |
| mako                       | 15.9 ms                                                      | 17.9 ms: 1.12x slower                                                  |
| json                       | 6.51 ms                                                      | 7.35 ms: 1.13x slower                                                  |
| sympy_expand               | 601 ms                                                       | 678 ms: 1.13x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 34.9 ms: 1.13x slower                                                  |
| logging_silent             | 130 ns                                                       | 148 ns: 1.14x slower                                                   |
| raytrace                   | 344 ms                                                       | 394 ms: 1.14x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 172 ms: 1.17x slower                                                   |
| coverage                   | 107 ms                                                       | 128 ms: 1.19x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 39.6 ms: 1.21x slower                                                  |
| python_startup             | 22.4 ms                                                      | 27.4 ms: 1.22x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.67 ms: 1.27x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.80 ms: 1.54x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.45 ms: 1.85x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 97.1 ms: 5.20x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (24): logging_simple, html5lib, richards, nqueens, xml_etree_generate, sqlglot_parse, pyflate, pprint_pformat, pycparser, xml_etree_process, tomli_loads, richards_super, nbody, mdp, crypto_pyaes, pidigits, unpickle_pure_python, logging_format, dulwich_log, sympy_integrate, docutils, regex_dna, deltablue, meteor_contest
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 99.88% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x