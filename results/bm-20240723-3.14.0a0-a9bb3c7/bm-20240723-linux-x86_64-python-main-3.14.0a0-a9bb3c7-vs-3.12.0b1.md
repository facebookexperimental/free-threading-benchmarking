# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.88x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 410 ms: 1.08x faster                                  |
| docutils       | 4.06 sec                                                              | 3.93 sec: 1.03x faster                                |
| html5lib       | 95.8 ms                                                               | 88.8 ms: 1.08x faster                                 |
| Geometric mean | (ref)                                                                 | 1.06x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 584 ms: 1.60x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 464 ms: 1.49x faster                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.24 sec: 1.45x faster                                |
| async_tree_memoization     | 949 ms                                                                | 671 ms: 1.41x faster                                  |
| async_tree_none            | 740 ms                                                                | 531 ms: 1.39x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.28 sec: 1.39x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 821 ms: 1.38x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 818 ms: 1.34x faster                                  |
| async_generators           | 617 ms                                                                | 570 ms: 1.08x faster                                  |
| Geometric mean             | (ref)                                                                 | 1.26x faster                                          |

Benchmark hidden because not significant (4): asyncio_websockets, coroutines, asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 127 ms                                                                | 115 ms: 1.10x faster                                  |
| nbody          | 125 ms                                                                | 114 ms: 1.09x faster                                  |
| pidigits       | 255 ms                                                                | 240 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                                 | 1.08x faster                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 197 ms                                                                | 182 ms: 1.08x faster                                  |
| regex_v8       | 31.1 ms                                                               | 32.9 ms: 1.06x slower                                 |
| Geometric mean | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| tomli_loads          | 2.99 sec                                                              | 2.68 sec: 1.12x faster                                |
| xml_etree_generate   | 128 ms                                                                | 116 ms: 1.11x faster                                  |
| unpickle_pure_python | 319 us                                                                | 294 us: 1.08x faster                                  |
| pickle_pure_python   | 447 us                                                                | 419 us: 1.07x faster                                  |
| xml_etree_parse      | 230 ms                                                                | 216 ms: 1.06x faster                                  |
| unpickle_list        | 7.19 us                                                               | 6.79 us: 1.06x faster                                 |
| json_loads           | 36.6 us                                                               | 37.9 us: 1.04x slower                                 |
| pickle               | 14.8 us                                                               | 15.8 us: 1.07x slower                                 |
| json_dumps           | 13.6 ms                                                               | 14.8 ms: 1.09x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.02x faster                                          |

