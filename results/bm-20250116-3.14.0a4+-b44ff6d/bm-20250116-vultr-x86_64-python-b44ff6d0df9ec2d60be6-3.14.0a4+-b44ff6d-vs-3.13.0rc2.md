# Results vs. 3.13.0rc2

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.052x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 616 ms: 1.48x faster                                                   |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 329 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                   |
| async_tree_none            | 354 ms                                                       | 274 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 511 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 534 ms: 1.25x faster                                                   |
| async_generators           | 377 ms                                                       | 321 ms: 1.18x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.3 ms: 1.11x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.2 ms: 1.07x faster                                                  |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                                   |
| nbody          | 85.1 ms                                                      | 86.5 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.61 ms: 1.18x faster                                                  |
| regex_dna      | 180 ms                                                       | 170 ms: 1.06x faster                                                   |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 84.4 ms: 1.01x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 217 us: 1.03x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 316 us: 1.07x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 616 ms: 1.48x faster                                                   |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 329 ms: 1.40x faster                                                   |
| deepcopy                   | 355 us                                                       | 259 us: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.2 us: 1.29x faster                                                  |
| async_tree_none            | 354 ms                                                       | 274 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 511 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 534 ms: 1.25x faster                                                   |
| spectral_norm              | 111 ms                                                       | 89.1 ms: 1.25x faster                                                  |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.61 ms: 1.18x faster                                                  |
| async_generators           | 377 ms                                                       | 321 ms: 1.18x faster                                                   |
| scimark_sor                | 134 ms                                                       | 115 ms: 1.17x faster                                                   |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                   |
| scimark_fft                | 349 ms                                                       | 309 ms: 1.13x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.3 ms: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.27 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                   |
| richards                   | 45.2 ms                                                      | 41.7 ms: 1.08x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.24 ms: 1.08x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| richards_super             | 51.6 ms                                                      | 48.1 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.2 ms: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                  |
| regex_dna                  | 180 ms                                                       | 170 ms: 1.06x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 700 ms: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 79.1 ms: 1.05x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.6 ms: 1.05x faster                                                  |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                                   |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| thrift                     | 778 us                                                       | 745 us: 1.05x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.75 ms: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.7 ms: 1.03x faster                                                  |
| meteor_contest             | 102 ms                                                       | 99.3 ms: 1.02x faster                                                  |
| fannkuch                   | 370 ms                                                       | 363 ms: 1.02x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.17 us: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 77.5 ms: 1.01x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 84.4 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.2 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 1.55 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 105 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 52.5 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.5 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.00x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 59.7 ms: 1.01x slower                                                  |
| json                       | 4.93 ms                                                      | 4.97 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.6 ms: 1.01x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.16 ms: 1.01x slower                                                  |
| nbody                      | 85.1 ms                                                      | 86.5 ms: 1.02x slower                                                  |
| logging_format             | 6.84 us                                                      | 6.96 us: 1.02x slower                                                  |
| comprehensions             | 16.5 us                                                      | 16.8 us: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                   |
| json_loads                 | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 217 us: 1.03x slower                                                   |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                   |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.47 sec: 1.05x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 316 us: 1.07x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.45 ms: 1.42x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 88.6 ms: 8.06x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (3): logging_simple, sqlglot_parse, sympy_expand
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.052x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x