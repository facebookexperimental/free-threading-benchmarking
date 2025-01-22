# Results vs. 3.13.0rc2

- fork: mpage
- ref: aa_test_6
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.049x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                       |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                     |
| Geometric mean | (ref)                                                        | 1.01x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.44x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                       |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.33x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                       |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                       |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.05x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                       |
| Geometric mean             | (ref)                                                        | 1.29x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.2 ms: 1.10x faster                                      |
| pidigits       | 217 ms                                                       | 206 ms: 1.05x faster                                       |
| nbody          | 85.1 ms                                                      | 91.7 ms: 1.08x slower                                      |
| Geometric mean | (ref)                                                        | 1.02x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                      |
| regex_dna      | 180 ms                                                       | 165 ms: 1.09x faster                                       |
| regex_compile  | 132 ms                                                       | 129 ms: 1.02x faster                                       |
| regex_v8       | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                      |
| Geometric mean | (ref)                                                        | 1.05x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                       |
| xml_etree_iterparse  | 94.9 ms                                                      | 89.8 ms: 1.06x faster                                      |
| xml_etree_generate   | 85.4 ms                                                      | 82.9 ms: 1.03x faster                                      |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                     |
| xml_etree_process    | 59.3 ms                                                      | 60.0 ms: 1.01x slower                                      |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                      |
| unpickle_pure_python | 210 us                                                       | 226 us: 1.07x slower                                       |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                       |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                      |
| Geometric mean       | (ref)                                                        | 1.01x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                      |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| Geometric mean         | (ref)                                                        | 1.16x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.7 ms: 1.01x slower                                      |
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                      |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                      |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                      |
| Geometric mean  | (ref)                                                        | 1.03x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.44x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                       |
| deepcopy                   | 355 us                                                       | 255 us: 1.39x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                       |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.33x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 480 ms: 1.33x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                       |
| deepcopy_memo              | 39.1 us                                                      | 30.1 us: 1.30x faster                                      |
| go                         | 141 ms                                                       | 114 ms: 1.24x faster                                       |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                      |
| spectral_norm              | 111 ms                                                       | 93.6 ms: 1.19x faster                                      |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                       |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.17x faster                                       |
| regex_effbot               | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                      |
| pylint                     | 317 ms                                                       | 281 ms: 1.13x faster                                       |
| scimark_fft                | 349 ms                                                       | 313 ms: 1.12x faster                                       |
| float                      | 77.5 ms                                                      | 70.2 ms: 1.10x faster                                      |
| telco                      | 7.82 ms                                                      | 7.11 ms: 1.10x faster                                      |
| richards                   | 45.2 ms                                                      | 41.2 ms: 1.10x faster                                      |
| regex_dna                  | 180 ms                                                       | 165 ms: 1.09x faster                                       |
| pyflate                    | 449 ms                                                       | 412 ms: 1.09x faster                                       |
| richards_super             | 51.6 ms                                                      | 47.4 ms: 1.09x faster                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.37 ms: 1.08x faster                                      |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                       |
| generators                 | 28.8 ms                                                      | 27.2 ms: 1.06x faster                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.8 ms: 1.06x faster                                      |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.05x faster                                      |
| pidigits                   | 217 ms                                                       | 206 ms: 1.05x faster                                       |
| bpe_tokeniser              | 4.45 sec                                                     | 4.24 sec: 1.05x faster                                     |
| thrift                     | 778 us                                                       | 746 us: 1.04x faster                                       |
| coverage                   | 83.0 ms                                                      | 80.0 ms: 1.04x faster                                      |
| pathlib                    | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                      |
| pprint_safe_repr           | 738 ms                                                       | 714 ms: 1.03x faster                                       |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                     |
| hexiom                     | 5.99 ms                                                      | 5.81 ms: 1.03x faster                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.4 ms: 1.03x faster                                      |
| xml_etree_generate         | 85.4 ms                                                      | 82.9 ms: 1.03x faster                                      |
| crypto_pyaes               | 67.9 ms                                                      | 66.0 ms: 1.03x faster                                      |
| regex_compile              | 132 ms                                                       | 129 ms: 1.02x faster                                       |
| mdp                        | 2.36 sec                                                     | 2.30 sec: 1.02x faster                                     |
| meteor_contest             | 102 ms                                                       | 99.6 ms: 1.02x faster                                      |
| chaos                      | 57.3 ms                                                      | 56.4 ms: 1.02x faster                                      |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                     |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                     |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                       |
| logging_silent             | 103 ns                                                       | 102 ns: 1.01x faster                                       |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                       |
| sqlglot_transpile          | 1.56 ms                                                      | 1.55 ms: 1.01x faster                                      |
| deltablue                  | 3.12 ms                                                      | 3.10 ms: 1.01x faster                                      |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                       |
| sqlglot_normalize          | 106 ms                                                       | 105 ms: 1.01x faster                                       |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.00x faster                                      |
| sympy_integrate            | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                      |
| genshi_text                | 21.5 ms                                                      | 21.7 ms: 1.01x slower                                      |
| json                       | 4.93 ms                                                      | 4.97 ms: 1.01x slower                                      |
| xml_etree_process          | 59.3 ms                                                      | 60.0 ms: 1.01x slower                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                      |
| fannkuch                   | 370 ms                                                       | 375 ms: 1.01x slower                                       |
| sympy_expand               | 457 ms                                                       | 465 ms: 1.02x slower                                       |
| genshi_xml                 | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                      |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                     |
| comprehensions             | 16.5 us                                                      | 16.8 us: 1.02x slower                                      |
| dulwich_log                | 74.8 ms                                                      | 76.7 ms: 1.03x slower                                      |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                       |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                      |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                      |
| raytrace                   | 253 ms                                                       | 263 ms: 1.04x slower                                       |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                      |
| regex_v8                   | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                      |
| unpickle_pure_python       | 210 us                                                       | 226 us: 1.07x slower                                       |
| logging_format             | 6.84 us                                                      | 7.35 us: 1.07x slower                                      |
| logging_simple             | 6.16 us                                                      | 6.63 us: 1.08x slower                                      |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                       |
| nbody                      | 85.1 ms                                                      | 91.7 ms: 1.08x slower                                      |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                      |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                      |
| gc_traversal               | 3.14 ms                                                      | 3.99 ms: 1.27x slower                                      |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                      |
| bench_mp_pool              | 11.0 ms                                                      | 89.7 ms: 8.16x slower                                      |
| Geometric mean             | (ref)                                                        | 1.02x faster                                               |

Benchmark hidden because not significant (5): nqueens, sqlglot_optimize, sympy_sum, sympy_str, sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x