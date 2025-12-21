# Results vs. 3.13.0rc2

- fork: python
- ref: e46f28c6afce9c85e4bc
- machine: linux-x86_64
- commit hash: e46f28c
- commit date: 2025-12-19
- overall geometric mean: 1.063x slower
- HPT reliability: 98.22%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 276 ms: 1.06x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.73 sec: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 607 ms: 1.50x faster                                                   |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 321 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                   |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 623 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 597 ms: 1.07x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.19x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.9 ms: 1.06x faster                                                  |
| pidigits       | 217 ms                                                       | 226 ms: 1.04x slower                                                   |
| nbody          | 85.1 ms                                                      | 120 ms: 1.42x slower                                                   |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.3 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                   |
| regex_compile  | 132 ms                                                       | 141 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.1 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| json_dumps           | 10.5 ms                                                      | 11.1 ms: 1.05x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 233 us: 1.11x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.24 sec: 1.12x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 331 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                  |
| json_loads           | 27.0 us                                                      | 32.2 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.64 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.0 ms: 1.17x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 57.4 ms: 1.18x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 26.7 ms: 1.24x slower                                                  |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.30 sec: 1.81x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.91 ms: 1.65x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.15 ms: 1.54x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 607 ms: 1.50x faster                                                   |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                   |
| deepcopy                   | 355 us                                                       | 271 us: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.9 us: 1.31x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 321 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                   |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                   |
| go                         | 141 ms                                                       | 120 ms: 1.18x faster                                                   |
| scimark_sor                | 134 ms                                                       | 119 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 69.5 ms: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 623 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 597 ms: 1.07x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 21.3 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.1 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.9 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.94 us: 1.06x faster                                                  |
| pylint                     | 317 ms                                                       | 299 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                   |
| scimark_fft                | 349 ms                                                       | 343 ms: 1.02x faster                                                   |
| logging_silent             | 103 ns                                                       | 102 ns: 1.01x faster                                                   |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x slower                                                   |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                   |
| pyflate                    | 449 ms                                                       | 459 ms: 1.02x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 763 ms: 1.03x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.73 sec: 1.04x slower                                                 |
| pidigits                   | 217 ms                                                       | 226 ms: 1.04x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.57 sec: 1.05x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.1 ms: 1.05x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.35 ms: 1.06x slower                                                  |
| 2to3                       | 260 ms                                                       | 276 ms: 1.06x slower                                                   |
| regex_compile              | 132 ms                                                       | 141 ms: 1.06x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.7 us: 1.08x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.6 ms: 1.09x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.70 us: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 62.5 ms: 1.09x slower                                                  |
| json                       | 4.93 ms                                                      | 5.47 ms: 1.11x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 233 us: 1.11x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.23 ms: 1.11x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.65 us: 1.12x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.24 sec: 1.12x slower                                                 |
| sympy_str                  | 275 ms                                                       | 308 ms: 1.12x slower                                                   |
| sympy_expand               | 457 ms                                                       | 513 ms: 1.12x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 331 us: 1.12x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.51 ms: 1.13x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 175 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                  |
| generators                 | 28.8 ms                                                      | 32.6 ms: 1.13x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.5 ms: 1.14x slower                                                  |
| thrift                     | 778 us                                                       | 889 us: 1.14x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 89.8 ms: 1.14x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.2 ms: 1.15x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 129 ms: 1.15x slower                                                   |
| raytrace                   | 253 ms                                                       | 292 ms: 1.16x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.0 ms: 1.17x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 57.4 ms: 1.18x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.2 ms: 1.18x slower                                                  |
| json_loads                 | 27.0 us                                                      | 32.2 us: 1.19x slower                                                  |
| meteor_contest             | 102 ms                                                       | 121 ms: 1.19x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.81 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 189 us: 1.22x slower                                                   |
| fannkuch                   | 370 ms                                                       | 455 ms: 1.23x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 26.7 ms: 1.24x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.5 ms: 1.27x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.64 ms: 1.30x slower                                                  |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                  |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.42x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.61x slower                                                  |
| telco                      | 7.82 ms                                                      | 173 ms: 22.12x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (2): html5lib, pycparser
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251219-3.15.0a3+-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.063x slower

# HPT report

- Reliability score: 98.22% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x