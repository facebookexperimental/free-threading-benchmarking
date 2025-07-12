# Results vs. 3.13.0rc2

- fork: python
- ref: db47f4d844acf2b6e52e
- machine: linux-x86_64
- commit hash: db47f4d
- commit date: 2025-07-11
- overall geometric mean: 1.036x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 608 ms: 1.50x faster                                                  |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 316 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 496 ms: 1.29x faster                                                  |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.5 ms: 1.10x faster                                                 |
| pidigits       | 217 ms                                                       | 200 ms: 1.08x faster                                                  |
| nbody          | 85.1 ms                                                      | 89.9 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                 |
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.6 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 57.3 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.0 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 207 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                 |
| genshi_xml     | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                 |
| mako           | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 608 ms: 1.50x faster                                                  |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 316 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 253 us: 1.41x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 28.6 us: 1.36x faster                                                 |
| go                         | 141 ms                                                       | 104 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 496 ms: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.70 us: 1.15x faster                                                 |
| spectral_norm              | 111 ms                                                       | 96.3 ms: 1.15x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                       | 396 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.5 ms: 1.12x faster                                                 |
| richards_super             | 51.6 ms                                                      | 46.2 ms: 1.12x faster                                                 |
| richards                   | 45.2 ms                                                      | 40.5 ms: 1.12x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                 |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 70.5 ms: 1.10x faster                                                 |
| pidigits                   | 217 ms                                                       | 200 ms: 1.08x faster                                                  |
| logging_silent             | 103 ns                                                       | 95.3 ns: 1.08x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.58 ms: 1.07x faster                                                 |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.4 us: 1.07x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.3 ms: 1.07x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 693 ms: 1.06x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 18.7 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                                |
| tomli_loads                | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| scimark_fft                | 349 ms                                                       | 334 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.91 us: 1.04x faster                                                 |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.3 ms: 1.04x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.63 us: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 754 us: 1.03x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.0 ms: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                |
| deltablue                  | 3.12 ms                                                      | 3.05 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.0 ms: 1.02x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 77.0 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.8 ms: 1.01x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 207 us: 1.01x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.6 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.6 ms: 1.00x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.7 ms: 1.00x faster                                                 |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.80 ms: 1.02x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                                 |
| sympy_expand               | 457 ms                                                       | 467 ms: 1.02x slower                                                  |
| fannkuch                   | 370 ms                                                       | 381 ms: 1.03x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.05x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 89.9 ms: 1.06x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.52 ms: 1.44x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.97 ms: 1.47x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.35x slower                                                  |
| telco                      | 7.82 ms                                                      | 155 ms: 19.86x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x