# Results vs. 3.13.0rc2

- fork: mpage
- ref: aa_test_1
- machine: linux-x86_64
- commit hash: de82556
- commit date: 2025-01-16
- overall geometric mean: 1.054x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.02x faster                                       |
| docutils       | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 325 ms: 1.42x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                       |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                       |
| async_generators           | 377 ms                                                       | 326 ms: 1.16x faster                                       |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                       |
| Geometric mean             | (ref)                                                        | 1.29x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                       |
| float          | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                      |
| nbody          | 85.1 ms                                                      | 86.3 ms: 1.01x slower                                      |
| Geometric mean | (ref)                                                        | 1.06x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                      |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                       |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                       |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                      |
| Geometric mean | (ref)                                                        | 1.03x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.87 sec: 1.07x faster                                     |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                       |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                      |
| xml_etree_generate   | 85.4 ms                                                      | 83.9 ms: 1.02x faster                                      |
| xml_etree_process    | 59.3 ms                                                      | 59.6 ms: 1.00x slower                                      |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                       |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                      |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                       |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                      |
| Geometric mean       | (ref)                                                        | 1.00x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.45 ms: 1.01x slower                                      |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| Geometric mean         | (ref)                                                        | 1.16x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.0 ms: 1.03x faster                                      |
| genshi_xml      | 48.8 ms                                                      | 48.1 ms: 1.01x faster                                      |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                      |
| django_template | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                      |
| Geometric mean  | (ref)                                                        | 1.01x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                       |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                       |
| async_tree_memoization     | 461 ms                                                       | 325 ms: 1.42x faster                                       |
| deepcopy                   | 355 us                                                       | 257 us: 1.38x faster                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                       |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                       |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                       |
| deepcopy_memo              | 39.1 us                                                      | 30.0 us: 1.30x faster                                      |
| spectral_norm              | 111 ms                                                       | 90.8 ms: 1.22x faster                                      |
| go                         | 141 ms                                                       | 117 ms: 1.21x faster                                       |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                      |
| async_generators           | 377 ms                                                       | 326 ms: 1.16x faster                                       |
| scimark_sor                | 134 ms                                                       | 116 ms: 1.15x faster                                       |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                       |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                       |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                      |
| scimark_fft                | 349 ms                                                       | 310 ms: 1.13x faster                                       |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                       |
| telco                      | 7.82 ms                                                      | 7.25 ms: 1.08x faster                                      |
| tomli_loads                | 2.01 sec                                                     | 1.87 sec: 1.07x faster                                     |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                      |
| float                      | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                      |
| richards_super             | 51.6 ms                                                      | 48.4 ms: 1.07x faster                                      |
| richards                   | 45.2 ms                                                      | 42.4 ms: 1.07x faster                                      |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                       |
| pprint_safe_repr           | 738 ms                                                       | 693 ms: 1.06x faster                                       |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.43 ms: 1.06x faster                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                     |
| thrift                     | 778 us                                                       | 736 us: 1.06x faster                                       |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                     |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                       |
| chaos                      | 57.3 ms                                                      | 54.7 ms: 1.05x faster                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                      |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                       |
| hexiom                     | 5.99 ms                                                      | 5.81 ms: 1.03x faster                                      |
| meteor_contest             | 102 ms                                                       | 98.6 ms: 1.03x faster                                      |
| genshi_text                | 21.5 ms                                                      | 21.0 ms: 1.03x faster                                      |
| 2to3                       | 260 ms                                                       | 253 ms: 1.02x faster                                       |
| coverage                   | 83.0 ms                                                      | 81.0 ms: 1.02x faster                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.9 ms: 1.02x faster                                      |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                      |
| xml_etree_generate         | 85.4 ms                                                      | 83.9 ms: 1.02x faster                                      |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                       |
| mdp                        | 2.36 sec                                                     | 2.32 sec: 1.02x faster                                     |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.01x faster                                      |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                       |
| genshi_xml                 | 48.8 ms                                                      | 48.1 ms: 1.01x faster                                      |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                       |
| docutils                   | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                     |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                       |
| nqueens                    | 78.6 ms                                                      | 78.0 ms: 1.01x faster                                      |
| sqlglot_normalize          | 106 ms                                                       | 105 ms: 1.00x faster                                       |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                      |
| sqlglot_optimize           | 52.7 ms                                                      | 52.6 ms: 1.00x faster                                      |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                       |
| xml_etree_process          | 59.3 ms                                                      | 59.6 ms: 1.00x slower                                      |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                     |
| python_startup_no_site     | 7.39 ms                                                      | 7.45 ms: 1.01x slower                                      |
| json                       | 4.93 ms                                                      | 4.96 ms: 1.01x slower                                      |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                      |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                       |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                      |
| dulwich_log                | 74.8 ms                                                      | 75.8 ms: 1.01x slower                                      |
| nbody                      | 85.1 ms                                                      | 86.3 ms: 1.01x slower                                      |
| logging_format             | 6.84 us                                                      | 6.99 us: 1.02x slower                                      |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                      |
| deltablue                  | 3.12 ms                                                      | 3.20 ms: 1.02x slower                                      |
| comprehensions             | 16.5 us                                                      | 16.9 us: 1.03x slower                                      |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                      |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                       |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                       |
| raytrace                   | 253 ms                                                       | 265 ms: 1.05x slower                                       |
| django_template            | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                      |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                      |
| regex_v8                   | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                      |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                      |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                      |
| gc_traversal               | 3.14 ms                                                      | 4.37 ms: 1.39x slower                                      |
| bench_mp_pool              | 11.0 ms                                                      | 88.8 ms: 8.08x slower                                      |
| Geometric mean             | (ref)                                                        | 1.03x faster                                               |

Benchmark hidden because not significant (4): logging_simple, sqlglot_transpile, sympy_expand, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250116-3.14.0a4+-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.054x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x