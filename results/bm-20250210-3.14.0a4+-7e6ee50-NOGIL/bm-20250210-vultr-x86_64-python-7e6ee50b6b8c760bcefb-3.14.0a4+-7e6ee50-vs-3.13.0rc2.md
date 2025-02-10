# Results vs. 3.13.0rc2

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.075x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 301 ms: 1.16x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.79 sec: 1.07x slower                                                 |
| html5lib       | 67.0 ms                                                      | 68.8 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 571 ms: 1.60x faster                                                   |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 349 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 537 ms: 1.24x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 385 ms: 1.02x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                   |
| float          | 77.5 ms                                                      | 75.8 ms: 1.02x faster                                                  |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                   |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.02x slower                                                  |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.3 us: 1.16x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 245 us: 1.17x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 366 us: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.55 ms: 1.29x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.2 ms: 1.21x slower                                                  |
| django_template | 34.1 ms                                                      | 42.5 ms: 1.25x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 28.0 ms: 1.30x slower                                                  |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.73 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 571 ms: 1.60x faster                                                   |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 349 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 537 ms: 1.24x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| deepcopy                   | 355 us                                                       | 306 us: 1.16x faster                                                   |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 37.7 us: 1.04x faster                                                  |
| float                      | 77.5 ms                                                      | 75.8 ms: 1.02x faster                                                  |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.01x faster                                                   |
| go                         | 141 ms                                                       | 139 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.0 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 3.14 us: 1.01x slower                                                  |
| async_generators           | 377 ms                                                       | 385 ms: 1.02x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.02x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 68.8 ms: 1.03x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.67 sec: 1.05x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.79 sec: 1.07x slower                                                 |
| json                       | 4.93 ms                                                      | 5.38 ms: 1.09x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 81.8 ms: 1.09x slower                                                  |
| pyflate                    | 449 ms                                                       | 491 ms: 1.09x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 808 ms: 1.10x slower                                                   |
| generators                 | 28.8 ms                                                      | 31.6 ms: 1.10x slower                                                  |
| logging_silent             | 103 ns                                                       | 113 ns: 1.10x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.62 ms: 1.10x slower                                                  |
| scimark_fft                | 349 ms                                                       | 388 ms: 1.11x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.67 sec: 1.12x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.65 sec: 1.12x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 119 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                  |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                   |
| thrift                     | 778 us                                                       | 899 us: 1.16x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.3 us: 1.16x slower                                                  |
| 2to3                       | 260 ms                                                       | 301 ms: 1.16x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 245 us: 1.17x slower                                                   |
| coverage                   | 83.0 ms                                                      | 97.1 ms: 1.17x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 184 ms: 1.18x slower                                                   |
| logging_simple             | 6.16 us                                                      | 7.30 us: 1.19x slower                                                  |
| sympy_expand               | 457 ms                                                       | 544 ms: 1.19x slower                                                   |
| chaos                      | 57.3 ms                                                      | 68.8 ms: 1.20x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.88 ms: 1.20x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 23.9 ms: 1.21x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.27 us: 1.21x slower                                                  |
| sympy_str                  | 275 ms                                                       | 333 ms: 1.21x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 59.2 ms: 1.21x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                  |
| comprehensions             | 16.5 us                                                      | 20.1 us: 1.22x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 96.1 ms: 1.22x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 138 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.80 ms: 1.23x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 7.40 ms: 1.24x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 366 us: 1.24x slower                                                   |
| django_template            | 34.1 ms                                                      | 42.5 ms: 1.25x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.56 ms: 1.25x slower                                                  |
| richards                   | 45.2 ms                                                      | 56.5 ms: 1.25x slower                                                  |
| richards_super             | 51.6 ms                                                      | 65.1 ms: 1.26x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 82.4 ms: 1.26x slower                                                  |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 87.2 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.55 ms: 1.29x slower                                                  |
| raytrace                   | 253 ms                                                       | 326 ms: 1.29x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 28.0 ms: 1.30x slower                                                  |
| fannkuch                   | 370 ms                                                       | 490 ms: 1.32x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.70 ms: 1.50x slower                                                  |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.62x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 94.3 ms: 8.58x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (2): scimark_sor, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x