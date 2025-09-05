# Results vs. 3.13.0rc2

- fork: python
- ref: fc0305a2d8bef7cffaa4
- machine: linux-x86_64
- commit hash: fc0305a
- commit date: 2025-09-04
- overall geometric mean: 1.036x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.03x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 622 ms: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 609 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 511 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 509 ms: 1.25x faster                                                  |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| pidigits       | 217 ms                                                       | 207 ms: 1.04x faster                                                  |
| nbody          | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                 |
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                        | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.59 ms: 1.10x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| xml_etree_generate   | 85.4 ms                                                      | 82.8 ms: 1.03x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.1 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                 |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                 |
| django_template | 34.1 ms                                                      | 34.6 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                  |
| deepcopy                   | 355 us                                                       | 242 us: 1.47x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.6 us: 1.47x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 622 ms: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 609 ms: 1.44x faster                                                  |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 511 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 509 ms: 1.25x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                 |
| spectral_norm              | 111 ms                                                       | 92.9 ms: 1.20x faster                                                 |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.6 ms: 1.12x faster                                                 |
| pyflate                    | 449 ms                                                       | 402 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.59 ms: 1.10x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.5 ms: 1.09x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.4 ms: 1.09x faster                                                 |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.59 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.5 ms: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| logging_simple             | 6.16 us                                                      | 5.81 us: 1.06x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 696 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                |
| scimark_fft                | 349 ms                                                       | 331 ms: 1.06x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.50 us: 1.05x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                 |
| logging_silent             | 103 ns                                                       | 97.8 ns: 1.05x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                 |
| pidigits                   | 217 ms                                                       | 207 ms: 1.04x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| thrift                     | 778 us                                                       | 750 us: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 251 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.8 ms: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                                |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                |
| coverage                   | 83.0 ms                                                      | 81.0 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.1 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.1 ms: 1.02x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.8 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.5 ms: 1.02x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.7 ms: 1.00x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                  |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                 |
| sympy_expand               | 457 ms                                                       | 462 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.77 ms: 1.01x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.6 ms: 1.01x slower                                                 |
| json                       | 4.93 ms                                                      | 5.01 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 380 ms: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.05x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.65 ms: 1.48x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 97.8 ms: 8.89x slower                                                 |
| telco                      | 7.82 ms                                                      | 158 ms: 20.16x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (3): genshi_xml, raytrace, generators
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x