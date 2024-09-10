# Results vs. 3.12.0b1

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.02x faster
- HPT reliability: 86.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.89x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.06 sec                                                              | 4.22 sec: 1.04x slower                                                |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 949 ms                                                                | 647 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 643 ms: 1.45x faster                                                  |
| async_tree_none            | 740 ms                                                                | 523 ms: 1.41x faster                                                  |
| async_tree_none_tg         | 692 ms                                                                | 494 ms: 1.40x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.33 sec: 1.36x faster                                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 893 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 875 ms: 1.26x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.42 sec: 1.25x faster                                                |
| async_generators           | 617 ms                                                                | 591 ms: 1.04x faster                                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.90 sec: 1.04x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.21x faster                                                          |

Benchmark hidden because not significant (3): coroutines, asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 5.19 ms: 1.04x slower                                                 |
| regex_dna      | 287 ms                                                                | 310 ms: 1.08x slower                                                  |
| regex_v8       | 31.1 ms                                                               | 36.2 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.06x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.99 sec                                                              | 2.72 sec: 1.10x faster                                                |
| pickle_pure_python   | 447 us                                                                | 418 us: 1.07x faster                                                  |
| unpickle_pure_python | 319 us                                                                | 299 us: 1.07x faster                                                  |
| json_loads           | 36.6 us                                                               | 37.8 us: 1.03x slower                                                 |
| pickle               | 14.8 us                                                               | 15.5 us: 1.05x slower                                                 |
| xml_etree_parse      | 230 ms                                                                | 253 ms: 1.10x slower                                                  |
| pickle_list          | 6.40 us                                                               | 7.25 us: 1.13x slower                                                 |
| json_dumps           | 13.6 ms                                                               | 15.4 ms: 1.13x slower                                                 |
| xml_etree_iterparse  | 157 ms                                                                | 182 ms: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.03x slower                                                          |

