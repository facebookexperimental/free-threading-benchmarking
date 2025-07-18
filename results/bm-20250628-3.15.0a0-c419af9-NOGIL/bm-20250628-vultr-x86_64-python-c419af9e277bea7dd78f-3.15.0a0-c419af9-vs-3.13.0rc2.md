# Results vs. 3.13.0rc2

- fork: python
- ref: c419af9e277bea7dd78f
- machine: linux-x86_64
- commit hash: c419af9
- commit date: 2025-06-28
- overall geometric mean: 1.012x slower
- HPT reliability: 94.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| html5lib       | 67.0 ms                                                      | 65.4 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 519 ms: 1.76x faster                                                  |
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 225 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 282 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 462 ms: 1.38x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                  |
| async_generators           | 377 ms                                                       | 368 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| float          | 77.5 ms                                                      | 69.7 ms: 1.11x faster                                                 |
| nbody          | 85.1 ms                                                      | 123 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.1 ms: 1.13x faster                                                 |
| regex_dna      | 180 ms                                                       | 163 ms: 1.10x faster                                                  |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 86.6 ms: 1.10x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                                |
| unpickle_pure_python | 210 us                                                       | 233 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 95.0 ms: 1.11x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 335 us: 1.14x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 12.0 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                 |
| json_loads           | 27.0 us                                                      | 31.3 us: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 39.3 ms: 1.15x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 58.2 ms: 1.19x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                 |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.79x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 519 ms: 1.76x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.92 ms: 1.64x faster                                                 |
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 225 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 282 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 462 ms: 1.38x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                  |
| deepcopy                   | 355 us                                                       | 295 us: 1.21x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.60 ms: 1.19x faster                                                 |
| go                         | 141 ms                                                       | 120 ms: 1.17x faster                                                  |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.1 ms: 1.13x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 34.8 us: 1.12x faster                                                 |
| float                      | 77.5 ms                                                      | 69.7 ms: 1.11x faster                                                 |
| regex_dna                  | 180 ms                                                       | 163 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.6 ms: 1.10x faster                                                 |
| scimark_sor                | 134 ms                                                       | 124 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.6 ms: 1.05x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 65.4 ms: 1.02x faster                                                 |
| async_generators           | 377 ms                                                       | 368 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.04 us: 1.02x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.36 sec: 1.02x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| generators                 | 28.8 ms                                                      | 29.5 ms: 1.02x slower                                                 |
| pyflate                    | 449 ms                                                       | 461 ms: 1.03x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| spectral_norm              | 111 ms                                                       | 115 ms: 1.03x slower                                                  |
| scimark_fft                | 349 ms                                                       | 366 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 778 ms: 1.05x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.4 us: 1.06x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.34 ms: 1.06x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.61 sec: 1.08x slower                                                |
| telco                      | 7.82 ms                                                      | 8.45 ms: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| json                       | 4.93 ms                                                      | 5.35 ms: 1.09x slower                                                 |
| 2to3                       | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.1 ms: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.8 ms: 1.10x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 86.7 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 233 us: 1.11x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.48 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 95.0 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.25 ms: 1.11x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.50 ms: 1.12x slower                                                 |
| thrift                     | 778 us                                                       | 874 us: 1.12x slower                                                  |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                  |
| sympy_expand               | 457 ms                                                       | 517 ms: 1.13x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.98 us: 1.13x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 335 us: 1.14x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.14x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.5 ms: 1.14x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 12.0 ms: 1.14x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 178 ms: 1.15x slower                                                  |
| django_template            | 34.1 ms                                                      | 39.3 ms: 1.15x slower                                                 |
| logging_format             | 6.84 us                                                      | 7.89 us: 1.15x slower                                                 |
| richards_super             | 51.6 ms                                                      | 59.6 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.3 us: 1.16x slower                                                 |
| meteor_contest             | 102 ms                                                       | 119 ms: 1.17x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 76.9 ms: 1.18x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 58.2 ms: 1.19x slower                                                 |
| raytrace                   | 253 ms                                                       | 302 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 189 us: 1.22x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                 |
| fannkuch                   | 370 ms                                                       | 464 ms: 1.25x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.7 ms: 1.29x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                 |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.33x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| nbody                      | 85.1 ms                                                      | 123 ms: 1.45x slower                                                  |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.15 ms: 3.43x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 104 ms: 9.49x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                          |

Benchmark hidden because not significant (2): pylint, logging_silent
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.012x slower

# HPT report

- Reliability score: 94.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x