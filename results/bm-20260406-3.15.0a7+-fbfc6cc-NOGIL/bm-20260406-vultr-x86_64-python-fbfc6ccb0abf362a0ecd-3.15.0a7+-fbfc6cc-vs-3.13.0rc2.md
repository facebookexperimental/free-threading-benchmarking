# Results vs. 3.13.0rc2

- fork: python
- ref: fbfc6ccb0abf362a0ecd
- machine: linux-x86_64
- commit hash: fbfc6cc
- commit date: 2026-04-06
- overall geometric mean: 1.059x slower
- HPT reliability: 90.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 283 ms: 1.09x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                 |
| html5lib       | 67.0 ms                                                      | 65.5 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 614 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 642 ms: 1.37x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 358 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.27x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 265 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 509 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                                   |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 514 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| float          | 77.5 ms                                                      | 74.5 ms: 1.04x faster                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 20.5 ms: 1.11x faster                                                  |
| regex_dna      | 180 ms                                                       | 169 ms: 1.07x faster                                                   |
| regex_compile  | 132 ms                                                       | 142 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 86.8 ms: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.96 sec: 1.03x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 11.0 ms: 1.05x slower                                                  |
| json_loads           | 27.0 us                                                      | 29.5 us: 1.09x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 236 us: 1.13x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 336 us: 1.14x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 69.1 ms: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.86 ms: 1.33x slower                                                  |
| python_startup         | 11.0 ms                                                      | 16.1 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 55.1 ms: 1.13x slower                                                  |
| django_template | 34.1 ms                                                      | 39.8 ms: 1.17x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 25.7 ms: 1.19x slower                                                  |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.93 ms: 1.63x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.03 ms: 1.56x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 614 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 642 ms: 1.37x faster                                                   |
| deepcopy                   | 355 us                                                       | 267 us: 1.33x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 358 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.27x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 265 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 509 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 31.6 us: 1.24x faster                                                  |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                   |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| go                         | 141 ms                                                       | 121 ms: 1.17x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 1.93 us: 1.15x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.5 ms: 1.11x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                  |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.8 ms: 1.09x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.90 us: 1.07x faster                                                  |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.07x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 71.1 ms: 1.05x faster                                                  |
| float                      | 77.5 ms                                                      | 74.5 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.96 sec: 1.03x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 65.5 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.39 sec: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 514 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                 |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.01x slower                                                   |
| json                       | 4.93 ms                                                      | 5.12 ms: 1.04x slower                                                  |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                   |
| pyflate                    | 449 ms                                                       | 469 ms: 1.04x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.0 ms: 1.05x slower                                                  |
| regex_compile              | 132 ms                                                       | 142 ms: 1.07x slower                                                   |
| chaos                      | 57.3 ms                                                      | 61.7 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 794 ms: 1.08x slower                                                   |
| 2to3                       | 260 ms                                                       | 283 ms: 1.09x slower                                                   |
| logging_simple             | 6.16 us                                                      | 6.72 us: 1.09x slower                                                  |
| json_loads                 | 27.0 us                                                      | 29.5 us: 1.09x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.9 ms: 1.10x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.65 sec: 1.10x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 87.3 ms: 1.11x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.66 ms: 1.11x slower                                                  |
| comprehensions             | 16.5 us                                                      | 18.4 us: 1.12x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.64 us: 1.12x slower                                                  |
| generators                 | 28.8 ms                                                      | 32.2 ms: 1.12x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.49 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.50 ms: 1.12x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 126 ms: 1.12x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 236 us: 1.13x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 55.1 ms: 1.13x slower                                                  |
| sympy_str                  | 275 ms                                                       | 311 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 336 us: 1.14x slower                                                   |
| sympy_expand               | 457 ms                                                       | 522 ms: 1.14x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 178 ms: 1.14x slower                                                   |
| richards_super             | 51.6 ms                                                      | 59.4 ms: 1.15x slower                                                  |
| richards                   | 45.2 ms                                                      | 52.1 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 69.1 ms: 1.16x slower                                                  |
| django_template            | 34.1 ms                                                      | 39.8 ms: 1.17x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.55 ms: 1.18x slower                                                  |
| thrift                     | 778 us                                                       | 924 us: 1.19x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 25.7 ms: 1.19x slower                                                  |
| raytrace                   | 253 ms                                                       | 302 ms: 1.20x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.4 ms: 1.20x slower                                                  |
| meteor_contest             | 102 ms                                                       | 123 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 191 us: 1.23x slower                                                   |
| fannkuch                   | 370 ms                                                       | 458 ms: 1.24x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 88.2 ms: 1.30x slower                                                  |
| coverage                   | 83.0 ms                                                      | 110 ms: 1.33x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.86 ms: 1.33x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                  |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| python_startup             | 11.0 ms                                                      | 16.1 ms: 1.47x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.46 ms: 1.59x slower                                                  |
| telco                      | 7.82 ms                                                      | 172 ms: 22.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (3): pylint, scimark_fft, pycparser
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260406-3.15.0a7+-fbfc6cc-NOGIL/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.059x slower

# HPT report

- Reliability score: 90.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x