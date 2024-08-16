# Results vs. 3.12.0b1

- fork: python
- ref: 3.13
- machine: linux-x86_64
- commit hash: 79452b1
- commit date: 2024-08-14
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.86x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| chameleon      | 9.30 ms                                                               | 9.84 ms: 1.06x slower                                   |
| Geometric mean | (ref)                                                                 | 1.00x slower                                            |

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 672 ms: 1.39x faster                                    |
| async_tree_none_tg         | 692 ms                                                                | 521 ms: 1.33x faster                                    |
| async_tree_io              | 1.79 sec                                                              | 1.38 sec: 1.30x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 849 ms: 1.30x faster                                    |
| async_tree_none            | 740 ms                                                                | 576 ms: 1.28x faster                                    |
| async_tree_memoization     | 949 ms                                                                | 745 ms: 1.27x faster                                    |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 899 ms: 1.26x faster                                    |
| async_tree_io_tg           | 1.80 sec                                                              | 1.46 sec: 1.24x faster                                  |
| async_generators           | 617 ms                                                                | 592 ms: 1.04x faster                                    |
| Geometric mean             | (ref)                                                                 | 1.18x faster                                            |

Benchmark hidden because not significant (4): coroutines, asyncio_tcp_ssl, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| float          | 127 ms                                                                | 115 ms: 1.10x faster                                    |
| Geometric mean | (ref)                                                                 | 1.05x faster                                            |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| regex_compile  | 197 ms                                                                | 177 ms: 1.11x faster                                    |
| regex_v8       | 31.1 ms                                                               | 32.4 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                                 | 1.02x faster                                            |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| unpickle_list        | 7.19 us                                                               | 6.67 us: 1.08x faster                                   |
| unpickle_pure_python | 319 us                                                                | 296 us: 1.08x faster                                    |
| pickle_pure_python   | 447 us                                                                | 417 us: 1.07x faster                                    |
| tomli_loads          | 2.99 sec                                                              | 2.80 sec: 1.07x faster                                  |
| pickle               | 14.8 us                                                               | 15.4 us: 1.04x slower                                   |
| pickle_list          | 6.40 us                                                               | 6.82 us: 1.07x slower                                   |
| unpickle             | 19.7 us                                                               | 21.4 us: 1.08x slower                                   |
| json_dumps           | 13.6 ms                                                               | 14.9 ms: 1.10x slower                                   |
| xml_etree_iterparse  | 157 ms                                                                | 176 ms: 1.12x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                            |

