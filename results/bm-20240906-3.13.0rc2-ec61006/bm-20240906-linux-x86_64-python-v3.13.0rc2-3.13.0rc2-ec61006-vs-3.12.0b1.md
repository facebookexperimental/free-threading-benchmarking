# Results vs. 3.12.0b1

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.86x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 670 ms: 1.39x faster                                         |
| async_tree_none_tg         | 692 ms                                                                | 504 ms: 1.37x faster                                         |
| async_tree_memoization     | 949 ms                                                                | 709 ms: 1.34x faster                                         |
| async_tree_none            | 740 ms                                                                | 572 ms: 1.29x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 852 ms: 1.29x faster                                         |
| async_tree_io              | 1.79 sec                                                              | 1.39 sec: 1.29x faster                                       |
| async_tree_io_tg           | 1.80 sec                                                              | 1.40 sec: 1.29x faster                                       |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 889 ms: 1.28x faster                                         |
| async_generators           | 617 ms                                                                | 567 ms: 1.09x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.19x faster                                                 |

Benchmark hidden because not significant (4): asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 127 ms                                                                | 116 ms: 1.09x faster                                         |
| nbody          | 125 ms                                                                | 119 ms: 1.05x faster                                         |
| Geometric mean | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 197 ms                                                                | 182 ms: 1.08x faster                                         |
| regex_effbot   | 4.97 ms                                                               | 4.74 ms: 1.05x faster                                        |
| regex_v8       | 31.1 ms                                                               | 32.8 ms: 1.05x slower                                        |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                 |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| unpickle_pure_python | 319 us                                                                | 290 us: 1.10x faster                                         |
| unpickle_list        | 7.19 us                                                               | 6.68 us: 1.08x faster                                        |
| tomli_loads          | 2.99 sec                                                              | 2.78 sec: 1.07x faster                                       |
| pickle_pure_python   | 447 us                                                                | 416 us: 1.07x faster                                         |
| json_loads           | 36.6 us                                                               | 34.3 us: 1.07x faster                                        |
| xml_etree_generate   | 128 ms                                                                | 122 ms: 1.05x faster                                         |
| json_dumps           | 13.6 ms                                                               | 14.1 ms: 1.04x slower                                        |
| pickle_list          | 6.40 us                                                               | 6.86 us: 1.07x slower                                        |
| xml_etree_iterparse  | 157 ms                                                                | 177 ms: 1.12x slower                                         |
| Geometric mean       | (ref)                                                                 | 1.01x faster                                                 |

