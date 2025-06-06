# Results vs. 3.13.0rc2

- fork: mpage
- ref: aa_test_4
- machine: linux-x86_64
- commit hash: 80948e8
- commit date: 2025-01-18
- overall geometric mean: 1.057x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                       |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 326 ms: 1.41x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 492 ms: 1.35x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                       |
| async_tree_none            | 354 ms                                                       | 270 ms: 1.31x faster                                       |
| async_generators           | 377 ms                                                       | 321 ms: 1.18x faster                                       |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                       |
| Geometric mean             | (ref)                                                        | 1.29x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                       |
| float          | 77.5 ms                                                      | 71.1 ms: 1.09x faster                                      |
| nbody          | 85.1 ms                                                      | 87.4 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                        | 1.06x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                      |
| regex_dna      | 180 ms                                                       | 169 ms: 1.06x faster                                       |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                       |
| regex_v8       | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                     |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                       |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                      |
| xml_etree_generate   | 85.4 ms                                                      | 84.3 ms: 1.01x faster                                      |
| json_loads           | 27.0 us                                                      | 27.5 us: 1.02x slower                                      |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                       |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                       |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                      |
| Geometric mean       | (ref)                                                        | 1.00x slower                                               |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                      |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                      |
| Geometric mean         | (ref)                                                        | 1.15x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                      |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                      |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                      |
| Geometric mean  | (ref)                                                        | 1.01x slower                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 326 ms: 1.41x faster                                       |
| deepcopy                   | 355 us                                                       | 260 us: 1.37x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 492 ms: 1.35x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                       |
| async_tree_none            | 354 ms                                                       | 270 ms: 1.31x faster                                       |
| deepcopy_memo              | 39.1 us                                                      | 30.1 us: 1.30x faster                                      |
| spectral_norm              | 111 ms                                                       | 88.1 ms: 1.26x faster                                      |
| go                         | 141 ms                                                       | 113 ms: 1.25x faster                                       |
| scimark_sor                | 134 ms                                                       | 112 ms: 1.20x faster                                       |
| deepcopy_reduce            | 3.11 us                                                      | 2.60 us: 1.19x faster                                      |
| async_generators           | 377 ms                                                       | 321 ms: 1.18x faster                                       |
| scimark_fft                | 349 ms                                                       | 307 ms: 1.14x faster                                       |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                       |
| pylint                     | 317 ms                                                       | 281 ms: 1.13x faster                                       |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                      |
| telco                      | 7.82 ms                                                      | 7.13 ms: 1.10x faster                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.29 ms: 1.10x faster                                      |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                       |
| float                      | 77.5 ms                                                      | 71.1 ms: 1.09x faster                                      |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                      |
| richards                   | 45.2 ms                                                      | 42.3 ms: 1.07x faster                                      |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.06x faster                                       |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                     |
| richards_super             | 51.6 ms                                                      | 48.8 ms: 1.06x faster                                      |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                       |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                     |
| chaos                      | 57.3 ms                                                      | 54.3 ms: 1.06x faster                                      |
| pprint_safe_repr           | 738 ms                                                       | 700 ms: 1.05x faster                                       |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                      |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                       |
| hexiom                     | 5.99 ms                                                      | 5.74 ms: 1.04x faster                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                      |
| crypto_pyaes               | 67.9 ms                                                      | 65.1 ms: 1.04x faster                                      |
| thrift                     | 778 us                                                       | 748 us: 1.04x faster                                       |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.3 ms: 1.03x faster                                      |
| meteor_contest             | 102 ms                                                       | 98.6 ms: 1.03x faster                                      |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                       |
| coverage                   | 83.0 ms                                                      | 80.7 ms: 1.03x faster                                      |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                      |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                      |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                     |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                       |
| sqlglot_parse              | 1.25 ms                                                      | 1.23 ms: 1.01x faster                                      |
| xml_etree_generate         | 85.4 ms                                                      | 84.3 ms: 1.01x faster                                      |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.01x faster                                      |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                       |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                       |
| nqueens                    | 78.6 ms                                                      | 77.9 ms: 1.01x faster                                      |
| mdp                        | 2.36 sec                                                     | 2.33 sec: 1.01x faster                                     |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                       |
| deltablue                  | 3.12 ms                                                      | 3.11 ms: 1.00x faster                                      |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.00x faster                                     |
| sqlglot_normalize          | 106 ms                                                       | 105 ms: 1.00x faster                                       |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                      |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                       |
| dulwich_log                | 74.8 ms                                                      | 75.4 ms: 1.01x slower                                      |
| json_loads                 | 27.0 us                                                      | 27.5 us: 1.02x slower                                      |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                       |
| logging_format             | 6.84 us                                                      | 6.99 us: 1.02x slower                                      |
| nbody                      | 85.1 ms                                                      | 87.4 ms: 1.03x slower                                      |
| comprehensions             | 16.5 us                                                      | 16.9 us: 1.03x slower                                      |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                       |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                      |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                      |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                       |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                       |
| regex_v8                   | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                      |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                      |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                      |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                      |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                      |
| bench_mp_pool              | 11.0 ms                                                      | 88.1 ms: 8.02x slower                                      |
| Geometric mean             | (ref)                                                        | 1.03x faster                                               |

Benchmark hidden because not significant (8): genshi_xml, sqlglot_optimize, sqlite_synth, json, sympy_expand, xml_etree_process, logging_simple, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250118-3.14.0a4+-80948e8/bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x