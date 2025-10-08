# Results vs. 3.13.0rc2

- fork: python
- ref: 85ec35d2ab8b764aefd6
- machine: linux-x86_64
- commit hash: 85ec35d
- commit date: 2025-10-08
- overall geometric mean: 1.050x slower
- HPT reliability: 93.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 279 ms: 1.08x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.67 sec: 1.02x slower                                                |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 518 ms: 1.76x faster                                                  |
| async_tree_io              | 876 ms                                                       | 544 ms: 1.61x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 225 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 283 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 468 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                  |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.2 ms: 1.12x faster                                                 |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                                  |
| nbody          | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                                 |
| regex_dna      | 180 ms                                                       | 170 ms: 1.06x faster                                                  |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.03 sec: 1.01x slower                                                |
| json_dumps           | 10.5 ms                                                      | 11.0 ms: 1.04x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 232 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 339 us: 1.15x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 69.3 ms: 1.17x slower                                                 |
| json_loads           | 27.0 us                                                      | 31.6 us: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 57.7 ms: 1.18x slower                                                 |
| django_template | 34.1 ms                                                      | 40.8 ms: 1.19x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                 |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.79x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 518 ms: 1.76x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.95 ms: 1.61x faster                                                 |
| async_tree_io              | 876 ms                                                       | 544 ms: 1.61x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 225 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 283 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 468 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                  |
| deepcopy                   | 355 us                                                       | 278 us: 1.28x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.1 us: 1.26x faster                                                 |
| go                         | 141 ms                                                       | 123 ms: 1.15x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                 |
| float                      | 77.5 ms                                                      | 69.2 ms: 1.12x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.8 ms: 1.09x faster                                                 |
| scimark_sor                | 134 ms                                                       | 124 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.93 us: 1.06x faster                                                 |
| regex_dna                  | 180 ms                                                       | 170 ms: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                 |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.8 ms: 1.04x faster                                                 |
| scimark_fft                | 349 ms                                                       | 341 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.03 sec: 1.01x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.67 sec: 1.02x slower                                                |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| pyflate                    | 449 ms                                                       | 463 ms: 1.03x slower                                                  |
| logging_silent             | 103 ns                                                       | 106 ns: 1.04x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.0 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 776 ms: 1.05x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.60 sec: 1.07x slower                                                |
| hexiom                     | 5.99 ms                                                      | 6.41 ms: 1.07x slower                                                 |
| 2to3                       | 260 ms                                                       | 279 ms: 1.08x slower                                                  |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| json                       | 4.93 ms                                                      | 5.40 ms: 1.10x slower                                                 |
| comprehensions             | 16.5 us                                                      | 18.1 us: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.9 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 232 us: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.25 ms: 1.11x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.87 us: 1.11x slower                                                 |
| chaos                      | 57.3 ms                                                      | 63.9 ms: 1.12x slower                                                 |
| thrift                     | 778 us                                                       | 872 us: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                 |
| sympy_str                  | 275 ms                                                       | 309 ms: 1.12x slower                                                  |
| sympy_expand               | 457 ms                                                       | 517 ms: 1.13x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.54 ms: 1.13x slower                                                 |
| generators                 | 28.8 ms                                                      | 32.7 ms: 1.14x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 89.4 ms: 1.14x slower                                                 |
| richards                   | 45.2 ms                                                      | 51.6 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.53 ms: 1.14x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 178 ms: 1.14x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.4 ms: 1.15x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 339 us: 1.15x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.87 us: 1.15x slower                                                 |
| meteor_contest             | 102 ms                                                       | 118 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 69.3 ms: 1.17x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.6 us: 1.17x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 132 ms: 1.18x slower                                                  |
| raytrace                   | 253 ms                                                       | 299 ms: 1.18x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 57.7 ms: 1.18x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.0 ms: 1.19x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.8 ms: 1.19x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 189 us: 1.22x slower                                                  |
| fannkuch                   | 370 ms                                                       | 453 ms: 1.23x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 84.9 ms: 1.25x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                 |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.33x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 15.2 ms: 1.39x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                 |
| nbody                      | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.06 ms: 3.33x slower                                                 |
| telco                      | 7.82 ms                                                      | 175 ms: 22.32x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                          |

Benchmark hidden because not significant (3): pylint, html5lib, spectral_norm
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.050x slower

# HPT report

- Reliability score: 93.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x