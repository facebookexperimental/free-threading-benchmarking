# Results vs. 3.13.0rc2

- fork: python
- ref: a7bb524fef61f77ede01
- machine: linux-x86_64
- commit hash: a7bb524
- commit date: 2026-08-17
- overall geometric mean: 1.033x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 259 ms: 1.00x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.35 sec: 1.11x faster                                                |
| html5lib       | 67.0 ms                                                      | 59.8 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 376 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 723 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                  |
| async_tree_none            | 354 ms                                                       | 298 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 551 ms: 1.16x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 364 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 298 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.6 ms: 1.00x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| float          | 77.5 ms                                                      | 73.1 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.55 ms: 1.21x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.04x faster                                                 |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.31 ms: 1.13x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.87 sec: 1.08x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                  |
| json_loads           | 27.0 us                                                      | 27.4 us: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 300 us: 1.02x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 141 ms: 1.03x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 88.4 ms: 1.04x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 62.2 ms: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.10 ms: 1.04x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| django_template | 34.1 ms                                                      | 36.8 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 115 ms: 2.77x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                |
| deepcopy                   | 355 us                                                       | 232 us: 1.53x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.4 us: 1.48x faster                                                 |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 120 us: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                       | 105 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 376 ms: 1.23x faster                                                  |
| spectral_norm              | 111 ms                                                       | 90.8 ms: 1.22x faster                                                 |
| async_tree_io              | 876 ms                                                       | 723 ms: 1.21x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.55 ms: 1.21x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                  |
| async_tree_none            | 354 ms                                                       | 298 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 551 ms: 1.16x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 364 ms: 1.14x faster                                                  |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.31 ms: 1.13x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 298 ms: 1.13x faster                                                  |
| scimark_fft                | 349 ms                                                       | 311 ms: 1.12x faster                                                  |
| pyflate                    | 449 ms                                                       | 400 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.8 ms: 1.12x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.35 sec: 1.11x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 67.2 ms: 1.11x faster                                                 |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                 |
| chaos                      | 57.3 ms                                                      | 53.2 ms: 1.08x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.87 sec: 1.08x faster                                                |
| logging_silent             | 103 ns                                                       | 95.9 ns: 1.07x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 73.8 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 73.1 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.68 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.24 sec: 1.05x faster                                                |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.6 ms: 1.05x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.04x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.10 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.1 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.55 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                 |
| raytrace                   | 253 ms                                                       | 249 ms: 1.02x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.01x faster                                                 |
| richards_super             | 51.6 ms                                                      | 51.2 ms: 1.01x faster                                                 |
| richards                   | 45.2 ms                                                      | 44.9 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                  |
| 2to3                       | 260 ms                                                       | 259 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.6 ms: 1.00x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.50 sec: 1.00x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| fannkuch                   | 370 ms                                                       | 374 ms: 1.01x slower                                                  |
| thrift                     | 778 us                                                       | 787 us: 1.01x slower                                                  |
| coverage                   | 83.0 ms                                                      | 84.2 ms: 1.01x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.02x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 300 us: 1.02x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                  |
| sympy_str                  | 275 ms                                                       | 282 ms: 1.03x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.02 us: 1.03x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 141 ms: 1.03x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 88.4 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.27 ms: 1.05x slower                                                 |
| sympy_expand               | 457 ms                                                       | 479 ms: 1.05x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 62.2 ms: 1.05x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 119 ms: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.8 ms: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.71 ms: 1.18x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.64 ms: 1.23x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.47x slower                                                 |
| telco                      | 7.82 ms                                                      | 160 ms: 20.49x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 237 ms: 21.56x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (6): json, logging_simple, regex_dna, meteor_contest, sqlite_synth, pprint_safe_repr
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x