Benchmark hidden because not significant (5): json_loads, pickle_dict, xml_etree_generate, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 14.6 ms: 1.11x faster                                   |
| python_startup         | 21.2 ms                                                               | 22.0 ms: 1.04x slower                                   |
| Geometric mean         | (ref)                                                                 | 1.03x faster                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| genshi_xml     | 73.6 ms                                                               | 68.3 ms: 1.08x faster                                   |
| mako           | 17.2 ms                                                               | 16.1 ms: 1.07x faster                                   |
| Geometric mean | (ref)                                                                 | 1.05x faster                                            |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------------|:---------------------------------------------------------------------:|:-------------------------------------------------------:|
| comprehensions             | 29.6 us                                                               | 20.9 us: 1.41x faster                                   |
| async_tree_memoization_tg  | 935 ms                                                                | 672 ms: 1.39x faster                                    |
| async_tree_none_tg         | 692 ms                                                                | 521 ms: 1.33x faster                                    |
| async_tree_io              | 1.79 sec                                                              | 1.38 sec: 1.30x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 849 ms: 1.30x faster                                    |
| async_tree_none            | 740 ms                                                                | 576 ms: 1.28x faster                                    |
| async_tree_memoization     | 949 ms                                                                | 745 ms: 1.27x faster                                    |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 899 ms: 1.26x faster                                    |
| logging_format             | 11.8 us                                                               | 9.48 us: 1.25x faster                                   |
| async_tree_io_tg           | 1.80 sec                                                              | 1.46 sec: 1.24x faster                                  |
| raytrace                   | 418 ms                                                                | 350 ms: 1.19x faster                                    |
| generators                 | 46.0 ms                                                               | 39.2 ms: 1.18x faster                                   |
| sympy_str                  | 425 ms                                                                | 367 ms: 1.16x faster                                    |
| dulwich_log                | 114 ms                                                                | 100.0 ms: 1.14x faster                                  |
| crypto_pyaes               | 112 ms                                                                | 99.8 ms: 1.12x faster                                   |
| deepcopy_memo              | 57.5 us                                                               | 51.7 us: 1.11x faster                                   |
| regex_compile              | 197 ms                                                                | 177 ms: 1.11x faster                                    |
| python_startup_no_site     | 16.3 ms                                                               | 14.6 ms: 1.11x faster                                   |
| deltablue                  | 5.05 ms                                                               | 4.56 ms: 1.11x faster                                   |
| chaos                      | 93.7 ms                                                               | 84.7 ms: 1.11x faster                                   |
| pycparser                  | 1.73 sec                                                              | 1.57 sec: 1.10x faster                                  |
| float                      | 127 ms                                                                | 115 ms: 1.10x faster                                    |
| logging_simple             | 9.89 us                                                               | 8.98 us: 1.10x faster                                   |
| scimark_monte_carlo        | 98.5 ms                                                               | 89.9 ms: 1.10x faster                                   |
| sympy_expand               | 689 ms                                                                | 631 ms: 1.09x faster                                    |
| pathlib                    | 31.7 ms                                                               | 29.3 ms: 1.08x faster                                   |
| unpickle_list              | 7.19 us                                                               | 6.67 us: 1.08x faster                                   |
| unpickle_pure_python       | 319 us                                                                | 296 us: 1.08x faster                                    |
| genshi_xml                 | 73.6 ms                                                               | 68.3 ms: 1.08x faster                                   |
| sympy_sum                  | 229 ms                                                                | 213 ms: 1.07x faster                                    |
| pickle_pure_python         | 447 us                                                                | 417 us: 1.07x faster                                    |
| mako                       | 17.2 ms                                                               | 16.1 ms: 1.07x faster                                   |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.98 ms: 1.07x faster                                   |
| tomli_loads                | 2.99 sec                                                              | 2.80 sec: 1.07x faster                                  |
| hexiom                     | 8.87 ms                                                               | 8.35 ms: 1.06x faster                                   |
| bpe_tokeniser              | 6.63 sec                                                              | 6.25 sec: 1.06x faster                                  |
| dask                       | 924 ms                                                                | 872 ms: 1.06x faster                                    |
| sympy_integrate            | 31.4 ms                                                               | 29.7 ms: 1.06x faster                                   |
| sqlglot_parse              | 1.89 ms                                                               | 1.80 ms: 1.05x faster                                   |
| scimark_fft                | 499 ms                                                                | 477 ms: 1.05x faster                                    |
| deepcopy_reduce            | 4.45 us                                                               | 4.27 us: 1.04x faster                                   |
| async_generators           | 617 ms                                                                | 592 ms: 1.04x faster                                    |
| logging_silent             | 135 ns                                                                | 130 ns: 1.04x faster                                    |
| deepcopy                   | 503 us                                                                | 484 us: 1.04x faster                                    |
| pickle                     | 14.8 us                                                               | 15.4 us: 1.04x slower                                   |
| python_startup             | 21.2 ms                                                               | 22.0 ms: 1.04x slower                                   |
| regex_v8                   | 31.1 ms                                                               | 32.4 ms: 1.04x slower                                   |
| gc_traversal               | 5.61 ms                                                               | 5.91 ms: 1.05x slower                                   |
| meteor_contest             | 149 ms                                                                | 157 ms: 1.06x slower                                    |
| go                         | 185 ms                                                                | 195 ms: 1.06x slower                                    |
| chameleon                  | 9.30 ms                                                               | 9.84 ms: 1.06x slower                                   |
| pickle_list                | 6.40 us                                                               | 6.82 us: 1.07x slower                                   |
| unpack_sequence            | 68.5 ns                                                               | 73.9 ns: 1.08x slower                                   |
| unpickle                   | 19.7 us                                                               | 21.4 us: 1.08x slower                                   |
| typing_runtime_protocols   | 199 us                                                                | 216 us: 1.08x slower                                    |
| sqlite_synth               | 3.75 us                                                               | 4.07 us: 1.09x slower                                   |
| json_dumps                 | 13.6 ms                                                               | 14.9 ms: 1.10x slower                                   |
| xml_etree_iterparse        | 157 ms                                                                | 176 ms: 1.12x slower                                    |
| richards_super             | 67.9 ms                                                               | 76.3 ms: 1.12x slower                                   |
| coverage                   | 97.6 ms                                                               | 110 ms: 1.13x slower                                    |
| gunicorn                   | 1.98 ms                                                               | 2.25 ms: 1.14x slower                                   |
| aiohttp                    | 1.92 ms                                                               | 2.23 ms: 1.16x slower                                   |
| telco                      | 9.71 ms                                                               | 11.4 ms: 1.17x slower                                   |
| create_gc_cycles           | 2.02 ms                                                               | 2.46 ms: 1.22x slower                                   |
| flaskblogging              | 6.74 ms                                                               | 8.78 ms: 1.30x slower                                   |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                            |

Benchmark hidden because not significant (37): pylint, tornado_http, thrift, django_template, coroutines, pidigits, regex_effbot, json, nqueens, sqlglot_normalize, pprint_pformat, bench_thread_pool, docutils, fannkuch, mdp, json_loads, pprint_safe_repr, nbody, 2to3, genshi_text, scimark_lu, sqlglot_optimize, asyncio_tcp_ssl, pickle_dict, pyflate, regex_dna, scimark_sor, xml_etree_generate, sqlglot_transpile, asyncio_websockets, spectral_norm, xml_etree_process, html5lib, xml_etree_parse, asyncio_tcp, richards, bench_mp_pool
Ignored benchmarks (3) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.86x