# Results vs. 3.13.0rc2

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: 7723ceb
- commit date: 2025-05-12
- overall geometric mean: 1.026x slower
- HPT reliability: 96.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 284 ms: 1.09x slower                                               |
| docutils       | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                             |
| Geometric mean | (ref)                                                        | 1.04x slower                                                       |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 522 ms: 1.75x faster                                               |
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 225 ms: 1.49x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 283 ms: 1.46x faster                                               |
| async_tree_none            | 354 ms                                                       | 259 ms: 1.36x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 514 ms: 1.30x faster                                               |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                               |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                              |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                               |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 71.2 ms: 1.09x faster                                              |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                               |
| nbody          | 85.1 ms                                                      | 121 ms: 1.42x slower                                               |
| Geometric mean | (ref)                                                        | 1.08x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                              |
| regex_v8       | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                              |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                               |
| regex_compile  | 132 ms                                                       | 145 ms: 1.10x slower                                               |
| Geometric mean | (ref)                                                        | 1.02x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 86.7 ms: 1.09x faster                                              |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                               |
| tomli_loads          | 2.01 sec                                                     | 2.16 sec: 1.07x slower                                             |
| unpickle_pure_python | 210 us                                                       | 230 us: 1.09x slower                                               |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                              |
| xml_etree_generate   | 85.4 ms                                                      | 97.4 ms: 1.14x slower                                              |
| pickle_pure_python   | 294 us                                                       | 336 us: 1.14x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 69.7 ms: 1.17x slower                                              |
| json_dumps           | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                              |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                              |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                              |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 55.5 ms: 1.14x slower                                              |
| django_template | 34.1 ms                                                      | 40.9 ms: 1.20x slower                                              |
| genshi_text     | 21.5 ms                                                      | 26.2 ms: 1.22x slower                                              |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                              |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                             |
| async_tree_io_tg           | 913 ms                                                       | 522 ms: 1.75x faster                                               |
| gc_traversal               | 3.14 ms                                                      | 1.89 ms: 1.66x faster                                              |
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 225 ms: 1.49x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 283 ms: 1.46x faster                                               |
| async_tree_none            | 354 ms                                                       | 259 ms: 1.36x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 514 ms: 1.30x faster                                               |
| deepcopy                   | 355 us                                                       | 297 us: 1.20x faster                                               |
| go                         | 141 ms                                                       | 124 ms: 1.14x faster                                               |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                              |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.7 ms: 1.09x faster                                              |
| deepcopy_memo              | 39.1 us                                                      | 35.7 us: 1.09x faster                                              |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                               |
| regex_v8                   | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                              |
| float                      | 77.5 ms                                                      | 71.2 ms: 1.09x faster                                              |
| sqlite_synth               | 2.21 us                                                      | 2.07 us: 1.06x faster                                              |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                               |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                               |
| dulwich_log                | 74.8 ms                                                      | 72.0 ms: 1.04x faster                                              |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                               |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                              |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                               |
| deepcopy_reduce            | 3.11 us                                                      | 3.06 us: 1.02x faster                                              |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                               |
| bpe_tokeniser              | 4.45 sec                                                     | 4.44 sec: 1.00x faster                                             |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                             |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                              |
| docutils                   | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                             |
| scimark_fft                | 349 ms                                                       | 362 ms: 1.04x slower                                               |
| generators                 | 28.8 ms                                                      | 30.1 ms: 1.05x slower                                              |
| json                       | 4.93 ms                                                      | 5.22 ms: 1.06x slower                                              |
| pprint_safe_repr           | 738 ms                                                       | 784 ms: 1.06x slower                                               |
| tomli_loads                | 2.01 sec                                                     | 2.16 sec: 1.07x slower                                             |
| pyflate                    | 449 ms                                                       | 482 ms: 1.08x slower                                               |
| chaos                      | 57.3 ms                                                      | 62.1 ms: 1.08x slower                                              |
| pprint_pformat             | 1.50 sec                                                     | 1.62 sec: 1.09x slower                                             |
| create_gc_cycles           | 1.34 ms                                                      | 1.46 ms: 1.09x slower                                              |
| unpickle_pure_python       | 210 us                                                       | 230 us: 1.09x slower                                               |
| 2to3                       | 260 ms                                                       | 284 ms: 1.09x slower                                               |
| hexiom                     | 5.99 ms                                                      | 6.58 ms: 1.10x slower                                              |
| regex_compile              | 132 ms                                                       | 145 ms: 1.10x slower                                               |
| telco                      | 7.82 ms                                                      | 8.69 ms: 1.11x slower                                              |
| sympy_integrate            | 19.8 ms                                                      | 22.2 ms: 1.12x slower                                              |
| richards                   | 45.2 ms                                                      | 50.7 ms: 1.12x slower                                              |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.27 ms: 1.12x slower                                              |
| nqueens                    | 78.6 ms                                                      | 88.2 ms: 1.12x slower                                              |
| richards_super             | 51.6 ms                                                      | 58.2 ms: 1.13x slower                                              |
| thrift                     | 778 us                                                       | 879 us: 1.13x slower                                               |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                              |
| genshi_xml                 | 48.8 ms                                                      | 55.5 ms: 1.14x slower                                              |
| deltablue                  | 3.12 ms                                                      | 3.56 ms: 1.14x slower                                              |
| xml_etree_generate         | 85.4 ms                                                      | 97.4 ms: 1.14x slower                                              |
| pickle_pure_python         | 294 us                                                       | 336 us: 1.14x slower                                               |
| scimark_lu                 | 113 ms                                                       | 129 ms: 1.15x slower                                               |
| sympy_str                  | 275 ms                                                       | 316 ms: 1.15x slower                                               |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                               |
| sympy_expand               | 457 ms                                                       | 534 ms: 1.17x slower                                               |
| xml_etree_process          | 59.3 ms                                                      | 69.7 ms: 1.17x slower                                              |
| comprehensions             | 16.5 us                                                      | 19.4 us: 1.18x slower                                              |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.1 ms: 1.18x slower                                              |
| raytrace                   | 253 ms                                                       | 300 ms: 1.19x slower                                               |
| django_template            | 34.1 ms                                                      | 40.9 ms: 1.20x slower                                              |
| genshi_text                | 21.5 ms                                                      | 26.2 ms: 1.22x slower                                              |
| typing_runtime_protocols   | 155 us                                                       | 191 us: 1.23x slower                                               |
| meteor_contest             | 102 ms                                                       | 127 ms: 1.25x slower                                               |
| json_dumps                 | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                              |
| logging_simple             | 6.16 us                                                      | 7.75 us: 1.26x slower                                              |
| logging_format             | 6.84 us                                                      | 8.64 us: 1.26x slower                                              |
| crypto_pyaes               | 67.9 ms                                                      | 85.8 ms: 1.26x slower                                              |
| fannkuch                   | 370 ms                                                       | 470 ms: 1.27x slower                                               |
| python_startup_no_site     | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                              |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.33x slower                                               |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                              |
| nbody                      | 85.1 ms                                                      | 121 ms: 1.42x slower                                               |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                              |
| bench_thread_pool          | 919 us                                                       | 3.13 ms: 3.41x slower                                              |
| logging_silent             | 103 ns                                                       | 538 ns: 5.25x slower                                               |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.34x slower                                               |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                       |

Benchmark hidden because not significant (2): pylint, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-7723ceb-NOGIL/bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.026x slower

# HPT report

- Reliability score: 96.40% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x