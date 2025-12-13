# Results vs. 3.13.0rc2

- fork: nascheme
- ref: set_lockfree_contain
- machine: linux-x86_64
- commit hash: 235b6eb
- commit date: 2025-12-13
- overall geometric mean: 1.066x slower
- HPT reliability: 96.04%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 281 ms: 1.08x slower                                                     |
| docutils       | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 617 ms: 1.48x faster                                                     |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 263 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.28x faster                                                     |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 519 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 544 ms: 1.22x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                     |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 203 ms: 1.07x faster                                                     |
| float          | 77.5 ms                                                      | 73.4 ms: 1.06x faster                                                    |
| nbody          | 85.1 ms                                                      | 123 ms: 1.44x slower                                                     |
| Geometric mean | (ref)                                                        | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                    |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                                     |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.0 ms: 1.07x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                     |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 237 us: 1.13x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 335 us: 1.14x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 98.1 ms: 1.15x slower                                                    |
| json_loads           | 27.0 us                                                      | 31.5 us: 1.17x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 70.5 ms: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.70 ms: 1.31x slower                                                    |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.2 ms: 1.19x slower                                                    |
| django_template | 34.1 ms                                                      | 41.1 ms: 1.21x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                    |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.78x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 1.92 ms: 1.64x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 7.17 ms: 1.53x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 617 ms: 1.48x faster                                                     |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 263 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.28x faster                                                     |
| deepcopy                   | 355 us                                                       | 279 us: 1.27x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.9 us: 1.26x faster                                                    |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 519 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 544 ms: 1.22x faster                                                     |
| go                         | 141 ms                                                       | 122 ms: 1.16x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| scimark_sor                | 134 ms                                                       | 121 ms: 1.11x faster                                                     |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 69.9 ms: 1.07x faster                                                    |
| pidigits                   | 217 ms                                                       | 203 ms: 1.07x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.0 ms: 1.07x faster                                                    |
| float                      | 77.5 ms                                                      | 73.4 ms: 1.06x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.98 us: 1.05x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 133 ms: 1.03x faster                                                     |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                                     |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                     |
| scimark_fft                | 349 ms                                                       | 344 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                     |
| pyflate                    | 449 ms                                                       | 459 ms: 1.02x slower                                                     |
| logging_silent             | 103 ns                                                       | 105 ns: 1.03x slower                                                     |
| generators                 | 28.8 ms                                                      | 29.6 ms: 1.03x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 782 ms: 1.06x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.62 sec: 1.08x slower                                                   |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 6.48 ms: 1.08x slower                                                    |
| 2to3                       | 260 ms                                                       | 281 ms: 1.08x slower                                                     |
| json                       | 4.93 ms                                                      | 5.38 ms: 1.09x slower                                                    |
| chaos                      | 57.3 ms                                                      | 62.7 ms: 1.09x slower                                                    |
| comprehensions             | 16.5 us                                                      | 18.0 us: 1.10x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 21.7 ms: 1.10x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.48 ms: 1.11x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.88 us: 1.12x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 237 us: 1.13x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 89.1 ms: 1.13x slower                                                    |
| sympy_sum                  | 156 ms                                                       | 177 ms: 1.14x slower                                                     |
| sympy_str                  | 275 ms                                                       | 312 ms: 1.14x slower                                                     |
| richards                   | 45.2 ms                                                      | 51.5 ms: 1.14x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 335 us: 1.14x slower                                                     |
| logging_format             | 6.84 us                                                      | 7.85 us: 1.15x slower                                                    |
| richards_super             | 51.6 ms                                                      | 59.2 ms: 1.15x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 98.1 ms: 1.15x slower                                                    |
| sympy_expand               | 457 ms                                                       | 526 ms: 1.15x slower                                                     |
| thrift                     | 778 us                                                       | 907 us: 1.17x slower                                                     |
| json_loads                 | 27.0 us                                                      | 31.5 us: 1.17x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 132 ms: 1.17x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.67 ms: 1.18x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 70.5 ms: 1.19x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.61 ms: 1.19x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 58.2 ms: 1.19x slower                                                    |
| raytrace                   | 253 ms                                                       | 303 ms: 1.20x slower                                                     |
| django_template            | 34.1 ms                                                      | 41.1 ms: 1.21x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.3 ms: 1.21x slower                                                    |
| meteor_contest             | 102 ms                                                       | 125 ms: 1.23x slower                                                     |
| fannkuch                   | 370 ms                                                       | 455 ms: 1.23x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.25x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 85.4 ms: 1.26x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 9.70 ms: 1.31x slower                                                    |
| coverage                   | 83.0 ms                                                      | 112 ms: 1.35x slower                                                     |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                    |
| nbody                      | 85.1 ms                                                      | 123 ms: 1.44x slower                                                     |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                    |
| telco                      | 7.82 ms                                                      | 177 ms: 22.64x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                             |

Benchmark hidden because not significant (3): pylint, coroutines, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251213-3.15.0a2+-235b6eb-NOGIL/bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2+-235b6eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 96.04% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x