Benchmark hidden because not significant (5): pickle_dict, xml_etree_generate, unpickle_list, xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 17.7 ms: 1.09x slower                                                 |
| python_startup         | 21.2 ms                                                               | 26.1 ms: 1.23x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 17.2 ms                                                               | 18.5 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (3): django_template, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 949 ms                                                                | 647 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 643 ms: 1.45x faster                                                  |
| deepcopy_memo              | 57.5 us                                                               | 39.5 us: 1.45x faster                                                 |
| async_tree_none            | 740 ms                                                                | 523 ms: 1.41x faster                                                  |
| async_tree_none_tg         | 692 ms                                                                | 494 ms: 1.40x faster                                                  |
| deepcopy                   | 503 us                                                                | 362 us: 1.39x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.33 sec: 1.36x faster                                                |
| comprehensions             | 29.6 us                                                               | 22.1 us: 1.34x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 893 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 875 ms: 1.26x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.42 sec: 1.25x faster                                                |
| logging_format             | 11.8 us                                                               | 9.69 us: 1.22x faster                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.13 ms: 1.22x faster                                                 |
| crypto_pyaes               | 112 ms                                                                | 95.7 ms: 1.17x faster                                                 |
| raytrace                   | 418 ms                                                                | 358 ms: 1.17x faster                                                  |
| logging_simple             | 9.89 us                                                               | 8.60 us: 1.15x faster                                                 |
| chaos                      | 93.7 ms                                                               | 83.6 ms: 1.12x faster                                                 |
| generators                 | 46.0 ms                                                               | 41.1 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 89.4 ms: 1.10x faster                                                 |
| go                         | 185 ms                                                                | 168 ms: 1.10x faster                                                  |
| tomli_loads                | 2.99 sec                                                              | 2.72 sec: 1.10x faster                                                |
| deepcopy_reduce            | 4.45 us                                                               | 4.09 us: 1.09x faster                                                 |
| sympy_expand               | 689 ms                                                                | 635 ms: 1.09x faster                                                  |
| sympy_sum                  | 229 ms                                                                | 211 ms: 1.08x faster                                                  |
| pickle_pure_python         | 447 us                                                                | 418 us: 1.07x faster                                                  |
| unpickle_pure_python       | 319 us                                                                | 299 us: 1.07x faster                                                  |
| scimark_fft                | 499 ms                                                                | 470 ms: 1.06x faster                                                  |
| sympy_integrate            | 31.4 ms                                                               | 29.9 ms: 1.05x faster                                                 |
| async_generators           | 617 ms                                                                | 591 ms: 1.04x faster                                                  |
| scimark_lu                 | 155 ms                                                                | 149 ms: 1.04x faster                                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 6.41 sec: 1.03x faster                                                |
| pprint_safe_repr           | 970 ms                                                                | 1.00 sec: 1.03x slower                                                |
| json_loads                 | 36.6 us                                                               | 37.8 us: 1.03x slower                                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.90 sec: 1.04x slower                                                |
| docutils                   | 4.06 sec                                                              | 4.22 sec: 1.04x slower                                                |
| regex_effbot               | 4.97 ms                                                               | 5.19 ms: 1.04x slower                                                 |
| richards_super             | 67.9 ms                                                               | 71.0 ms: 1.05x slower                                                 |
| pickle                     | 14.8 us                                                               | 15.5 us: 1.05x slower                                                 |
| unpack_sequence            | 68.5 ns                                                               | 72.4 ns: 1.06x slower                                                 |
| logging_silent             | 135 ns                                                                | 143 ns: 1.06x slower                                                  |
| sqlite_synth               | 3.75 us                                                               | 4.03 us: 1.07x slower                                                 |
| mako                       | 17.2 ms                                                               | 18.5 ms: 1.07x slower                                                 |
| json                       | 6.68 ms                                                               | 7.18 ms: 1.08x slower                                                 |
| regex_dna                  | 287 ms                                                                | 310 ms: 1.08x slower                                                  |
| python_startup_no_site     | 16.3 ms                                                               | 17.7 ms: 1.09x slower                                                 |
| xml_etree_parse            | 230 ms                                                                | 253 ms: 1.10x slower                                                  |
| gc_traversal               | 5.61 ms                                                               | 6.19 ms: 1.10x slower                                                 |
| pyflate                    | 661 ms                                                                | 735 ms: 1.11x slower                                                  |
| pickle_list                | 6.40 us                                                               | 7.25 us: 1.13x slower                                                 |
| json_dumps                 | 13.6 ms                                                               | 15.4 ms: 1.13x slower                                                 |
| xml_etree_iterparse        | 157 ms                                                                | 182 ms: 1.16x slower                                                  |
| typing_runtime_protocols   | 199 us                                                                | 231 us: 1.16x slower                                                  |
| regex_v8                   | 31.1 ms                                                               | 36.2 ms: 1.16x slower                                                 |
| telco                      | 9.71 ms                                                               | 11.5 ms: 1.19x slower                                                 |
| python_startup             | 21.2 ms                                                               | 26.1 ms: 1.23x slower                                                 |
| coverage                   | 97.6 ms                                                               | 121 ms: 1.24x slower                                                  |
| bench_thread_pool          | 3.11 ms                                                               | 3.89 ms: 1.25x slower                                                 |
| create_gc_cycles           | 2.02 ms                                                               | 2.70 ms: 1.34x slower                                                 |
| bench_mp_pool              | 18.4 ms                                                               | 26.6 ms: 1.45x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (38): dulwich_log, sympy_str, deltablue, regex_compile, django_template, pathlib, genshi_text, pprint_pformat, pickle_dict, genshi_xml, html5lib, sqlglot_parse, float, coroutines, pidigits, xml_etree_generate, unpickle_list, thrift, sqlglot_transpile, tornado_http, sqlglot_optimize, scimark_sor, xml_etree_process, pylint, asyncio_tcp, 2to3, spectral_norm, asyncio_websockets, mdp, sqlglot_normalize, meteor_contest, fannkuch, pycparser, nqueens, nbody, hexiom, richards, unpickle
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 86.10% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.89x