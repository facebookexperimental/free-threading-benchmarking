# Results vs. 3.13.0rc2

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.077x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 302 ms: 1.16x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.79 sec: 1.07x slower                                                 |
| html5lib       | 67.0 ms                                                      | 69.4 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 576 ms: 1.59x faster                                                   |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 349 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 532 ms: 1.25x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| async_generators           | 377 ms                                                       | 367 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                   |
| float          | 77.5 ms                                                      | 73.4 ms: 1.05x faster                                                  |
| nbody          | 85.1 ms                                                      | 134 ms: 1.57x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                  |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.7 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.1 ms: 1.13x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.30 sec: 1.15x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.7 ms: 1.16x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 245 us: 1.17x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 12.7 ms: 1.21x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 373 us: 1.27x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.2 ms: 1.24x slower                                                  |
| django_template | 34.1 ms                                                      | 43.4 ms: 1.27x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                                  |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 576 ms: 1.59x faster                                                   |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 349 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 532 ms: 1.25x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| deepcopy                   | 355 us                                                       | 310 us: 1.15x faster                                                   |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.03 us: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.7 ms: 1.08x faster                                                  |
| spectral_norm              | 111 ms                                                       | 103 ms: 1.08x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| float                      | 77.5 ms                                                      | 73.4 ms: 1.05x faster                                                  |
| go                         | 141 ms                                                       | 136 ms: 1.04x faster                                                   |
| scimark_sor                | 134 ms                                                       | 130 ms: 1.04x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 37.9 us: 1.03x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                                  |
| async_generators           | 377 ms                                                       | 367 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                   |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 69.4 ms: 1.04x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.24 us: 1.04x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.72 sec: 1.06x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.06x slower                                                 |
| scimark_fft                | 349 ms                                                       | 372 ms: 1.07x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.79 sec: 1.07x slower                                                 |
| logging_silent             | 103 ns                                                       | 110 ns: 1.07x slower                                                   |
| json                       | 4.93 ms                                                      | 5.34 ms: 1.08x slower                                                  |
| generators                 | 28.8 ms                                                      | 31.3 ms: 1.09x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.52 ms: 1.09x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 81.9 ms: 1.09x slower                                                  |
| pyflate                    | 449 ms                                                       | 491 ms: 1.10x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 816 ms: 1.11x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.68 sec: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.1 ms: 1.13x slower                                                  |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                   |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.69 sec: 1.14x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.14x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.30 sec: 1.15x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.7 ms: 1.16x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.15 us: 1.16x slower                                                  |
| 2to3                       | 260 ms                                                       | 302 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 61.5 ms: 1.17x slower                                                  |
| thrift                     | 778 us                                                       | 908 us: 1.17x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 245 us: 1.17x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.50 ms: 1.17x slower                                                  |
| coverage                   | 83.0 ms                                                      | 98.0 ms: 1.18x slower                                                  |
| chaos                      | 57.3 ms                                                      | 67.7 ms: 1.18x slower                                                  |
| sympy_expand               | 457 ms                                                       | 543 ms: 1.19x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 134 ms: 1.19x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                   |
| logging_format             | 6.84 us                                                      | 8.18 us: 1.20x slower                                                  |
| sympy_str                  | 275 ms                                                       | 332 ms: 1.21x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 12.7 ms: 1.21x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.89 ms: 1.21x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 7.36 ms: 1.23x slower                                                  |
| richards                   | 45.2 ms                                                      | 55.6 ms: 1.23x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 96.8 ms: 1.23x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.6 ms: 1.23x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 60.2 ms: 1.24x slower                                                  |
| richards_super             | 51.6 ms                                                      | 64.7 ms: 1.25x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.57 ms: 1.26x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 373 us: 1.27x slower                                                   |
| comprehensions             | 16.5 us                                                      | 20.9 us: 1.27x slower                                                  |
| django_template            | 34.1 ms                                                      | 43.4 ms: 1.27x slower                                                  |
| fannkuch                   | 370 ms                                                       | 471 ms: 1.28x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                                  |
| raytrace                   | 253 ms                                                       | 323 ms: 1.28x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 87.2 ms: 1.28x slower                                                  |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.54 ms: 1.29x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.60 ms: 1.47x slower                                                  |
| nbody                      | 85.1 ms                                                      | 134 ms: 1.57x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 94.2 ms: 8.57x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (3): gc_traversal, create_gc_cycles, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x