Benchmark hidden because not significant (5): pickle_dict, xml_etree_process, pickle_list, unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 14.8 ms: 1.10x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 48.6 ms                                                               | 45.4 ms: 1.07x faster                                 |
| genshi_xml      | 73.6 ms                                                               | 69.7 ms: 1.06x faster                                 |
| Geometric mean  | (ref)                                                                 | 1.05x faster                                          |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 584 ms: 1.60x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 464 ms: 1.49x faster                                  |
| deepcopy_memo              | 57.5 us                                                               | 38.7 us: 1.48x faster                                 |
| async_tree_io_tg           | 1.80 sec                                                              | 1.24 sec: 1.45x faster                                |
| async_tree_memoization     | 949 ms                                                                | 671 ms: 1.41x faster                                  |
| async_tree_none            | 740 ms                                                                | 531 ms: 1.39x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.28 sec: 1.39x faster                                |
| deepcopy                   | 503 us                                                                | 361 us: 1.39x faster                                  |
| comprehensions             | 29.6 us                                                               | 21.3 us: 1.39x faster                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 821 ms: 1.38x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 818 ms: 1.34x faster                                  |
| logging_format             | 11.8 us                                                               | 9.35 us: 1.26x faster                                 |
| raytrace                   | 418 ms                                                                | 339 ms: 1.23x faster                                  |
| generators                 | 46.0 ms                                                               | 38.3 ms: 1.20x faster                                 |
| deepcopy_reduce            | 4.45 us                                                               | 3.71 us: 1.20x faster                                 |
| logging_simple             | 9.89 us                                                               | 8.31 us: 1.19x faster                                 |
| dulwich_log                | 114 ms                                                                | 95.9 ms: 1.19x faster                                 |
| sympy_str                  | 425 ms                                                                | 360 ms: 1.18x faster                                  |
| deltablue                  | 5.05 ms                                                               | 4.31 ms: 1.17x faster                                 |
| chaos                      | 93.7 ms                                                               | 81.6 ms: 1.15x faster                                 |
| thrift                     | 1.17 ms                                                               | 1.03 ms: 1.14x faster                                 |
| sympy_expand               | 689 ms                                                                | 605 ms: 1.14x faster                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.65 ms: 1.12x faster                                 |
| tomli_loads                | 2.99 sec                                                              | 2.68 sec: 1.12x faster                                |
| scimark_monte_carlo        | 98.5 ms                                                               | 88.4 ms: 1.11x faster                                 |
| pathlib                    | 31.7 ms                                                               | 28.6 ms: 1.11x faster                                 |
| xml_etree_generate         | 128 ms                                                                | 116 ms: 1.11x faster                                  |
| pycparser                  | 1.73 sec                                                              | 1.57 sec: 1.10x faster                                |
| crypto_pyaes               | 112 ms                                                                | 102 ms: 1.10x faster                                  |
| sqlglot_parse              | 1.89 ms                                                               | 1.72 ms: 1.10x faster                                 |
| float                      | 127 ms                                                                | 115 ms: 1.10x faster                                  |
| python_startup_no_site     | 16.3 ms                                                               | 14.8 ms: 1.10x faster                                 |
| nbody                      | 125 ms                                                                | 114 ms: 1.09x faster                                  |
| unpickle_pure_python       | 319 us                                                                | 294 us: 1.08x faster                                  |
| async_generators           | 617 ms                                                                | 570 ms: 1.08x faster                                  |
| 2to3                       | 444 ms                                                                | 410 ms: 1.08x faster                                  |
| regex_compile              | 197 ms                                                                | 182 ms: 1.08x faster                                  |
| html5lib                   | 95.8 ms                                                               | 88.8 ms: 1.08x faster                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 6.17 sec: 1.07x faster                                |
| sympy_integrate            | 31.4 ms                                                               | 29.2 ms: 1.07x faster                                 |
| sympy_sum                  | 229 ms                                                                | 214 ms: 1.07x faster                                  |
| logging_silent             | 135 ns                                                                | 126 ns: 1.07x faster                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 2.13 ms: 1.07x faster                                 |
| django_template            | 48.6 ms                                                               | 45.4 ms: 1.07x faster                                 |
| hexiom                     | 8.87 ms                                                               | 8.31 ms: 1.07x faster                                 |
| pickle_pure_python         | 447 us                                                                | 419 us: 1.07x faster                                  |
| mdp                        | 3.84 sec                                                              | 3.61 sec: 1.06x faster                                |
| dask                       | 924 ms                                                                | 868 ms: 1.06x faster                                  |
| xml_etree_parse            | 230 ms                                                                | 216 ms: 1.06x faster                                  |
| pidigits                   | 255 ms                                                                | 240 ms: 1.06x faster                                  |
| unpickle_list              | 7.19 us                                                               | 6.79 us: 1.06x faster                                 |
| genshi_xml                 | 73.6 ms                                                               | 69.7 ms: 1.06x faster                                 |
| pprint_pformat             | 2.03 sec                                                              | 1.92 sec: 1.05x faster                                |
| richards                   | 63.4 ms                                                               | 60.4 ms: 1.05x faster                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 73.2 ms: 1.04x faster                                 |
| scimark_fft                | 499 ms                                                                | 478 ms: 1.04x faster                                  |
| docutils                   | 4.06 sec                                                              | 3.93 sec: 1.03x faster                                |
| json_loads                 | 36.6 us                                                               | 37.9 us: 1.04x slower                                 |
| typing_runtime_protocols   | 199 us                                                                | 210 us: 1.05x slower                                  |
| regex_v8                   | 31.1 ms                                                               | 32.9 ms: 1.06x slower                                 |
| pickle                     | 14.8 us                                                               | 15.8 us: 1.07x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 14.8 ms: 1.09x slower                                 |
| bench_thread_pool          | 3.11 ms                                                               | 3.42 ms: 1.10x slower                                 |
| bench_mp_pool              | 18.4 ms                                                               | 20.3 ms: 1.10x slower                                 |
| create_gc_cycles           | 2.02 ms                                                               | 2.27 ms: 1.12x slower                                 |
| unpack_sequence            | 68.5 ns                                                               | 78.4 ns: 1.15x slower                                 |
| telco                      | 9.71 ms                                                               | 11.1 ms: 1.15x slower                                 |
| json                       | 6.68 ms                                                               | 7.74 ms: 1.16x slower                                 |
| coverage                   | 97.6 ms                                                               | 126 ms: 1.29x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.08x faster                                          |

Benchmark hidden because not significant (29): tornado_http, pylint, mako, pickle_dict, nqueens, fannkuch, xml_etree_process, regex_effbot, genshi_text, pickle_list, pprint_safe_repr, meteor_contest, asyncio_websockets, sqlite_synth, coroutines, regex_dna, asyncio_tcp, scimark_lu, python_startup, sqlglot_normalize, gc_traversal, scimark_sor, asyncio_tcp_ssl, richards_super, pyflate, unpickle, xml_etree_iterparse, go, spectral_norm
Ignored benchmarks (7) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.88x