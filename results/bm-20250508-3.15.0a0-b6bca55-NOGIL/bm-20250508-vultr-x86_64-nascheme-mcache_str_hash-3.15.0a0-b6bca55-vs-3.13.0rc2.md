# Results vs. 3.13.0rc2

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: b6bca55
- commit date: 2025-05-08
- overall geometric mean: 1.024x slower
- HPT reliability: 98.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 285 ms: 1.10x slower                                               |
| docutils       | 2.62 sec                                                     | 2.71 sec: 1.03x slower                                             |
| Geometric mean | (ref)                                                        | 1.05x slower                                                       |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 523 ms: 1.75x faster                                               |
| async_tree_io              | 876 ms                                                       | 552 ms: 1.59x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 224 ms: 1.50x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 284 ms: 1.46x faster                                               |
| async_tree_none            | 354 ms                                                       | 259 ms: 1.37x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 512 ms: 1.30x faster                                               |
| async_generators           | 377 ms                                                       | 365 ms: 1.03x faster                                               |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                              |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                               |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                               |
| float          | 77.5 ms                                                      | 69.9 ms: 1.11x faster                                              |
| nbody          | 85.1 ms                                                      | 121 ms: 1.42x slower                                               |
| Geometric mean | (ref)                                                        | 1.04x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                              |
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                              |
| regex_compile  | 132 ms                                                       | 145 ms: 1.10x slower                                               |
| Geometric mean | (ref)                                                        | 1.02x faster                                                       |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.4 ms: 1.09x faster                                              |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                               |
| tomli_loads          | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                             |
| unpickle_pure_python | 210 us                                                       | 226 us: 1.08x slower                                               |
| xml_etree_generate   | 85.4 ms                                                      | 94.4 ms: 1.11x slower                                              |
| pickle_pure_python   | 294 us                                                       | 328 us: 1.11x slower                                               |
| json_loads           | 27.0 us                                                      | 30.6 us: 1.13x slower                                              |
| xml_etree_process    | 59.3 ms                                                      | 67.3 ms: 1.13x slower                                              |
| json_dumps           | 10.5 ms                                                      | 13.4 ms: 1.27x slower                                              |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                              |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                              |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 55.9 ms: 1.15x slower                                              |
| django_template | 34.1 ms                                                      | 39.8 ms: 1.17x slower                                              |
| genshi_text     | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                              |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                              |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.34 sec: 1.76x faster                                             |
| async_tree_io_tg           | 913 ms                                                       | 523 ms: 1.75x faster                                               |
| gc_traversal               | 3.14 ms                                                      | 1.91 ms: 1.65x faster                                              |
| async_tree_io              | 876 ms                                                       | 552 ms: 1.59x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 224 ms: 1.50x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 284 ms: 1.46x faster                                               |
| async_tree_none            | 354 ms                                                       | 259 ms: 1.37x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 512 ms: 1.30x faster                                               |
| deepcopy                   | 355 us                                                       | 294 us: 1.21x faster                                               |
| go                         | 141 ms                                                       | 124 ms: 1.14x faster                                               |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                               |
| float                      | 77.5 ms                                                      | 69.9 ms: 1.11x faster                                              |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.11x faster                                               |
| deepcopy_memo              | 39.1 us                                                      | 35.4 us: 1.10x faster                                              |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                              |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                              |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.4 ms: 1.09x faster                                              |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                               |
| dulwich_log                | 74.8 ms                                                      | 71.1 ms: 1.05x faster                                              |
| sqlite_synth               | 2.21 us                                                      | 2.10 us: 1.05x faster                                              |
| async_generators           | 377 ms                                                       | 365 ms: 1.03x faster                                               |
| deepcopy_reduce            | 3.11 us                                                      | 3.05 us: 1.02x faster                                              |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                               |
| logging_silent             | 103 ns                                                       | 101 ns: 1.01x faster                                               |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                              |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                               |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                             |
| generators                 | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                              |
| pathlib                    | 19.2 ms                                                      | 19.7 ms: 1.03x slower                                              |
| docutils                   | 2.62 sec                                                     | 2.71 sec: 1.03x slower                                             |
| scimark_fft                | 349 ms                                                       | 366 ms: 1.05x slower                                               |
| json                       | 4.93 ms                                                      | 5.18 ms: 1.05x slower                                              |
| pprint_safe_repr           | 738 ms                                                       | 779 ms: 1.06x slower                                               |
| tomli_loads                | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                             |
| pprint_pformat             | 1.50 sec                                                     | 1.61 sec: 1.07x slower                                             |
| unpickle_pure_python       | 210 us                                                       | 226 us: 1.08x slower                                               |
| pyflate                    | 449 ms                                                       | 486 ms: 1.08x slower                                               |
| regex_compile              | 132 ms                                                       | 145 ms: 1.10x slower                                               |
| 2to3                       | 260 ms                                                       | 285 ms: 1.10x slower                                               |
| xml_etree_generate         | 85.4 ms                                                      | 94.4 ms: 1.11x slower                                              |
| hexiom                     | 5.99 ms                                                      | 6.64 ms: 1.11x slower                                              |
| create_gc_cycles           | 1.34 ms                                                      | 1.49 ms: 1.11x slower                                              |
| chaos                      | 57.3 ms                                                      | 63.7 ms: 1.11x slower                                              |
| telco                      | 7.82 ms                                                      | 8.72 ms: 1.11x slower                                              |
| pickle_pure_python         | 294 us                                                       | 328 us: 1.11x slower                                               |
| thrift                     | 778 us                                                       | 875 us: 1.12x slower                                               |
| nqueens                    | 78.6 ms                                                      | 88.4 ms: 1.12x slower                                              |
| sympy_integrate            | 19.8 ms                                                      | 22.3 ms: 1.13x slower                                              |
| richards_super             | 51.6 ms                                                      | 58.4 ms: 1.13x slower                                              |
| json_loads                 | 27.0 us                                                      | 30.6 us: 1.13x slower                                              |
| richards                   | 45.2 ms                                                      | 51.3 ms: 1.13x slower                                              |
| xml_etree_process          | 59.3 ms                                                      | 67.3 ms: 1.13x slower                                              |
| deltablue                  | 3.12 ms                                                      | 3.54 ms: 1.13x slower                                              |
| genshi_xml                 | 48.8 ms                                                      | 55.9 ms: 1.15x slower                                              |
| logging_simple             | 6.16 us                                                      | 7.13 us: 1.16x slower                                              |
| logging_format             | 6.84 us                                                      | 7.96 us: 1.16x slower                                              |
| django_template            | 34.1 ms                                                      | 39.8 ms: 1.17x slower                                              |
| sympy_str                  | 275 ms                                                       | 320 ms: 1.17x slower                                               |
| sympy_sum                  | 156 ms                                                       | 182 ms: 1.17x slower                                               |
| scimark_lu                 | 113 ms                                                       | 132 ms: 1.17x slower                                               |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.53 ms: 1.17x slower                                              |
| sympy_expand               | 457 ms                                                       | 537 ms: 1.18x slower                                               |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.0 ms: 1.18x slower                                              |
| comprehensions             | 16.5 us                                                      | 19.4 us: 1.18x slower                                              |
| raytrace                   | 253 ms                                                       | 301 ms: 1.19x slower                                               |
| genshi_text                | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                              |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.24x slower                                               |
| json_dumps                 | 10.5 ms                                                      | 13.4 ms: 1.27x slower                                              |
| crypto_pyaes               | 67.9 ms                                                      | 86.4 ms: 1.27x slower                                              |
| fannkuch                   | 370 ms                                                       | 476 ms: 1.29x slower                                               |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                               |
| python_startup_no_site     | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                              |
| coverage                   | 83.0 ms                                                      | 109 ms: 1.32x slower                                               |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                              |
| nbody                      | 85.1 ms                                                      | 121 ms: 1.42x slower                                               |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                              |
| bench_thread_pool          | 919 us                                                       | 3.13 ms: 3.40x slower                                              |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.37x slower                                               |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                       |

Benchmark hidden because not significant (4): pylint, bpe_tokeniser, regex_dna, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250508-3.15.0a0-b6bca55-NOGIL/bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 98.11% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x