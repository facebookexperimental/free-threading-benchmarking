# Results vs. 3.12.6

- fork: python
- ref: cfeaa992ba9bad9be268
- machine: linux-x86_64
- commit hash: cfeaa99
- commit date: 2024-12-16
- overall geometric mean: 1.118x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 429 ms: 1.06x faster                                                   |
| docutils       | 4.00 sec                                               | 3.63 sec: 1.10x faster                                                 |
| html5lib       | 88.9 ms                                                | 83.6 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 869 ms: 2.23x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 877 ms: 2.11x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 460 ms: 2.02x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 516 ms: 1.89x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 378 ms: 1.86x faster                                                   |
| async_tree_none            | 741 ms                                                 | 401 ms: 1.85x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 673 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 703 ms: 1.53x faster                                                   |
| async_generators           | 589 ms                                                 | 534 ms: 1.10x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.60x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 108 ms: 1.14x faster                                                   |
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.60 ms: 1.12x faster                                                  |
| regex_compile  | 187 ms                                                 | 171 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 193 ms: 1.24x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 146 ms: 1.16x faster                                                   |
| json_loads          | 37.9 us                                                | 34.4 us: 1.10x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.68 sec: 1.07x faster                                                 |
| xml_etree_process   | 83.7 ms                                                | 78.9 ms: 1.06x faster                                                  |
| xml_etree_generate  | 127 ms                                                 | 121 ms: 1.05x faster                                                   |
| json_dumps          | 14.3 ms                                                | 15.7 ms: 1.09x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (2): unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.4 ms: 1.22x faster                                                  |
| python_startup         | 23.7 ms                                                | 25.6 ms: 1.08x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 27.6 ms: 1.09x faster                                                  |
| mako           | 15.7 ms                                                | 16.5 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 869 ms: 2.23x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 877 ms: 2.11x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 460 ms: 2.02x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 516 ms: 1.89x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 378 ms: 1.86x faster                                                   |
| async_tree_none            | 741 ms                                                 | 401 ms: 1.85x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 673 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 703 ms: 1.53x faster                                                   |
| deepcopy                   | 468 us                                                 | 324 us: 1.44x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 39.5 us: 1.33x faster                                                  |
| logging_simple             | 9.45 us                                                | 7.52 us: 1.26x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.6 us: 1.26x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 174 ms: 1.25x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 193 ms: 1.24x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 2.84 ms: 1.23x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.4 ms: 1.22x faster                                                  |
| pylint                     | 465 ms                                                 | 386 ms: 1.20x faster                                                   |
| pathlib                    | 31.6 ms                                                | 26.3 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.38 us: 1.20x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.52 sec: 1.18x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 91.7 ms: 1.17x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 146 ms: 1.16x faster                                                   |
| spectral_norm              | 156 ms                                                 | 135 ms: 1.15x faster                                                   |
| raytrace                   | 408 ms                                                 | 354 ms: 1.15x faster                                                   |
| nqueens                    | 117 ms                                                 | 102 ms: 1.15x faster                                                   |
| float                      | 123 ms                                                 | 108 ms: 1.14x faster                                                   |
| scimark_fft                | 500 ms                                                 | 440 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.91 ms: 1.13x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 196 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.85 sec: 1.13x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 140 ms: 1.12x faster                                                   |
| go                         | 172 ms                                                 | 154 ms: 1.12x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.60 ms: 1.12x faster                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.2 ms: 1.11x faster                                                  |
| pyflate                    | 727 ms                                                 | 655 ms: 1.11x faster                                                   |
| async_generators           | 589 ms                                                 | 534 ms: 1.10x faster                                                   |
| json_loads                 | 37.9 us                                                | 34.4 us: 1.10x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.63 sec: 1.10x faster                                                 |
| logging_format             | 9.59 us                                                | 8.75 us: 1.10x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 88.0 ms: 1.10x faster                                                  |
| genshi_text                | 30.2 ms                                                | 27.6 ms: 1.09x faster                                                  |
| regex_compile              | 187 ms                                                 | 171 ms: 1.09x faster                                                   |
| sympy_str                  | 385 ms                                                 | 357 ms: 1.08x faster                                                   |
| json                       | 6.85 ms                                                | 6.36 ms: 1.08x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.68 sec: 1.07x faster                                                 |
| scimark_sor                | 167 ms                                                 | 156 ms: 1.07x faster                                                   |
| html5lib                   | 88.9 ms                                                | 83.6 ms: 1.06x faster                                                  |
| 2to3                       | 456 ms                                                 | 429 ms: 1.06x faster                                                   |
| xml_etree_process          | 83.7 ms                                                | 78.9 ms: 1.06x faster                                                  |
| dulwich_log                | 100 ms                                                 | 94.6 ms: 1.06x faster                                                  |
| chaos                      | 84.9 ms                                                | 80.2 ms: 1.06x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.76 sec: 1.06x faster                                                 |
| pidigits                   | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| sqlglot_parse              | 1.79 ms                                                | 1.70 ms: 1.05x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 121 ms: 1.05x faster                                                   |
| logging_silent             | 139 ns                                                 | 133 ns: 1.05x faster                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 72.8 ms: 1.04x faster                                                  |
| scimark_lu                 | 152 ms                                                 | 146 ms: 1.04x faster                                                   |
| sympy_expand               | 582 ms                                                 | 603 ms: 1.04x slower                                                   |
| mako                       | 15.7 ms                                                | 16.5 ms: 1.05x slower                                                  |
| telco                      | 9.59 ms                                                | 10.2 ms: 1.06x slower                                                  |
| python_startup             | 23.7 ms                                                | 25.6 ms: 1.08x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.7 ms: 1.09x slower                                                  |
| coverage                   | 95.4 ms                                                | 109 ms: 1.15x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.52 ms: 1.28x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.31 ms: 1.71x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 89.1 ms: 4.31x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (23): hexiom, fannkuch, unpickle_pure_python, richards_super, sqlglot_transpile, pickle_pure_python, typing_runtime_protocols, pprint_safe_repr, sqlite_synth, asyncio_websockets, genshi_xml, sympy_integrate, meteor_contest, thrift, regex_dna, pprint_pformat, coroutines, deltablue, generators, regex_v8, richards, nbody, django_template
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.118x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.13x