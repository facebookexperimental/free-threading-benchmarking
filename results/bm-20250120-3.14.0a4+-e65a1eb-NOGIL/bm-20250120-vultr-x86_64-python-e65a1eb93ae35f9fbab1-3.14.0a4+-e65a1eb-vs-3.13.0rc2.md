# Results vs. 3.13.0rc2

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.110x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 313 ms: 1.21x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                                 |
| html5lib       | 67.0 ms                                                      | 72.5 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 580 ms: 1.57x faster                                                   |
| async_tree_io              | 876 ms                                                       | 611 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                   |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 569 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.11x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 25.0 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 217 ms: 1.00x slower                                                   |
| nbody          | 85.1 ms                                                      | 137 ms: 1.62x slower                                                   |
| Geometric mean | (ref)                                                        | 1.17x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| regex_compile  | 132 ms                                                       | 159 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| json_loads           | 27.0 us                                                      | 30.6 us: 1.13x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 98.9 ms: 1.16x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.43 sec: 1.21x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.24x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 75.3 ms: 1.27x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 280 us: 1.33x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 395 us: 1.34x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                  |
| django_template | 34.1 ms                                                      | 44.8 ms: 1.31x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 29.8 ms: 1.38x slower                                                  |
| mako            | 11.3 ms                                                      | 16.3 ms: 1.44x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.35x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 580 ms: 1.57x faster                                                   |
| async_tree_io              | 876 ms                                                       | 611 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                   |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 569 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.11x faster                                                   |
| deepcopy                   | 355 us                                                       | 323 us: 1.10x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.07 us: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.7 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                                   |
| pidigits                   | 217 ms                                                       | 217 ms: 1.00x slower                                                   |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| go                         | 141 ms                                                       | 142 ms: 1.01x slower                                                   |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.01x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.9 us: 1.02x slower                                                  |
| scimark_sor                | 134 ms                                                       | 140 ms: 1.04x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 25.0 ms: 1.06x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.37 ms: 1.07x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.80 sec: 1.08x slower                                                 |
| json                       | 4.93 ms                                                      | 5.33 ms: 1.08x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 72.5 ms: 1.08x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.38 us: 1.08x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.10x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                                  |
| pyflate                    | 449 ms                                                       | 504 ms: 1.12x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 84.5 ms: 1.13x slower                                                  |
| scimark_fft                | 349 ms                                                       | 395 ms: 1.13x slower                                                   |
| json_loads                 | 27.0 us                                                      | 30.6 us: 1.13x slower                                                  |
| logging_silent             | 103 ns                                                       | 118 ns: 1.15x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 98.9 ms: 1.16x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.5 ms: 1.16x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 123 ms: 1.17x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 861 ms: 1.17x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.79 sec: 1.19x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.78 sec: 1.19x slower                                                 |
| coverage                   | 83.0 ms                                                      | 98.9 ms: 1.19x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 63.1 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.64 ms: 1.20x slower                                                  |
| regex_compile              | 132 ms                                                       | 159 ms: 1.20x slower                                                   |
| thrift                     | 778 us                                                       | 939 us: 1.21x slower                                                   |
| 2to3                       | 260 ms                                                       | 313 ms: 1.21x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.43 sec: 1.21x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 191 ms: 1.23x slower                                                   |
| sympy_expand               | 457 ms                                                       | 565 ms: 1.24x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.24x slower                                                  |
| sympy_str                  | 275 ms                                                       | 343 ms: 1.25x slower                                                   |
| chaos                      | 57.3 ms                                                      | 71.6 ms: 1.25x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 24.8 ms: 1.25x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.95 ms: 1.25x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 98.8 ms: 1.26x slower                                                  |
| richards                   | 45.2 ms                                                      | 56.9 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.3 ms: 1.27x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 7.60 ms: 1.27x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 143 ms: 1.27x slower                                                   |
| richards_super             | 51.6 ms                                                      | 65.7 ms: 1.27x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 83.2 ms: 1.27x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.87 us: 1.28x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.8 ms: 1.29x slower                                                  |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 1.62 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                  |
| comprehensions             | 16.5 us                                                      | 21.4 us: 1.30x slower                                                  |
| django_template            | 34.1 ms                                                      | 44.8 ms: 1.31x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.99 us: 1.31x slower                                                  |
| raytrace                   | 253 ms                                                       | 334 ms: 1.32x slower                                                   |
| fannkuch                   | 370 ms                                                       | 492 ms: 1.33x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 280 us: 1.33x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 395 us: 1.34x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 210 us: 1.36x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 29.8 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.3 ms: 1.44x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.77 ms: 1.53x slower                                                  |
| nbody                      | 85.1 ms                                                      | 137 ms: 1.62x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.35 ms: 3.65x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 95.7 ms: 8.71x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.17x slower                                                           |

Benchmark hidden because not significant (3): float, create_gc_cycles, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.110x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.34x