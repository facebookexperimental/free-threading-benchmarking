# Results vs. 3.13.0rc2

- fork: DinoV
- ref: lazy_imports
- machine: linux-x86_64
- commit hash: 27836e5
- commit date: 2025-09-22
- overall geometric mean: 1.034x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                       |
| html5lib       | 67.0 ms                                                      | 61.4 ms: 1.09x faster                                        |
| Geometric mean | (ref)                                                        | 1.06x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                         |
| async_tree_io_tg           | 913 ms                                                       | 627 ms: 1.46x faster                                         |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                         |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.34x faster                                         |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                         |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 503 ms: 1.33x faster                                         |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                         |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 508 ms: 1.26x faster                                         |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                         |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                         |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                        |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 197 ms: 1.10x faster                                         |
| float          | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                        |
| nbody          | 85.1 ms                                                      | 90.7 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                        | 1.03x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.67 ms: 1.16x faster                                        |
| regex_v8       | 22.7 ms                                                      | 21.1 ms: 1.08x faster                                        |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                         |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                         |
| Geometric mean | (ref)                                                        | 1.09x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.58 ms: 1.10x faster                                        |
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                       |
| xml_etree_generate   | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                        |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                        |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                         |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.2 ms: 1.02x faster                                        |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                         |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                        |
| pickle_pure_python   | 294 us                                                       | 307 us: 1.04x slower                                         |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                        |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                        |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                        |
| genshi_xml      | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                        |
| django_template | 34.1 ms                                                      | 34.0 ms: 1.01x faster                                        |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                       |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.49x faster                                        |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                         |
| deepcopy                   | 355 us                                                       | 242 us: 1.47x faster                                         |
| async_tree_io_tg           | 913 ms                                                       | 627 ms: 1.46x faster                                         |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                         |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.34x faster                                         |
| go                         | 141 ms                                                       | 105 ms: 1.33x faster                                         |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.33x faster                                         |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 503 ms: 1.33x faster                                         |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                         |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 508 ms: 1.26x faster                                         |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.23x faster                                         |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.20x faster                                        |
| spectral_norm              | 111 ms                                                       | 94.7 ms: 1.17x faster                                        |
| regex_effbot               | 3.08 ms                                                      | 2.67 ms: 1.16x faster                                        |
| pylint                     | 317 ms                                                       | 279 ms: 1.13x faster                                         |
| dulwich_log                | 74.8 ms                                                      | 66.2 ms: 1.13x faster                                        |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                         |
| pidigits                   | 217 ms                                                       | 197 ms: 1.10x faster                                         |
| json_dumps                 | 10.5 ms                                                      | 9.58 ms: 1.10x faster                                        |
| pyflate                    | 449 ms                                                       | 410 ms: 1.09x faster                                         |
| html5lib                   | 67.0 ms                                                      | 61.4 ms: 1.09x faster                                        |
| richards                   | 45.2 ms                                                      | 41.5 ms: 1.09x faster                                        |
| richards_super             | 51.6 ms                                                      | 47.5 ms: 1.09x faster                                        |
| regex_v8                   | 22.7 ms                                                      | 21.1 ms: 1.08x faster                                        |
| float                      | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                        |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                         |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                        |
| pprint_safe_repr           | 738 ms                                                       | 694 ms: 1.06x faster                                         |
| hexiom                     | 5.99 ms                                                      | 5.66 ms: 1.06x faster                                        |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                       |
| logging_simple             | 6.16 us                                                      | 5.84 us: 1.06x faster                                        |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.9 ms: 1.06x faster                                        |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.05x faster                                        |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.05x faster                                       |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                         |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.04x faster                                        |
| logging_format             | 6.84 us                                                      | 6.56 us: 1.04x faster                                        |
| comprehensions             | 16.5 us                                                      | 15.8 us: 1.04x faster                                        |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                       |
| scimark_fft                | 349 ms                                                       | 337 ms: 1.04x faster                                         |
| generators                 | 28.8 ms                                                      | 27.9 ms: 1.03x faster                                        |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                       |
| typing_runtime_protocols   | 155 us                                                       | 151 us: 1.03x faster                                         |
| meteor_contest             | 102 ms                                                       | 98.9 ms: 1.03x faster                                        |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                       |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                         |
| xml_etree_generate         | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                        |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                        |
| xml_etree_parse            | 136 ms                                                       | 134 ms: 1.02x faster                                         |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.2 ms: 1.02x faster                                        |
| sympy_str                  | 275 ms                                                       | 270 ms: 1.02x faster                                         |
| logging_silent             | 103 ns                                                       | 101 ns: 1.02x faster                                         |
| python_startup_no_site     | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                        |
| coverage                   | 83.0 ms                                                      | 81.8 ms: 1.01x faster                                        |
| thrift                     | 778 us                                                       | 768 us: 1.01x faster                                         |
| chaos                      | 57.3 ms                                                      | 56.7 ms: 1.01x faster                                        |
| nqueens                    | 78.6 ms                                                      | 77.8 ms: 1.01x faster                                        |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                         |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                         |
| genshi_xml                 | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                        |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                         |
| django_template            | 34.1 ms                                                      | 34.0 ms: 1.01x faster                                        |
| crypto_pyaes               | 67.9 ms                                                      | 68.4 ms: 1.01x slower                                        |
| json                       | 4.93 ms                                                      | 5.02 ms: 1.02x slower                                        |
| sympy_expand               | 457 ms                                                       | 466 ms: 1.02x slower                                         |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                        |
| fannkuch                   | 370 ms                                                       | 378 ms: 1.02x slower                                         |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.89 ms: 1.04x slower                                        |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                        |
| pickle_pure_python         | 294 us                                                       | 307 us: 1.04x slower                                         |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                        |
| nbody                      | 85.1 ms                                                      | 90.7 ms: 1.07x slower                                        |
| deltablue                  | 3.12 ms                                                      | 3.36 ms: 1.08x slower                                        |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                        |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                        |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                        |
| create_gc_cycles           | 1.34 ms                                                      | 1.95 ms: 1.46x slower                                        |
| gc_traversal               | 3.14 ms                                                      | 4.75 ms: 1.51x slower                                        |
| telco                      | 7.82 ms                                                      | 158 ms: 20.18x slower                                        |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                 |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mako, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (9) of results/bm-20250922-3.15.0a0-27836e5/bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5.json: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x