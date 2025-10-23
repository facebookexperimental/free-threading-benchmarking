# Results vs. 3.13.0rc2

- fork: python
- ref: bd2c7e8c8b10f4d31eab
- machine: linux-x86_64
- commit hash: bd2c7e8
- commit date: 2025-10-22
- overall geometric mean: 1.035x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                 |
| html5lib       | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 555 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 592 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 70.7 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 89.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                  |
| regex_compile  | 132 ms                                                       | 125 ms: 1.05x faster                                                   |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.6 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.74 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 82.8 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.5 ms: 1.01x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                 |
| async_tree_io              | 876 ms                                                       | 555 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 592 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.49x faster                                                  |
| deepcopy                   | 355 us                                                       | 246 us: 1.45x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                   |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.25x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.18x faster                                                  |
| spectral_norm              | 111 ms                                                       | 95.8 ms: 1.16x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.6 ms: 1.12x faster                                                  |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| scimark_fft                | 349 ms                                                       | 316 ms: 1.11x faster                                                   |
| richards                   | 45.2 ms                                                      | 40.9 ms: 1.11x faster                                                  |
| richards_super             | 51.6 ms                                                      | 46.9 ms: 1.10x faster                                                  |
| pylint                     | 317 ms                                                       | 288 ms: 1.10x faster                                                   |
| float                      | 77.5 ms                                                      | 70.7 ms: 1.09x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 68.8 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.74 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                       | 417 ms: 1.08x faster                                                   |
| async_generators           | 377 ms                                                       | 352 ms: 1.07x faster                                                   |
| comprehensions             | 16.5 us                                                      | 15.4 us: 1.07x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                                 |
| regex_compile              | 132 ms                                                       | 125 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 700 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.1 ms: 1.05x faster                                                  |
| logging_silent             | 103 ns                                                       | 97.6 ns: 1.05x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.71 ms: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.7 ms: 1.04x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.1 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.8 ms: 1.03x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.97 us: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.71 us: 1.02x faster                                                  |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| meteor_contest             | 102 ms                                                       | 99.7 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.6 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.63 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.5 ms: 1.01x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.6 ms: 1.01x faster                                                  |
| thrift                     | 778 us                                                       | 770 us: 1.01x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 79.0 ms: 1.00x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 157 ms: 1.01x slower                                                   |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                   |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.4 ms: 1.02x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.28 us: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| sympy_expand               | 457 ms                                                       | 479 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                                   |
| nbody                      | 85.1 ms                                                      | 89.8 ms: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.31 ms: 1.06x slower                                                  |
| fannkuch                   | 370 ms                                                       | 393 ms: 1.06x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 998 us: 1.09x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.68 ms: 1.49x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.33x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (3): genshi_xml, raytrace, regex_v8
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x