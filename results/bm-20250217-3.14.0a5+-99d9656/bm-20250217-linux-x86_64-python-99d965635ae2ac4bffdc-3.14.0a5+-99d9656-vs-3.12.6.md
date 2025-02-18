# Results vs. 3.12.6

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.104x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.56 sec: 1.12x faster                                                 |
| html5lib       | 88.9 ms                                                | 82.9 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 919 ms: 2.10x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 480 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 464 ms: 2.00x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 931 ms: 1.99x faster                                                   |
| async_tree_none            | 741 ms                                                 | 410 ms: 1.81x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 403 ms: 1.75x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 697 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 719 ms: 1.50x faster                                                   |
| async_generators           | 589 ms                                                 | 545 ms: 1.08x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.56x faster                                                           |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 98.6 ms: 1.25x faster                                                  |
| pidigits       | 250 ms                                                 | 226 ms: 1.10x faster                                                   |
| nbody          | 119 ms                                                 | 124 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.20 ms: 1.22x faster                                                  |
| regex_compile  | 187 ms                                                 | 171 ms: 1.09x faster                                                   |
| regex_v8       | 32.5 ms                                                | 35.0 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 201 ms: 1.20x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| xml_etree_iterparse | 169 ms                                                 | 150 ms: 1.13x faster                                                   |
| pickle_pure_python  | 436 us                                                 | 403 us: 1.08x faster                                                   |
| json_loads          | 37.9 us                                                | 40.3 us: 1.06x slower                                                  |
| json_dumps          | 14.3 ms                                                | 16.1 ms: 1.13x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_generate, unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.6 ms: 1.13x faster                                                  |
| python_startup         | 23.7 ms                                                | 26.6 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 27.8 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (3): genshi_xml, django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 919 ms: 2.10x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 480 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 464 ms: 2.00x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 931 ms: 1.99x faster                                                   |
| async_tree_none            | 741 ms                                                 | 410 ms: 1.81x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 403 ms: 1.75x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 697 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 719 ms: 1.50x faster                                                   |
| comprehensions             | 27.1 us                                                | 20.2 us: 1.34x faster                                                  |
| spectral_norm              | 156 ms                                                 | 121 ms: 1.28x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 41.3 us: 1.27x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 172 ms: 1.27x faster                                                   |
| float                      | 123 ms                                                 | 98.6 ms: 1.25x faster                                                  |
| deepcopy                   | 468 us                                                 | 379 us: 1.24x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.20 ms: 1.22x faster                                                  |
| pylint                     | 465 ms                                                 | 385 ms: 1.21x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 201 ms: 1.20x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.81 ms: 1.15x faster                                                  |
| logging_format             | 9.59 us                                                | 8.38 us: 1.14x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.06 ms: 1.13x faster                                                  |
| scimark_fft                | 500 ms                                                 | 442 ms: 1.13x faster                                                   |
| raytrace                   | 408 ms                                                 | 361 ms: 1.13x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.58 sec: 1.13x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 150 ms: 1.13x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 15.6 ms: 1.13x faster                                                  |
| chaos                      | 84.9 ms                                                | 75.6 ms: 1.12x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.56 sec: 1.12x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 5.87 sec: 1.12x faster                                                 |
| nqueens                    | 117 ms                                                 | 105 ms: 1.12x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.13 ms: 1.11x faster                                                  |
| go                         | 172 ms                                                 | 155 ms: 1.11x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.58 sec: 1.11x faster                                                 |
| pyflate                    | 727 ms                                                 | 658 ms: 1.11x faster                                                   |
| pidigits                   | 250 ms                                                 | 226 ms: 1.10x faster                                                   |
| logging_simple             | 9.45 us                                                | 8.56 us: 1.10x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 142 ms: 1.10x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 97.4 ms: 1.10x faster                                                  |
| sympy_str                  | 385 ms                                                 | 350 ms: 1.10x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 88.2 ms: 1.09x faster                                                  |
| regex_compile              | 187 ms                                                 | 171 ms: 1.09x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 204 ms: 1.09x faster                                                   |
| genshi_text                | 30.2 ms                                                | 27.8 ms: 1.09x faster                                                  |
| async_generators           | 589 ms                                                 | 545 ms: 1.08x faster                                                   |
| pickle_pure_python         | 436 us                                                 | 403 us: 1.08x faster                                                   |
| thrift                     | 1.06 ms                                                | 983 us: 1.08x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.76 us: 1.07x faster                                                  |
| html5lib                   | 88.9 ms                                                | 82.9 ms: 1.07x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 27.8 ms: 1.07x faster                                                  |
| fannkuch                   | 540 ms                                                 | 508 ms: 1.06x faster                                                   |
| scimark_sor                | 167 ms                                                 | 158 ms: 1.05x faster                                                   |
| nbody                      | 119 ms                                                 | 124 ms: 1.04x slower                                                   |
| json_loads                 | 37.9 us                                                | 40.3 us: 1.06x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.0 ms: 1.08x slower                                                  |
| json                       | 6.85 ms                                                | 7.38 ms: 1.08x slower                                                  |
| telco                      | 9.59 ms                                                | 10.5 ms: 1.09x slower                                                  |
| python_startup             | 23.7 ms                                                | 26.6 ms: 1.12x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.1 ms: 1.13x slower                                                  |
| coverage                   | 95.4 ms                                                | 124 ms: 1.30x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.78 ms: 1.50x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.46 ms: 1.79x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 91.0 ms: 4.40x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (28): dulwich_log, sqlalchemy_imperative, xml_etree_generate, 2to3, typing_runtime_protocols, genshi_xml, richards, logging_silent, pathlib, richards_super, pprint_safe_repr, pprint_pformat, scimark_lu, sqlite_synth, deltablue, django_template, generators, regex_dna, coroutines, meteor_contest, sqlglot_parse, unpickle_pure_python, asyncio_websockets, hexiom, sympy_expand, xml_etree_process, mako, sqlglot_optimize
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.13x