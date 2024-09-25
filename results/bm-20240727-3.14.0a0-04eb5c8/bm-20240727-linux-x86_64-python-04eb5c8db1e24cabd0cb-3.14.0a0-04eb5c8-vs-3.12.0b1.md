# Results vs. 3.12.0b1

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.89x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.06 sec                                                              | 3.95 sec: 1.03x faster                                                |
| tornado_http   | 262 ms                                                                | 228 ms: 1.15x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.06x faster                                                          |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 591 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 692 ms                                                                | 451 ms: 1.53x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 626 ms: 1.52x faster                                                  |
| async_tree_none            | 740 ms                                                                | 499 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.22 sec: 1.48x faster                                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 794 ms: 1.43x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.26 sec: 1.42x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 806 ms: 1.36x faster                                                  |
| async_generators           | 617 ms                                                                | 580 ms: 1.06x faster                                                  |
| coroutines                 | 30.1 ms                                                               | 31.6 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.28x faster                                                          |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 127 ms                                                                | 112 ms: 1.13x faster                                                  |
| nbody          | 125 ms                                                                | 118 ms: 1.06x faster                                                  |
| pidigits       | 255 ms                                                                | 243 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 197 ms                                                                | 174 ms: 1.13x faster                                                  |
| regex_effbot   | 4.97 ms                                                               | 4.78 ms: 1.04x faster                                                 |
| regex_v8       | 31.1 ms                                                               | 35.8 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|--------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads        | 2.99 sec                                                              | 2.66 sec: 1.12x faster                                                |
| xml_etree_generate | 128 ms                                                                | 117 ms: 1.10x faster                                                  |
| xml_etree_process  | 85.7 ms                                                               | 81.3 ms: 1.05x faster                                                 |
| pickle             | 14.8 us                                                               | 15.6 us: 1.05x slower                                                 |
| json_dumps         | 13.6 ms                                                               | 15.5 ms: 1.14x slower                                                 |
| Geometric mean     | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (9): unpickle_pure_python, pickle_pure_python, pickle_list, xml_etree_parse, xml_etree_iterparse, unpickle_list, unpickle, pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 15.0 ms: 1.08x faster                                                 |
| python_startup         | 21.2 ms                                                               | 22.1 ms: 1.04x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.02x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 48.6 ms                                                               | 44.0 ms: 1.10x faster                                                 |
| mako            | 17.2 ms                                                               | 16.3 ms: 1.05x faster                                                 |
| genshi_text     | 31.9 ms                                                               | 30.2 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.05x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 935 ms                                                                | 591 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 692 ms                                                                | 451 ms: 1.53x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 626 ms: 1.52x faster                                                  |
| deepcopy_memo              | 57.5 us                                                               | 38.4 us: 1.50x faster                                                 |
| async_tree_none            | 740 ms                                                                | 499 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.22 sec: 1.48x faster                                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 794 ms: 1.43x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.26 sec: 1.42x faster                                                |
| comprehensions             | 29.6 us                                                               | 20.9 us: 1.42x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 806 ms: 1.36x faster                                                  |
| deepcopy                   | 503 us                                                                | 372 us: 1.35x faster                                                  |
| logging_format             | 11.8 us                                                               | 8.93 us: 1.32x faster                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 5.99 ms: 1.25x faster                                                 |
| logging_simple             | 9.89 us                                                               | 7.95 us: 1.24x faster                                                 |
| raytrace                   | 418 ms                                                                | 338 ms: 1.24x faster                                                  |
| sympy_str                  | 425 ms                                                                | 345 ms: 1.23x faster                                                  |
| deltablue                  | 5.05 ms                                                               | 4.11 ms: 1.23x faster                                                 |
| deepcopy_reduce            | 4.45 us                                                               | 3.64 us: 1.22x faster                                                 |
| pathlib                    | 31.7 ms                                                               | 26.6 ms: 1.19x faster                                                 |
| chaos                      | 93.7 ms                                                               | 79.1 ms: 1.18x faster                                                 |
| generators                 | 46.0 ms                                                               | 39.3 ms: 1.17x faster                                                 |
| sympy_expand               | 689 ms                                                                | 591 ms: 1.17x faster                                                  |
| tornado_http               | 262 ms                                                                | 228 ms: 1.15x faster                                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 87.1 ms: 1.13x faster                                                 |
| regex_compile              | 197 ms                                                                | 174 ms: 1.13x faster                                                  |
| float                      | 127 ms                                                                | 112 ms: 1.13x faster                                                  |
| tomli_loads                | 2.99 sec                                                              | 2.66 sec: 1.12x faster                                                |
| sqlglot_parse              | 1.89 ms                                                               | 1.69 ms: 1.12x faster                                                 |
| crypto_pyaes               | 112 ms                                                                | 99.9 ms: 1.12x faster                                                 |
| sympy_integrate            | 31.4 ms                                                               | 28.1 ms: 1.12x faster                                                 |
| sympy_sum                  | 229 ms                                                                | 207 ms: 1.11x faster                                                  |
| django_template            | 48.6 ms                                                               | 44.0 ms: 1.10x faster                                                 |
| xml_etree_generate         | 128 ms                                                                | 117 ms: 1.10x faster                                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 6.13 sec: 1.08x faster                                                |
| python_startup_no_site     | 16.3 ms                                                               | 15.0 ms: 1.08x faster                                                 |
| sqlglot_transpile          | 2.28 ms                                                               | 2.12 ms: 1.08x faster                                                 |
| meteor_contest             | 149 ms                                                                | 138 ms: 1.08x faster                                                  |
| pycparser                  | 1.73 sec                                                              | 1.63 sec: 1.06x faster                                                |
| async_generators           | 617 ms                                                                | 580 ms: 1.06x faster                                                  |
| thrift                     | 1.17 ms                                                               | 1.10 ms: 1.06x faster                                                 |
| scimark_fft                | 499 ms                                                                | 471 ms: 1.06x faster                                                  |
| logging_silent             | 135 ns                                                                | 128 ns: 1.06x faster                                                  |
| dask                       | 924 ms                                                                | 872 ms: 1.06x faster                                                  |
| nbody                      | 125 ms                                                                | 118 ms: 1.06x faster                                                  |
| mdp                        | 3.84 sec                                                              | 3.64 sec: 1.06x faster                                                |
| mako                       | 17.2 ms                                                               | 16.3 ms: 1.05x faster                                                 |
| genshi_text                | 31.9 ms                                                               | 30.2 ms: 1.05x faster                                                 |
| xml_etree_process          | 85.7 ms                                                               | 81.3 ms: 1.05x faster                                                 |
| pidigits                   | 255 ms                                                                | 243 ms: 1.05x faster                                                  |
| spectral_norm              | 158 ms                                                                | 150 ms: 1.05x faster                                                  |
| hexiom                     | 8.87 ms                                                               | 8.49 ms: 1.04x faster                                                 |
| pprint_pformat             | 2.03 sec                                                              | 1.94 sec: 1.04x faster                                                |
| regex_effbot               | 4.97 ms                                                               | 4.78 ms: 1.04x faster                                                 |
| docutils                   | 4.06 sec                                                              | 3.95 sec: 1.03x faster                                                |
| python_startup             | 21.2 ms                                                               | 22.1 ms: 1.04x slower                                                 |
| coroutines                 | 30.1 ms                                                               | 31.6 ms: 1.05x slower                                                 |
| pickle                     | 14.8 us                                                               | 15.6 us: 1.05x slower                                                 |
| sqlite_synth               | 3.75 us                                                               | 4.13 us: 1.10x slower                                                 |
| telco                      | 9.71 ms                                                               | 10.9 ms: 1.12x slower                                                 |
| json_dumps                 | 13.6 ms                                                               | 15.5 ms: 1.14x slower                                                 |
| create_gc_cycles           | 2.02 ms                                                               | 2.32 ms: 1.15x slower                                                 |
| regex_v8                   | 31.1 ms                                                               | 35.8 ms: 1.15x slower                                                 |
| typing_runtime_protocols   | 199 us                                                                | 234 us: 1.17x slower                                                  |
| coverage                   | 97.6 ms                                                               | 118 ms: 1.21x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.09x faster                                                          |

Benchmark hidden because not significant (33): pylint, bench_thread_pool, 2to3, unpickle_pure_python, pickle_pure_python, asyncio_tcp, html5lib, sqlglot_normalize, richards_super, fannkuch, asyncio_websockets, gc_traversal, asyncio_tcp_ssl, scimark_sor, unpack_sequence, regex_dna, pickle_list, pyflate, genshi_xml, richards, scimark_lu, xml_etree_parse, xml_etree_iterparse, pprint_safe_repr, unpickle_list, unpickle, pickle_dict, json, sqlglot_optimize, json_loads, go, bench_mp_pool, nqueens
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.89x