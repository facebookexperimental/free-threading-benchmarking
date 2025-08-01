# Results vs. 3.13.0rc2

- fork: python
- ref: 4e40f2bea7edfa5ba7e2
- machine: linux-x86_64
- commit hash: 4e40f2b
- commit date: 2025-07-27
- overall geometric mean: 1.059x slower
- HPT reliability: 98.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 286 ms: 1.10x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.73 sec: 1.04x slower                                                |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 517 ms: 1.77x faster                                                  |
| async_tree_io              | 876 ms                                                       | 537 ms: 1.63x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 224 ms: 1.50x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 282 ms: 1.47x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 474 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                          |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| float          | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                 |
| nbody          | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| regex_compile  | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.16 sec: 1.07x slower                                                |
| unpickle_pure_python | 210 us                                                       | 233 us: 1.11x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.7 ms: 1.11x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 95.9 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                 |
| json_loads           | 27.0 us                                                      | 31.7 us: 1.17x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 347 us: 1.18x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 58.5 ms: 1.20x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.3 ms: 1.27x slower                                                 |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.78x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 517 ms: 1.77x faster                                                  |
| async_tree_io              | 876 ms                                                       | 537 ms: 1.63x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.96 ms: 1.60x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 224 ms: 1.50x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 282 ms: 1.47x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 474 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                  |
| deepcopy                   | 355 us                                                       | 301 us: 1.18x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                 |
| go                         | 141 ms                                                       | 122 ms: 1.16x faster                                                  |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 34.8 us: 1.12x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                 |
| scimark_sor                | 134 ms                                                       | 126 ms: 1.07x faster                                                  |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.9 ms: 1.04x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.02x faster                                                  |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.44 sec: 1.00x faster                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.16 us: 1.02x slower                                                 |
| pyflate                    | 449 ms                                                       | 458 ms: 1.02x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 19.7 ms: 1.02x slower                                                 |
| logging_silent             | 103 ns                                                       | 105 ns: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.73 sec: 1.04x slower                                                |
| scimark_fft                | 349 ms                                                       | 366 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.06x slower                                                |
| hexiom                     | 5.99 ms                                                      | 6.39 ms: 1.07x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.16 sec: 1.07x slower                                                |
| pprint_safe_repr           | 738 ms                                                       | 793 ms: 1.08x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.7 us: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.63 sec: 1.09x slower                                                |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                                 |
| 2to3                       | 260 ms                                                       | 286 ms: 1.10x slower                                                  |
| generators                 | 28.8 ms                                                      | 31.9 ms: 1.11x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 233 us: 1.11x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 87.3 ms: 1.11x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.7 ms: 1.11x slower                                                 |
| chaos                      | 57.3 ms                                                      | 63.9 ms: 1.12x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.2 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 95.9 ms: 1.12x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.98 us: 1.13x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.14x slower                                                  |
| thrift                     | 778 us                                                       | 887 us: 1.14x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.9 ms: 1.15x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.54 ms: 1.15x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.42 ms: 1.15x slower                                                 |
| sympy_str                  | 275 ms                                                       | 317 ms: 1.15x slower                                                  |
| sympy_expand               | 457 ms                                                       | 528 ms: 1.16x slower                                                  |
| richards_super             | 51.6 ms                                                      | 60.0 ms: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.99 us: 1.17x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.66 ms: 1.17x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.7 us: 1.17x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 347 us: 1.18x slower                                                  |
| meteor_contest             | 102 ms                                                       | 120 ms: 1.18x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 58.5 ms: 1.20x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.7 ms: 1.20x slower                                                 |
| raytrace                   | 253 ms                                                       | 305 ms: 1.21x slower                                                  |
| fannkuch                   | 370 ms                                                       | 450 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 189 us: 1.22x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 27.3 ms: 1.27x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 86.3 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                 |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.33x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.16 ms: 3.43x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.87x slower                                                  |
| telco                      | 7.82 ms                                                      | 177 ms: 22.65x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                          |

Benchmark hidden because not significant (3): pylint, html5lib, async_generators
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.059x slower

# HPT report

- Reliability score: 98.49% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x