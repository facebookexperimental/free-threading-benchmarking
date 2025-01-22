# Results vs. 3.13.0rc2

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.054x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 598 ms: 1.46x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                   |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                   |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.6 ms: 1.09x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.7 ms: 1.11x faster                                                  |
| pidigits       | 217 ms                                                       | 198 ms: 1.09x faster                                                   |
| nbody          | 85.1 ms                                                      | 90.7 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.0 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.94 sec: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.0 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 60.4 ms: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.05x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 598 ms: 1.46x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.45x faster                                                   |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                   |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.8 us: 1.31x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                   |
| go                         | 141 ms                                                       | 113 ms: 1.25x faster                                                   |
| spectral_norm              | 111 ms                                                       | 90.1 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.22x faster                                                  |
| scimark_sor                | 134 ms                                                       | 112 ms: 1.20x faster                                                   |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                   |
| pylint                     | 317 ms                                                       | 279 ms: 1.13x faster                                                   |
| scimark_fft                | 349 ms                                                       | 313 ms: 1.12x faster                                                   |
| float                      | 77.5 ms                                                      | 69.7 ms: 1.11x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.3 ms: 1.09x faster                                                  |
| pidigits                   | 217 ms                                                       | 198 ms: 1.09x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.6 ms: 1.09x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.6 ms: 1.09x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.21 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.38 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                   |
| thrift                     | 778 us                                                       | 734 us: 1.06x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 697 ms: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.0 ms: 1.06x faster                                                  |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| generators                 | 28.8 ms                                                      | 27.5 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.25 sec: 1.05x faster                                                 |
| chaos                      | 57.3 ms                                                      | 54.9 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.7 ms: 1.04x faster                                                  |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.94 sec: 1.04x faster                                                 |
| coverage                   | 83.0 ms                                                      | 80.2 ms: 1.03x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.80 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.0 ms: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.52 ms: 1.02x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.22 ms: 1.02x faster                                                  |
| logging_silent             | 103 ns                                                       | 101 ns: 1.02x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 3.06 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.01x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                   |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 67.4 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.1 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 52.6 ms: 1.00x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                  |
| fannkuch                   | 370 ms                                                       | 371 ms: 1.00x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                   |
| json                       | 4.93 ms                                                      | 4.97 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.01x slower                                                   |
| comprehensions             | 16.5 us                                                      | 16.7 us: 1.01x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.9 ms: 1.01x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 60.4 ms: 1.02x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                  |
| raytrace                   | 253 ms                                                       | 258 ms: 1.02x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.09 us: 1.04x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.44 sec: 1.04x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.39 us: 1.04x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 221 us: 1.05x slower                                                   |
| nbody                      | 85.1 ms                                                      | 90.7 ms: 1.07x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.29 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 89.0 ms: 8.09x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (4): meteor_contest, sympy_expand, genshi_text, scimark_lu
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.054x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x