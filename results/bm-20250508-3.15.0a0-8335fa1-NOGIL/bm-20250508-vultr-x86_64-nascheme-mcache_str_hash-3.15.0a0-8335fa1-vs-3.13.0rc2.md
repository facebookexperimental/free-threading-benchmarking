# Results vs. 3.13.0rc2

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: 8335fa1
- commit date: 2025-05-08
- overall geometric mean: 1.026x slower
- HPT reliability: 95.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 286 ms: 1.10x slower                                               |
| docutils       | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                             |
| Geometric mean | (ref)                                                        | 1.04x slower                                                       |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 520 ms: 1.76x faster                                               |
| async_tree_io              | 876 ms                                                       | 550 ms: 1.59x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 226 ms: 1.49x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 284 ms: 1.46x faster                                               |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 474 ms: 1.35x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 502 ms: 1.33x faster                                               |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                               |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                               |
| float          | 77.5 ms                                                      | 70.7 ms: 1.10x faster                                              |
| nbody          | 85.1 ms                                                      | 119 ms: 1.40x slower                                               |
| Geometric mean | (ref)                                                        | 1.04x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                              |
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                              |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                               |
| regex_compile  | 132 ms                                                       | 145 ms: 1.10x slower                                               |
| Geometric mean | (ref)                                                        | 1.03x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.2 ms: 1.09x faster                                              |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                               |
| tomli_loads          | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                             |
| unpickle_pure_python | 210 us                                                       | 232 us: 1.10x slower                                               |
| json_loads           | 27.0 us                                                      | 30.4 us: 1.13x slower                                              |
| xml_etree_generate   | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                              |
| pickle_pure_python   | 294 us                                                       | 334 us: 1.13x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 69.8 ms: 1.18x slower                                              |
| json_dumps           | 10.5 ms                                                      | 13.4 ms: 1.27x slower                                              |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                              |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                              |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 55.4 ms: 1.14x slower                                              |
| django_template | 34.1 ms                                                      | 40.9 ms: 1.20x slower                                              |
| genshi_text     | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                              |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                              |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.34 sec: 1.76x faster                                             |
| async_tree_io_tg           | 913 ms                                                       | 520 ms: 1.76x faster                                               |
| gc_traversal               | 3.14 ms                                                      | 1.90 ms: 1.65x faster                                              |
| async_tree_io              | 876 ms                                                       | 550 ms: 1.59x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 226 ms: 1.49x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 284 ms: 1.46x faster                                               |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 474 ms: 1.35x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 502 ms: 1.33x faster                                               |
| deepcopy                   | 355 us                                                       | 292 us: 1.22x faster                                               |
| go                         | 141 ms                                                       | 124 ms: 1.13x faster                                               |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                               |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                              |
| deepcopy_memo              | 39.1 us                                                      | 35.4 us: 1.10x faster                                              |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                               |
| float                      | 77.5 ms                                                      | 70.7 ms: 1.10x faster                                              |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.2 ms: 1.09x faster                                              |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                              |
| sqlite_synth               | 2.21 us                                                      | 2.07 us: 1.06x faster                                              |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                               |
| dulwich_log                | 74.8 ms                                                      | 71.9 ms: 1.04x faster                                              |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                               |
| deepcopy_reduce            | 3.11 us                                                      | 3.04 us: 1.02x faster                                              |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                               |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                              |
| bpe_tokeniser              | 4.45 sec                                                     | 4.42 sec: 1.01x faster                                             |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                             |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                              |
| docutils                   | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                             |
| json                       | 4.93 ms                                                      | 5.19 ms: 1.05x slower                                              |
| scimark_fft                | 349 ms                                                       | 369 ms: 1.06x slower                                               |
| pprint_safe_repr           | 738 ms                                                       | 780 ms: 1.06x slower                                               |
| tomli_loads                | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                             |
| generators                 | 28.8 ms                                                      | 30.7 ms: 1.07x slower                                              |
| pyflate                    | 449 ms                                                       | 481 ms: 1.07x slower                                               |
| pprint_pformat             | 1.50 sec                                                     | 1.62 sec: 1.08x slower                                             |
| regex_compile              | 132 ms                                                       | 145 ms: 1.10x slower                                               |
| chaos                      | 57.3 ms                                                      | 62.9 ms: 1.10x slower                                              |
| 2to3                       | 260 ms                                                       | 286 ms: 1.10x slower                                               |
| unpickle_pure_python       | 210 us                                                       | 232 us: 1.10x slower                                               |
| create_gc_cycles           | 1.34 ms                                                      | 1.48 ms: 1.11x slower                                              |
| hexiom                     | 5.99 ms                                                      | 6.68 ms: 1.12x slower                                              |
| nqueens                    | 78.6 ms                                                      | 88.1 ms: 1.12x slower                                              |
| richards                   | 45.2 ms                                                      | 50.7 ms: 1.12x slower                                              |
| telco                      | 7.82 ms                                                      | 8.79 ms: 1.12x slower                                              |
| sympy_integrate            | 19.8 ms                                                      | 22.3 ms: 1.12x slower                                              |
| json_loads                 | 27.0 us                                                      | 30.4 us: 1.13x slower                                              |
| richards_super             | 51.6 ms                                                      | 58.3 ms: 1.13x slower                                              |
| xml_etree_generate         | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                              |
| pickle_pure_python         | 294 us                                                       | 334 us: 1.13x slower                                               |
| deltablue                  | 3.12 ms                                                      | 3.54 ms: 1.13x slower                                              |
| genshi_xml                 | 48.8 ms                                                      | 55.4 ms: 1.14x slower                                              |
| thrift                     | 778 us                                                       | 889 us: 1.14x slower                                               |
| sympy_str                  | 275 ms                                                       | 318 ms: 1.16x slower                                               |
| scimark_lu                 | 113 ms                                                       | 131 ms: 1.16x slower                                               |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                               |
| xml_etree_process          | 59.3 ms                                                      | 69.8 ms: 1.18x slower                                              |
| scimark_monte_carlo        | 65.4 ms                                                      | 76.9 ms: 1.18x slower                                              |
| raytrace                   | 253 ms                                                       | 297 ms: 1.18x slower                                               |
| sympy_expand               | 457 ms                                                       | 538 ms: 1.18x slower                                               |
| comprehensions             | 16.5 us                                                      | 19.6 us: 1.19x slower                                              |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.62 ms: 1.19x slower                                              |
| django_template            | 34.1 ms                                                      | 40.9 ms: 1.20x slower                                              |
| genshi_text                | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                              |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.25x slower                                               |
| meteor_contest             | 102 ms                                                       | 127 ms: 1.25x slower                                               |
| logging_simple             | 6.16 us                                                      | 7.76 us: 1.26x slower                                              |
| logging_format             | 6.84 us                                                      | 8.62 us: 1.26x slower                                              |
| json_dumps                 | 10.5 ms                                                      | 13.4 ms: 1.27x slower                                              |
| crypto_pyaes               | 67.9 ms                                                      | 86.5 ms: 1.27x slower                                              |
| fannkuch                   | 370 ms                                                       | 473 ms: 1.28x slower                                               |
| python_startup_no_site     | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                              |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.33x slower                                               |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                              |
| nbody                      | 85.1 ms                                                      | 119 ms: 1.40x slower                                               |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                              |
| bench_thread_pool          | 919 us                                                       | 3.13 ms: 3.41x slower                                              |
| logging_silent             | 103 ns                                                       | 536 ns: 5.23x slower                                               |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.36x slower                                               |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                       |

Benchmark hidden because not significant (3): pylint, html5lib, spectral_norm
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250508-3.15.0a0-8335fa1-NOGIL/bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.026x slower

# HPT report

- Reliability score: 95.66% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x