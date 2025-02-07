# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: b0fcd85
- commit date: 2025-02-06
- overall geometric mean: 1.069x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 303 ms: 1.17x slower                                              |
| docutils       | 2.62 sec                                                     | 2.81 sec: 1.07x slower                                            |
| html5lib       | 67.0 ms                                                      | 72.3 ms: 1.08x slower                                             |
| Geometric mean | (ref)                                                        | 1.11x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 556 ms: 1.64x faster                                              |
| async_tree_io              | 876 ms                                                       | 589 ms: 1.49x faster                                              |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.40x faster                                              |
| async_tree_memoization     | 461 ms                                                       | 344 ms: 1.34x faster                                              |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                              |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                              |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 531 ms: 1.26x faster                                              |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                             |
| async_generators           | 377 ms                                                       | 372 ms: 1.02x faster                                              |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 202 ms: 1.07x faster                                              |
| float          | 77.5 ms                                                      | 73.0 ms: 1.06x faster                                             |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                              |
| Geometric mean | (ref)                                                        | 1.11x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                             |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                              |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                             |
| regex_compile  | 132 ms                                                       | 152 ms: 1.15x slower                                              |
| Geometric mean | (ref)                                                        | 1.02x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                             |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                              |
| xml_etree_generate   | 85.4 ms                                                      | 95.2 ms: 1.11x slower                                             |
| unpickle_pure_python | 210 us                                                       | 240 us: 1.14x slower                                              |
| xml_etree_process    | 59.3 ms                                                      | 68.0 ms: 1.15x slower                                             |
| tomli_loads          | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                            |
| json_loads           | 27.0 us                                                      | 31.6 us: 1.17x slower                                             |
| pickle_pure_python   | 294 us                                                       | 354 us: 1.20x slower                                              |
| json_dumps           | 10.5 ms                                                      | 12.7 ms: 1.21x slower                                             |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.77 ms: 1.32x slower                                             |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                             |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.7 ms: 1.20x slower                                             |
| django_template | 34.1 ms                                                      | 41.4 ms: 1.21x slower                                             |
| genshi_text     | 21.5 ms                                                      | 27.6 ms: 1.28x slower                                             |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                        | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.67 ms: 1.88x faster                                             |
| async_tree_io_tg           | 913 ms                                                       | 556 ms: 1.64x faster                                              |
| async_tree_io              | 876 ms                                                       | 589 ms: 1.49x faster                                              |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.40x faster                                              |
| async_tree_memoization     | 461 ms                                                       | 344 ms: 1.34x faster                                              |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                              |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                              |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 531 ms: 1.26x faster                                              |
| deepcopy                   | 355 us                                                       | 304 us: 1.17x faster                                              |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                             |
| sqlite_synth               | 2.21 us                                                      | 2.01 us: 1.10x faster                                             |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                             |
| pidigits                   | 217 ms                                                       | 202 ms: 1.07x faster                                              |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                              |
| float                      | 77.5 ms                                                      | 73.0 ms: 1.06x faster                                             |
| deepcopy_memo              | 39.1 us                                                      | 37.1 us: 1.05x faster                                             |
| scimark_sor                | 134 ms                                                       | 129 ms: 1.04x faster                                              |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                             |
| go                         | 141 ms                                                       | 137 ms: 1.03x faster                                              |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                             |
| async_generators           | 377 ms                                                       | 372 ms: 1.02x faster                                              |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                              |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                              |
| regex_dna                  | 180 ms                                                       | 184 ms: 1.02x slower                                              |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                             |
| logging_silent             | 103 ns                                                       | 106 ns: 1.04x slower                                              |
| bpe_tokeniser              | 4.45 sec                                                     | 4.65 sec: 1.05x slower                                            |
| create_gc_cycles           | 1.34 ms                                                      | 1.40 ms: 1.05x slower                                             |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                            |
| docutils                   | 2.62 sec                                                     | 2.81 sec: 1.07x slower                                            |
| pprint_safe_repr           | 738 ms                                                       | 795 ms: 1.08x slower                                              |
| html5lib                   | 67.0 ms                                                      | 72.3 ms: 1.08x slower                                             |
| pyflate                    | 449 ms                                                       | 485 ms: 1.08x slower                                              |
| json                       | 4.93 ms                                                      | 5.41 ms: 1.10x slower                                             |
| scimark_fft                | 349 ms                                                       | 385 ms: 1.10x slower                                              |
| telco                      | 7.82 ms                                                      | 8.64 ms: 1.10x slower                                             |
| pprint_pformat             | 1.50 sec                                                     | 1.65 sec: 1.11x slower                                            |
| dulwich_log                | 74.8 ms                                                      | 82.7 ms: 1.11x slower                                             |
| sqlglot_normalize          | 106 ms                                                       | 117 ms: 1.11x slower                                              |
| generators                 | 28.8 ms                                                      | 32.1 ms: 1.11x slower                                             |
| xml_etree_generate         | 85.4 ms                                                      | 95.2 ms: 1.11x slower                                             |
| thrift                     | 778 us                                                       | 883 us: 1.13x slower                                              |
| mdp                        | 2.36 sec                                                     | 2.68 sec: 1.14x slower                                            |
| unpickle_pure_python       | 210 us                                                       | 240 us: 1.14x slower                                              |
| xml_etree_process          | 59.3 ms                                                      | 68.0 ms: 1.15x slower                                             |
| sqlglot_optimize           | 52.7 ms                                                      | 60.4 ms: 1.15x slower                                             |
| regex_compile              | 132 ms                                                       | 152 ms: 1.15x slower                                              |
| logging_simple             | 6.16 us                                                      | 7.14 us: 1.16x slower                                             |
| tomli_loads                | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                            |
| 2to3                       | 260 ms                                                       | 303 ms: 1.17x slower                                              |
| json_loads                 | 27.0 us                                                      | 31.6 us: 1.17x slower                                             |
| chaos                      | 57.3 ms                                                      | 67.1 ms: 1.17x slower                                             |
| coverage                   | 83.0 ms                                                      | 97.2 ms: 1.17x slower                                             |
| comprehensions             | 16.5 us                                                      | 19.5 us: 1.18x slower                                             |
| sqlglot_transpile          | 1.56 ms                                                      | 1.84 ms: 1.18x slower                                             |
| pickle_pure_python         | 294 us                                                       | 354 us: 1.20x slower                                              |
| logging_format             | 6.84 us                                                      | 8.22 us: 1.20x slower                                             |
| scimark_lu                 | 113 ms                                                       | 136 ms: 1.20x slower                                              |
| genshi_xml                 | 48.8 ms                                                      | 58.7 ms: 1.20x slower                                             |
| json_dumps                 | 10.5 ms                                                      | 12.7 ms: 1.21x slower                                             |
| sympy_sum                  | 156 ms                                                       | 188 ms: 1.21x slower                                              |
| django_template            | 34.1 ms                                                      | 41.4 ms: 1.21x slower                                             |
| sympy_expand               | 457 ms                                                       | 555 ms: 1.21x slower                                              |
| sympy_integrate            | 19.8 ms                                                      | 24.1 ms: 1.22x slower                                             |
| sqlglot_parse              | 1.25 ms                                                      | 1.52 ms: 1.22x slower                                             |
| nqueens                    | 78.6 ms                                                      | 96.2 ms: 1.22x slower                                             |
| raytrace                   | 253 ms                                                       | 310 ms: 1.23x slower                                              |
| hexiom                     | 5.99 ms                                                      | 7.36 ms: 1.23x slower                                             |
| richards                   | 45.2 ms                                                      | 55.6 ms: 1.23x slower                                             |
| sympy_str                  | 275 ms                                                       | 337 ms: 1.23x slower                                              |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.83 ms: 1.24x slower                                             |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.2 ms: 1.24x slower                                             |
| richards_super             | 51.6 ms                                                      | 65.0 ms: 1.26x slower                                             |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                              |
| genshi_text                | 21.5 ms                                                      | 27.6 ms: 1.28x slower                                             |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                              |
| crypto_pyaes               | 67.9 ms                                                      | 88.1 ms: 1.30x slower                                             |
| python_startup_no_site     | 7.39 ms                                                      | 9.77 ms: 1.32x slower                                             |
| fannkuch                   | 370 ms                                                       | 489 ms: 1.32x slower                                              |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                             |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                             |
| deltablue                  | 3.12 ms                                                      | 4.55 ms: 1.46x slower                                             |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                              |
| bench_thread_pool          | 919 us                                                       | 3.30 ms: 3.59x slower                                             |
| bench_mp_pool              | 11.0 ms                                                      | 95.9 ms: 8.72x slower                                             |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                      |

Benchmark hidden because not significant (2): deepcopy_reduce, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250206-3.14.0a4+-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x