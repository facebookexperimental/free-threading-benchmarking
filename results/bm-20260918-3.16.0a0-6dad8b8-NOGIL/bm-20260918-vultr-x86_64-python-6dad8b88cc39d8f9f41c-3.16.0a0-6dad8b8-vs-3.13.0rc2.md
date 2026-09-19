# Results vs. 3.13.0rc2

- fork: python
- ref: 6dad8b88cc39d8f9f41c
- machine: linux-x86_64
- commit hash: 6dad8b8
- commit date: 2026-09-18
- overall geometric mean: 1.076x slower
- HPT reliability: 98.79%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 296 ms: 1.14x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.94 sec: 1.12x slower                                                |
| html5lib       | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 705 ms: 1.30x faster                                                  |
| async_tree_io              | 876 ms                                                       | 728 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 614 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 588 ms: 1.08x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 508 ms: 1.02x faster                                                  |
| async_tree_none            | 354 ms                                                       | 375 ms: 1.06x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.6 ms: 1.09x slower                                                 |
| async_generators           | 377 ms                                                       | 415 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 85.1 ms: 1.10x slower                                                 |
| nbody          | 85.1 ms                                                      | 122 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.3 ms: 1.07x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                 |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.99 ms: 1.05x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.96 sec: 1.02x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 141 ms: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.4 us: 1.13x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 238 us: 1.14x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 339 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 99.0 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 74.9 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.73 ms: 1.32x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.4 ms: 1.49x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.0 ms: 1.20x slower                                                 |
| mako            | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.31x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 129 ms: 2.46x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.77 ms: 1.77x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.73 ms: 1.63x faster                                                 |
| deepcopy                   | 355 us                                                       | 267 us: 1.33x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 705 ms: 1.30x faster                                                  |
| async_tree_io              | 876 ms                                                       | 728 ms: 1.20x faster                                                  |
| pidigits                   | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 33.0 us: 1.18x faster                                                 |
| go                         | 141 ms                                                       | 120 ms: 1.18x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.93 us: 1.14x faster                                                 |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 614 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 588 ms: 1.08x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 69.9 ms: 1.07x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.3 ms: 1.07x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.92 us: 1.06x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 147 us: 1.06x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.99 ms: 1.05x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                 |
| spectral_norm              | 111 ms                                                       | 107 ms: 1.04x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                 |
| scimark_fft                | 349 ms                                                       | 341 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 508 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.96 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                |
| html5lib                   | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                 |
| pyflate                    | 449 ms                                                       | 456 ms: 1.02x slower                                                  |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                  |
| logging_silent             | 103 ns                                                       | 105 ns: 1.02x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 141 ms: 1.04x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.39 ms: 1.04x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                |
| chaos                      | 57.3 ms                                                      | 60.6 ms: 1.06x slower                                                 |
| async_tree_none            | 354 ms                                                       | 375 ms: 1.06x slower                                                  |
| json                       | 4.93 ms                                                      | 5.35 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 801 ms: 1.09x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.6 ms: 1.09x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.54 ms: 1.09x slower                                                 |
| comprehensions             | 16.5 us                                                      | 18.0 us: 1.09x slower                                                 |
| float                      | 77.5 ms                                                      | 85.1 ms: 1.10x slower                                                 |
| async_generators           | 377 ms                                                       | 415 ms: 1.10x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.21 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.67 sec: 1.11x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.94 sec: 1.12x slower                                                |
| json_loads                 | 27.0 us                                                      | 30.4 us: 1.13x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.98 us: 1.13x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 238 us: 1.14x slower                                                  |
| 2to3                       | 260 ms                                                       | 296 ms: 1.14x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 89.5 ms: 1.14x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 339 us: 1.15x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.15x slower                                                  |
| raytrace                   | 253 ms                                                       | 292 ms: 1.16x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 99.0 ms: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| sympy_str                  | 275 ms                                                       | 319 ms: 1.16x slower                                                  |
| sympy_expand               | 457 ms                                                       | 534 ms: 1.17x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.00 us: 1.17x slower                                                 |
| richards                   | 45.2 ms                                                      | 53.0 ms: 1.17x slower                                                 |
| richards_super             | 51.6 ms                                                      | 60.6 ms: 1.17x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.1 ms: 1.18x slower                                                 |
| generators                 | 28.8 ms                                                      | 34.1 ms: 1.18x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.70 ms: 1.19x slower                                                 |
| thrift                     | 778 us                                                       | 930 us: 1.20x slower                                                  |
| django_template            | 34.1 ms                                                      | 41.0 ms: 1.20x slower                                                 |
| meteor_contest             | 102 ms                                                       | 125 ms: 1.23x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 74.9 ms: 1.26x slower                                                 |
| fannkuch                   | 370 ms                                                       | 467 ms: 1.26x slower                                                  |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 88.2 ms: 1.30x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.73 ms: 1.32x slower                                                 |
| mako                       | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| coverage                   | 83.0 ms                                                      | 118 ms: 1.42x slower                                                  |
| nbody                      | 85.1 ms                                                      | 122 ms: 1.44x slower                                                  |
| python_startup             | 11.0 ms                                                      | 16.4 ms: 1.49x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.62x slower                                                 |
| telco                      | 7.82 ms                                                      | 175 ms: 22.33x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_memoization_tg, xml_etree_iterparse, async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 98.79% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x