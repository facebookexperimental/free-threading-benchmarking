# Results vs. 3.13.0rc2

- fork: python
- ref: 6dad8b88cc39d8f9f41c
- machine: linux-x86_64
- commit hash: 6dad8b8
- commit date: 2026-09-18
- overall geometric mean: 1.028x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.41 sec: 1.08x faster                                                |
| html5lib       | 67.0 ms                                                      | 59.8 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 557 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 551 ms: 1.16x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 406 ms: 1.14x faster                                                  |
| async_tree_io              | 876 ms                                                       | 781 ms: 1.12x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 370 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 301 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                  |
| async_tree_none            | 354 ms                                                       | 332 ms: 1.07x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.10x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| float          | 77.5 ms                                                      | 72.6 ms: 1.07x faster                                                 |
| nbody          | 85.1 ms                                                      | 91.4 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                 |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                  |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| json_dumps           | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 89.2 ms: 1.04x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                  |
| xml_etree_parse      | 136 ms                                                       | 145 ms: 1.07x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 63.5 ms: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.72 ms: 1.04x slower                                                 |
| python_startup         | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| django_template | 34.1 ms                                                      | 37.0 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 112 ms: 2.83x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.12 sec: 2.10x faster                                                |
| deepcopy                   | 355 us                                                       | 228 us: 1.56x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 27.5 us: 1.42x faster                                                 |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 119 us: 1.30x faster                                                  |
| spectral_norm              | 111 ms                                                       | 86.3 ms: 1.29x faster                                                 |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.53 us: 1.23x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 557 ms: 1.20x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 551 ms: 1.16x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 406 ms: 1.14x faster                                                  |
| scimark_fft                | 349 ms                                                       | 309 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                       | 398 ms: 1.13x faster                                                  |
| async_tree_io              | 876 ms                                                       | 781 ms: 1.12x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| async_tree_memoization_tg  | 414 ms                                                       | 370 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.8 ms: 1.12x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 301 ms: 1.12x faster                                                  |
| pidigits                   | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 67.6 ms: 1.11x faster                                                 |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.41 sec: 1.08x faster                                                |
| nqueens                    | 78.6 ms                                                      | 72.9 ms: 1.08x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.41 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 72.6 ms: 1.07x faster                                                 |
| async_tree_none            | 354 ms                                                       | 332 ms: 1.07x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.64 ms: 1.06x faster                                                 |
| chaos                      | 57.3 ms                                                      | 54.1 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                |
| logging_silent             | 103 ns                                                       | 97.1 ns: 1.06x faster                                                 |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.9 us: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 721 ms: 1.02x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.9 ms: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.04 us: 1.02x faster                                                 |
| richards                   | 45.2 ms                                                      | 44.5 ms: 1.02x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 249 ms: 1.01x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.77 us: 1.01x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                |
| richards_super             | 51.6 ms                                                      | 51.1 ms: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                                  |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                 |
| thrift                     | 778 us                                                       | 789 us: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.02x slower                                                |
| coverage                   | 83.0 ms                                                      | 84.7 ms: 1.02x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 216 us: 1.03x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.6 ms: 1.03x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| sympy_expand               | 457 ms                                                       | 476 ms: 1.04x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.72 ms: 1.04x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 89.2 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 120 ms: 1.06x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 145 ms: 1.07x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 63.5 ms: 1.07x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.35 ms: 1.07x slower                                                 |
| nbody                      | 85.1 ms                                                      | 91.4 ms: 1.07x slower                                                 |
| django_template            | 34.1 ms                                                      | 37.0 ms: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.71 ms: 1.18x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.63 ms: 1.22x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.47x slower                                                 |
| telco                      | 7.82 ms                                                      | 160 ms: 20.51x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 288 ms: 26.18x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (3): sqlite_synth, json_loads, 2to3
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260918-3.16.0a0-6dad8b8/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x