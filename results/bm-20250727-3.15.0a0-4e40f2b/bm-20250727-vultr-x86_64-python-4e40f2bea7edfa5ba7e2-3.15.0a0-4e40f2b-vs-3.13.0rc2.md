# Results vs. 3.13.0rc2

- fork: python
- ref: 4e40f2bea7edfa5ba7e2
- machine: linux-x86_64
- commit hash: 4e40f2b
- commit date: 2025-07-27
- overall geometric mean: 1.031x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 62.3 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 596 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 622 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                  |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 259 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 501 ms: 1.27x faster                                                  |
| async_generators           | 377 ms                                                       | 341 ms: 1.10x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 70.5 ms: 1.10x faster                                                 |
| nbody          | 85.1 ms                                                      | 89.5 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.65 ms: 1.17x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.3 ms: 1.06x faster                                                 |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.3 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.1 ms: 1.02x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.5 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                 |
| django_template | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 49.4 ms: 1.01x slower                                                 |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                |
| async_tree_io              | 876 ms                                                       | 596 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 622 ms: 1.47x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 28.5 us: 1.37x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                  |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 259 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 501 ms: 1.27x faster                                                  |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.25x faster                                                  |
| spectral_norm              | 111 ms                                                       | 94.5 ms: 1.18x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.65 ms: 1.17x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.68 us: 1.16x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.2 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                       | 401 ms: 1.12x faster                                                  |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 341 ms: 1.10x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.1 ms: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 70.5 ms: 1.10x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.1 ms: 1.10x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 62.3 ms: 1.08x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 691 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| regex_v8                   | 22.7 ms                                                      | 21.3 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.67 ms: 1.06x faster                                                 |
| logging_silent             | 103 ns                                                       | 97.5 ns: 1.05x faster                                                 |
| scimark_fft                | 349 ms                                                       | 332 ms: 1.05x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.0 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                 |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| thrift                     | 778 us                                                       | 757 us: 1.03x faster                                                  |
| logging_simple             | 6.16 us                                                      | 6.00 us: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.0 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.3 ms: 1.03x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.05 ms: 1.02x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 76.9 ms: 1.02x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.1 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.2 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.1 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| sympy_str                  | 275 ms                                                       | 270 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.5 ms: 1.02x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.01x faster                                                |
| raytrace                   | 253 ms                                                       | 249 ms: 1.01x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.5 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.0 ms: 1.01x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 154 us: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.5 ms: 1.01x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 49.4 ms: 1.01x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.8 ms: 1.01x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                 |
| sympy_expand               | 457 ms                                                       | 464 ms: 1.02x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 381 ms: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.10 ms: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.30 us: 1.04x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.5 ms: 1.05x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.01 ms: 1.06x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.97 ms: 1.47x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.73 ms: 1.50x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.34x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.49x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): logging_format
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x