Benchmark hidden because not significant (5): xml_etree_process, xml_etree_parse, pickle_dict, pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 15.3 ms: 1.06x faster                                        |
| python_startup         | 21.2 ms                                                               | 22.4 ms: 1.05x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 48.6 ms                                                               | 44.3 ms: 1.10x faster                                        |
| mako            | 17.2 ms                                                               | 15.9 ms: 1.08x faster                                        |
| Geometric mean  | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 670 ms: 1.39x faster                                         |
| async_tree_none_tg         | 692 ms                                                                | 504 ms: 1.37x faster                                         |
| async_tree_memoization     | 949 ms                                                                | 709 ms: 1.34x faster                                         |
| comprehensions             | 29.6 us                                                               | 22.2 us: 1.33x faster                                        |
| async_tree_none            | 740 ms                                                                | 572 ms: 1.29x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 852 ms: 1.29x faster                                         |
| async_tree_io              | 1.79 sec                                                              | 1.39 sec: 1.29x faster                                       |
| async_tree_io_tg           | 1.80 sec                                                              | 1.40 sec: 1.29x faster                                       |
| logging_format             | 11.8 us                                                               | 9.24 us: 1.28x faster                                        |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 889 ms: 1.28x faster                                         |
| dulwich_log                | 114 ms                                                                | 93.7 ms: 1.22x faster                                        |
| raytrace                   | 418 ms                                                                | 344 ms: 1.21x faster                                         |
| logging_simple             | 9.89 us                                                               | 8.56 us: 1.16x faster                                        |
| generators                 | 46.0 ms                                                               | 40.0 ms: 1.15x faster                                        |
| sympy_expand               | 689 ms                                                                | 601 ms: 1.15x faster                                         |
| deepcopy_memo              | 57.5 us                                                               | 50.1 us: 1.15x faster                                        |
| deltablue                  | 5.05 ms                                                               | 4.44 ms: 1.14x faster                                        |
| sympy_str                  | 425 ms                                                                | 379 ms: 1.12x faster                                         |
| chaos                      | 93.7 ms                                                               | 83.6 ms: 1.12x faster                                        |
| crypto_pyaes               | 112 ms                                                                | 100 ms: 1.12x faster                                         |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.76 ms: 1.11x faster                                        |
| pycparser                  | 1.73 sec                                                              | 1.57 sec: 1.10x faster                                       |
| unpickle_pure_python       | 319 us                                                                | 290 us: 1.10x faster                                         |
| django_template            | 48.6 ms                                                               | 44.3 ms: 1.10x faster                                        |
| float                      | 127 ms                                                                | 116 ms: 1.09x faster                                         |
| hexiom                     | 8.87 ms                                                               | 8.11 ms: 1.09x faster                                        |
| sympy_sum                  | 229 ms                                                                | 210 ms: 1.09x faster                                         |
| scimark_monte_carlo        | 98.5 ms                                                               | 90.6 ms: 1.09x faster                                        |
| async_generators           | 617 ms                                                                | 567 ms: 1.09x faster                                         |
| deepcopy_reduce            | 4.45 us                                                               | 4.10 us: 1.09x faster                                        |
| regex_compile              | 197 ms                                                                | 182 ms: 1.08x faster                                         |
| mako                       | 17.2 ms                                                               | 15.9 ms: 1.08x faster                                        |
| sqlglot_parse              | 1.89 ms                                                               | 1.76 ms: 1.08x faster                                        |
| unpickle_list              | 7.19 us                                                               | 6.68 us: 1.08x faster                                        |
| tomli_loads                | 2.99 sec                                                              | 2.78 sec: 1.07x faster                                       |
| pickle_pure_python         | 447 us                                                                | 416 us: 1.07x faster                                         |
| json_loads                 | 36.6 us                                                               | 34.3 us: 1.07x faster                                        |
| thrift                     | 1.17 ms                                                               | 1.10 ms: 1.07x faster                                        |
| pathlib                    | 31.7 ms                                                               | 29.9 ms: 1.06x faster                                        |
| python_startup_no_site     | 16.3 ms                                                               | 15.3 ms: 1.06x faster                                        |
| sqlglot_normalize          | 148 ms                                                                | 140 ms: 1.06x faster                                         |
| scimark_lu                 | 155 ms                                                                | 146 ms: 1.06x faster                                         |
| scimark_fft                | 499 ms                                                                | 473 ms: 1.05x faster                                         |
| bpe_tokeniser              | 6.63 sec                                                              | 6.28 sec: 1.05x faster                                       |
| nbody                      | 125 ms                                                                | 119 ms: 1.05x faster                                         |
| xml_etree_generate         | 128 ms                                                                | 122 ms: 1.05x faster                                         |
| dask                       | 924 ms                                                                | 881 ms: 1.05x faster                                         |
| regex_effbot               | 4.97 ms                                                               | 4.74 ms: 1.05x faster                                        |
| pprint_pformat             | 2.03 sec                                                              | 1.94 sec: 1.04x faster                                       |
| logging_silent             | 135 ns                                                                | 130 ns: 1.04x faster                                         |
| json_dumps                 | 13.6 ms                                                               | 14.1 ms: 1.04x slower                                        |
| scimark_sor                | 171 ms                                                                | 179 ms: 1.04x slower                                         |
| regex_v8                   | 31.1 ms                                                               | 32.8 ms: 1.05x slower                                        |
| python_startup             | 21.2 ms                                                               | 22.4 ms: 1.05x slower                                        |
| aiohttp                    | 1.92 ms                                                               | 2.03 ms: 1.06x slower                                        |
| sqlite_synth               | 3.75 us                                                               | 3.99 us: 1.06x slower                                        |
| pickle_list                | 6.40 us                                                               | 6.86 us: 1.07x slower                                        |
| richards_super             | 67.9 ms                                                               | 73.2 ms: 1.08x slower                                        |
| unpack_sequence            | 68.5 ns                                                               | 74.3 ns: 1.09x slower                                        |
| coverage                   | 97.6 ms                                                               | 107 ms: 1.10x slower                                         |
| xml_etree_iterparse        | 157 ms                                                                | 177 ms: 1.12x slower                                         |
| typing_runtime_protocols   | 199 us                                                                | 226 us: 1.13x slower                                         |
| flaskblogging              | 6.74 ms                                                               | 7.68 ms: 1.14x slower                                        |
| create_gc_cycles           | 2.02 ms                                                               | 2.41 ms: 1.19x slower                                        |
| telco                      | 9.71 ms                                                               | 12.2 ms: 1.25x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (37): bench_thread_pool, pylint, tornado_http, sqlglot_transpile, sympy_integrate, html5lib, gunicorn, json, sqlglot_optimize, genshi_xml, regex_dna, pidigits, docutils, deepcopy, mdp, asyncio_tcp, asyncio_tcp_ssl, genshi_text, fannkuch, spectral_norm, asyncio_websockets, xml_etree_process, 2to3, pyflate, chameleon, xml_etree_parse, meteor_contest, pickle_dict, nqueens, gc_traversal, pprint_safe_repr, bench_mp_pool, pickle, coroutines, richards, go, unpickle
Ignored benchmarks (3) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.86x