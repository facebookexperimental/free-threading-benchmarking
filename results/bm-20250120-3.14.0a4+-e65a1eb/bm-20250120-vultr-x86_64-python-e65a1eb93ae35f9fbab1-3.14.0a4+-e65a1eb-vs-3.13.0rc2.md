# Results vs. 3.13.0rc2

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.057x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                   |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                   |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                   |
| async_generators           | 377 ms                                                       | 318 ms: 1.18x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.07x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                  |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                                   |
| nbody          | 85.1 ms                                                      | 91.2 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                  |
| regex_dna      | 180 ms                                                       | 169 ms: 1.06x faster                                                   |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 60.3 ms: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.05x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.0 ms: 1.01x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                   |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.44x faster                                                   |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 493 ms: 1.35x faster                                                   |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.9 us: 1.31x faster                                                  |
| go                         | 141 ms                                                       | 112 ms: 1.26x faster                                                   |
| scimark_sor                | 134 ms                                                       | 111 ms: 1.21x faster                                                   |
| spectral_norm              | 111 ms                                                       | 92.2 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.60 us: 1.20x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                  |
| async_generators           | 377 ms                                                       | 318 ms: 1.18x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.10 ms: 1.15x faster                                                  |
| scimark_fft                | 349 ms                                                       | 305 ms: 1.15x faster                                                   |
| pylint                     | 317 ms                                                       | 279 ms: 1.13x faster                                                   |
| float                      | 77.5 ms                                                      | 69.8 ms: 1.11x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.0 ms: 1.10x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.2 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                       | 415 ms: 1.08x faster                                                   |
| telco                      | 7.82 ms                                                      | 7.28 ms: 1.07x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.06x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.70 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 703 ms: 1.05x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.5 ms: 1.05x faster                                                  |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                                   |
| chaos                      | 57.3 ms                                                      | 54.8 ms: 1.05x faster                                                  |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| coverage                   | 83.0 ms                                                      | 79.6 ms: 1.04x faster                                                  |
| meteor_contest             | 102 ms                                                       | 97.4 ms: 1.04x faster                                                  |
| thrift                     | 778 us                                                       | 749 us: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.2 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                 |
| mdp                        | 2.36 sec                                                     | 2.30 sec: 1.02x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.05 ms: 1.02x faster                                                  |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 76.9 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.01x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 67.0 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 52.4 ms: 1.01x faster                                                  |
| fannkuch                   | 370 ms                                                       | 367 ms: 1.01x faster                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 1.55 ms: 1.01x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.00x faster                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.0 ms: 1.01x slower                                                  |
| sympy_expand               | 457 ms                                                       | 459 ms: 1.01x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| comprehensions             | 16.5 us                                                      | 16.6 us: 1.01x slower                                                  |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                  |
| logging_silent             | 103 ns                                                       | 104 ns: 1.01x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.02x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 60.3 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 76.5 ms: 1.02x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.36 us: 1.03x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.18 us: 1.05x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 221 us: 1.05x slower                                                   |
| nbody                      | 85.1 ms                                                      | 91.2 ms: 1.07x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.99 ms: 1.27x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 89.7 ms: 8.16x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (3): sympy_str, sqlglot_parse, sympy_integrate
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x