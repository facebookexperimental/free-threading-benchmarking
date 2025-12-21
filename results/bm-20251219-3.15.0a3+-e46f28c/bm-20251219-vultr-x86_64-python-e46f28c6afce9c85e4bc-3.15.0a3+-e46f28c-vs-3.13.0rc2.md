# Results vs. 3.13.0rc2

- fork: python
- ref: e46f28c6afce9c85e4bc
- machine: linux-x86_64
- commit hash: e46f28c
- commit date: 2025-12-19
- overall geometric mean: 1.033x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 245 ms: 1.06x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 554 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 584 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 243 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 533 ms: 1.20x faster                                                   |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.7 ms: 1.10x faster                                                  |
| pidigits       | 217 ms                                                       | 209 ms: 1.04x faster                                                   |
| nbody          | 85.1 ms                                                      | 88.0 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                  |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.00 ms: 1.05x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| json_loads           | 27.0 us                                                      | 27.3 us: 1.01x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 311 us: 1.06x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.04x faster                                                 |
| async_tree_io              | 876 ms                                                       | 554 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 584 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 307 ms: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.49x faster                                                  |
| async_tree_none            | 354 ms                                                       | 243 ms: 1.45x faster                                                   |
| deepcopy                   | 355 us                                                       | 248 us: 1.43x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 533 ms: 1.25x faster                                                   |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 533 ms: 1.20x faster                                                   |
| spectral_norm              | 111 ms                                                       | 93.5 ms: 1.19x faster                                                  |
| scimark_fft                | 349 ms                                                       | 304 ms: 1.15x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.73 us: 1.14x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 284 ms: 1.12x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                       | 404 ms: 1.11x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 68.2 ms: 1.10x faster                                                  |
| float                      | 77.5 ms                                                      | 70.7 ms: 1.10x faster                                                  |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.32 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.0 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.74 us: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.3 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 692 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                 |
| 2to3                       | 260 ms                                                       | 245 ms: 1.06x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.00 ms: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.70 ms: 1.05x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.07 sec: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.0 ms: 1.04x faster                                                  |
| pidigits                   | 217 ms                                                       | 209 ms: 1.04x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.63 us: 1.03x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.7 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.1 ms: 1.03x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                  |
| meteor_contest             | 102 ms                                                       | 99.7 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.28 ms: 1.02x faster                                                  |
| thrift                     | 778 us                                                       | 766 us: 1.02x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.7 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                   |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.00x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 155 ms: 1.00x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 79.2 ms: 1.01x slower                                                  |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                   |
| json_loads                 | 27.0 us                                                      | 27.3 us: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                   |
| logging_silent             | 103 ns                                                       | 104 ns: 1.01x slower                                                   |
| json                       | 4.93 ms                                                      | 4.99 ms: 1.01x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.0 ms: 1.02x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.28 us: 1.03x slower                                                  |
| nbody                      | 85.1 ms                                                      | 88.0 ms: 1.03x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                  |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| fannkuch                   | 370 ms                                                       | 385 ms: 1.04x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.28 ms: 1.05x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 311 us: 1.06x slower                                                   |
| sympy_expand               | 457 ms                                                       | 484 ms: 1.06x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.82 ms: 1.53x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.49x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 335 ms: 30.50x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_text
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251219-3.15.0a3+-e46f28c/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3+-e46f28c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x