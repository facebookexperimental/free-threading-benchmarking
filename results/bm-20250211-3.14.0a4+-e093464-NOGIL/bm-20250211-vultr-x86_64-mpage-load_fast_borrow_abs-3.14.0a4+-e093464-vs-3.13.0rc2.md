# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: e093464
- commit date: 2025-02-11
- overall geometric mean: 1.069x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 302 ms: 1.16x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.81 sec: 1.07x slower                                                |
| html5lib       | 67.0 ms                                                      | 71.8 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 572 ms: 1.60x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 510 ms: 1.25x faster                                                  |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 542 ms: 1.23x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                          |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 71.7 ms: 1.08x faster                                                 |
| nbody          | 85.1 ms                                                      | 123 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                 |
| regex_dna      | 180 ms                                                       | 171 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.02x slower                                                 |
| regex_compile  | 132 ms                                                       | 151 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.5 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 243 us: 1.16x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.5 us: 1.17x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 364 us: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.63 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.1 ms: 1.21x slower                                                 |
| django_template | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.6 ms: 1.28x slower                                                 |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.65 ms: 1.90x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 572 ms: 1.60x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 510 ms: 1.25x faster                                                  |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 542 ms: 1.23x faster                                                  |
| deepcopy                   | 355 us                                                       | 304 us: 1.17x faster                                                  |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.01 us: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 71.7 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.5 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 36.9 us: 1.06x faster                                                 |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.06x faster                                                  |
| go                         | 141 ms                                                       | 136 ms: 1.03x faster                                                  |
| scimark_sor                | 134 ms                                                       | 130 ms: 1.03x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                                 |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.18 us: 1.02x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.02x slower                                                 |
| scimark_fft                | 349 ms                                                       | 359 ms: 1.03x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.68 sec: 1.05x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                                |
| logging_silent             | 103 ns                                                       | 110 ns: 1.07x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 71.8 ms: 1.07x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.38 ms: 1.07x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.81 sec: 1.07x slower                                                |
| pyflate                    | 449 ms                                                       | 483 ms: 1.08x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.14 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 806 ms: 1.09x slower                                                  |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 82.5 ms: 1.10x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.67 sec: 1.11x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 119 ms: 1.13x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                 |
| regex_compile              | 132 ms                                                       | 151 ms: 1.14x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.71 sec: 1.15x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 60.7 ms: 1.15x slower                                                 |
| thrift                     | 778 us                                                       | 900 us: 1.16x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 243 us: 1.16x slower                                                  |
| 2to3                       | 260 ms                                                       | 302 ms: 1.16x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.5 us: 1.17x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 69.5 ms: 1.17x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.29 us: 1.18x slower                                                 |
| coverage                   | 83.0 ms                                                      | 98.9 ms: 1.19x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.86 ms: 1.19x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 134 ms: 1.19x slower                                                  |
| sympy_expand               | 457 ms                                                       | 546 ms: 1.19x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                  |
| chaos                      | 57.3 ms                                                      | 68.8 ms: 1.20x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.21 us: 1.20x slower                                                 |
| comprehensions             | 16.5 us                                                      | 19.8 us: 1.20x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.7 ms: 1.20x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 23.9 ms: 1.21x slower                                                 |
| generators                 | 28.8 ms                                                      | 34.8 ms: 1.21x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 59.1 ms: 1.21x slower                                                 |
| sympy_str                  | 275 ms                                                       | 334 ms: 1.22x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                                 |
| richards                   | 45.2 ms                                                      | 55.4 ms: 1.22x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 96.3 ms: 1.23x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 364 us: 1.23x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.54 ms: 1.23x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.40 ms: 1.24x slower                                                 |
| meteor_contest             | 102 ms                                                       | 126 ms: 1.24x slower                                                  |
| django_template            | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                 |
| raytrace                   | 253 ms                                                       | 314 ms: 1.24x slower                                                  |
| richards_super             | 51.6 ms                                                      | 64.4 ms: 1.25x slower                                                 |
| fannkuch                   | 370 ms                                                       | 468 ms: 1.27x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 27.6 ms: 1.28x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.8 ms: 1.29x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.63 ms: 1.30x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                 |
| nbody                      | 85.1 ms                                                      | 123 ms: 1.45x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.60 ms: 1.47x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.29 ms: 3.58x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 93.1 ms: 8.47x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                          |

Benchmark hidden because not significant (2): async_generators, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250211-3.14.0a4+-e093464-NOGIL/bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.33x