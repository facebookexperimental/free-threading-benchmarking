# Results vs. 3.13.0rc2

- fork: mpage
- ref: aa_test_5
- machine: linux-x86_64
- commit hash: 2ea0525
- commit date: 2025-01-21
- overall geometric mean: 1.051x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                       |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 613 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.44x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 486 ms: 1.37x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                       |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.33x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                       |
| async_generators           | 377 ms                                                       | 319 ms: 1.18x faster                                       |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                       |
| Geometric mean             | (ref)                                                        | 1.30x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                       |
| float          | 77.5 ms                                                      | 71.3 ms: 1.09x faster                                      |
| nbody          | 85.1 ms                                                      | 93.1 ms: 1.09x slower                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                      |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                       |
| regex_compile  | 132 ms                                                       | 128 ms: 1.03x faster                                       |
| regex_v8       | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                      |
| Geometric mean | (ref)                                                        | 1.03x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                       |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                      |
| tomli_loads          | 2.01 sec                                                     | 1.94 sec: 1.03x faster                                     |
| xml_etree_generate   | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                      |
| xml_etree_process    | 59.3 ms                                                      | 60.6 ms: 1.02x slower                                      |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                      |
| unpickle_pure_python | 210 us                                                       | 225 us: 1.07x slower                                       |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                      |
| pickle_pure_python   | 294 us                                                       | 322 us: 1.10x slower                                       |
| Geometric mean       | (ref)                                                        | 1.02x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                      |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                      |
| Geometric mean         | (ref)                                                        | 1.16x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                      |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                      |
| Geometric mean  | (ref)                                                        | 1.02x slower                                               |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 613 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.44x faster                                       |
| deepcopy                   | 355 us                                                       | 255 us: 1.39x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 486 ms: 1.37x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 476 ms: 1.34x faster                                       |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.33x faster                                       |
| deepcopy_memo              | 39.1 us                                                      | 29.7 us: 1.31x faster                                      |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                       |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                       |
| spectral_norm              | 111 ms                                                       | 91.5 ms: 1.21x faster                                      |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                      |
| async_generators           | 377 ms                                                       | 319 ms: 1.18x faster                                       |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                       |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.09 ms: 1.15x faster                                      |
| scimark_fft                | 349 ms                                                       | 305 ms: 1.15x faster                                       |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                       |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                      |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                       |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                      |
| float                      | 77.5 ms                                                      | 71.3 ms: 1.09x faster                                      |
| richards                   | 45.2 ms                                                      | 41.9 ms: 1.08x faster                                      |
| telco                      | 7.82 ms                                                      | 7.29 ms: 1.07x faster                                      |
| richards_super             | 51.6 ms                                                      | 48.2 ms: 1.07x faster                                      |
| pyflate                    | 449 ms                                                       | 419 ms: 1.07x faster                                       |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                       |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                     |
| pprint_safe_repr           | 738 ms                                                       | 703 ms: 1.05x faster                                       |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                      |
| coverage                   | 83.0 ms                                                      | 79.5 ms: 1.04x faster                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.04x faster                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.7 ms: 1.04x faster                                      |
| pathlib                    | 19.2 ms                                                      | 18.4 ms: 1.04x faster                                      |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                       |
| generators                 | 28.8 ms                                                      | 27.8 ms: 1.04x faster                                      |
| hexiom                     | 5.99 ms                                                      | 5.78 ms: 1.04x faster                                      |
| tomli_loads                | 2.01 sec                                                     | 1.94 sec: 1.03x faster                                     |
| thrift                     | 778 us                                                       | 753 us: 1.03x faster                                       |
| meteor_contest             | 102 ms                                                       | 98.4 ms: 1.03x faster                                      |
| regex_compile              | 132 ms                                                       | 128 ms: 1.03x faster                                       |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                       |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                      |
| mdp                        | 2.36 sec                                                     | 2.30 sec: 1.02x faster                                     |
| xml_etree_generate         | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                      |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                     |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                       |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                       |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.01x faster                                       |
| nqueens                    | 78.6 ms                                                      | 77.7 ms: 1.01x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                       |
| sqlglot_optimize           | 52.7 ms                                                      | 52.6 ms: 1.00x faster                                      |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                       |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                      |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                      |
| comprehensions             | 16.5 us                                                      | 16.6 us: 1.01x slower                                      |
| dulwich_log                | 74.8 ms                                                      | 75.9 ms: 1.01x slower                                      |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                     |
| logging_silent             | 103 ns                                                       | 104 ns: 1.02x slower                                       |
| crypto_pyaes               | 67.9 ms                                                      | 69.1 ms: 1.02x slower                                      |
| xml_etree_process          | 59.3 ms                                                      | 60.6 ms: 1.02x slower                                      |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                      |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                      |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.03x slower                                       |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                      |
| logging_format             | 6.84 us                                                      | 7.15 us: 1.05x slower                                      |
| logging_simple             | 6.16 us                                                      | 6.44 us: 1.05x slower                                      |
| raytrace                   | 253 ms                                                       | 266 ms: 1.05x slower                                       |
| regex_v8                   | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                      |
| unpickle_pure_python       | 210 us                                                       | 225 us: 1.07x slower                                       |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                      |
| nbody                      | 85.1 ms                                                      | 93.1 ms: 1.09x slower                                      |
| pickle_pure_python         | 294 us                                                       | 322 us: 1.10x slower                                       |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                      |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                      |
| gc_traversal               | 3.14 ms                                                      | 4.23 ms: 1.35x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                      |
| bench_mp_pool              | 11.0 ms                                                      | 88.8 ms: 8.08x slower                                      |
| Geometric mean             | (ref)                                                        | 1.02x faster                                               |

Benchmark hidden because not significant (8): sympy_str, genshi_text, sqlglot_transpile, sympy_integrate, sqlite_synth, deltablue, sympy_expand, genshi_xml
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250121-3.14.0a4+-2ea0525/bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x