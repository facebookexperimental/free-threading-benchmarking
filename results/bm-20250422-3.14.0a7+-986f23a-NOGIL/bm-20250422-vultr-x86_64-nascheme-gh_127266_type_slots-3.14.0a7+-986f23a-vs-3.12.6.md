# Results vs. 3.12.6

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 986f23a
- commit date: 2025-04-22
- overall geometric mean: 1.031x faster
- HPT reliability: 57.38%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                     |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                   |
| html5lib       | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.96x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.96x faster                                                     |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 468 ms: 1.54x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                     |
| async_generators           | 384 ms                                                 | 358 ms: 1.07x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.56x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.2 ms: 1.20x faster                                                    |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                     |
| nbody          | 89.3 ms                                                | 110 ms: 1.23x slower                                                     |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                    |
| regex_compile  | 142 ms                                                 | 143 ms: 1.01x slower                                                     |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                    |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.07 sec: 1.02x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 228 us: 1.03x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 326 us: 1.06x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 93.3 ms: 1.09x slower                                                    |
| json_loads           | 26.5 us                                                | 29.4 us: 1.11x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 66.6 ms: 1.13x slower                                                    |
| json_dumps           | 10.4 ms                                                | 12.6 ms: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                    |
| genshi_text     | 22.8 ms                                                | 25.8 ms: 1.13x slower                                                    |
| django_template | 34.7 ms                                                | 40.4 ms: 1.17x slower                                                    |
| mako            | 11.0 ms                                                | 15.2 ms: 1.38x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.96x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.96x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                   |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 468 ms: 1.54x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                     |
| deepcopy                   | 352 us                                                 | 290 us: 1.21x faster                                                     |
| float                      | 80.8 ms                                                | 67.2 ms: 1.20x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 34.8 us: 1.16x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                    |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 1.99 us: 1.11x faster                                                    |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.34 sec: 1.09x faster                                                   |
| spectral_norm              | 110 ms                                                 | 102 ms: 1.08x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                     |
| async_generators           | 384 ms                                                 | 358 ms: 1.07x faster                                                     |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                     |
| generators                 | 32.2 ms                                                | 30.1 ms: 1.07x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                    |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                     |
| raytrace                   | 299 ms                                                 | 288 ms: 1.04x faster                                                     |
| chaos                      | 62.8 ms                                                | 61.0 ms: 1.03x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                   |
| comprehensions             | 19.8 us                                                | 19.3 us: 1.03x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.02 us: 1.02x faster                                                    |
| scimark_fft                | 342 ms                                                 | 335 ms: 1.02x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 2.07 sec: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                     |
| regex_compile              | 142 ms                                                 | 143 ms: 1.01x slower                                                     |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                    |
| deltablue                  | 3.45 ms                                                | 3.52 ms: 1.02x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                   |
| pyflate                    | 448 ms                                                 | 459 ms: 1.02x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 764 ms: 1.03x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 228 us: 1.03x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.96 us: 1.05x slower                                                    |
| html5lib                   | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                    |
| logging_format             | 7.35 us                                                | 7.78 us: 1.06x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 326 us: 1.06x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.55 ms: 1.06x slower                                                    |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 81.8 ms: 1.07x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 153 ms: 1.07x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.07x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.4 ms: 1.07x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 73.4 ms: 1.07x slower                                                    |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                    |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                     |
| richards                   | 45.9 ms                                                | 49.7 ms: 1.08x slower                                                    |
| nqueens                    | 80.1 ms                                                | 87.2 ms: 1.09x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 93.3 ms: 1.09x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 55.4 ms: 1.10x slower                                                    |
| richards_super             | 51.9 ms                                                | 57.3 ms: 1.11x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.4 us: 1.11x slower                                                    |
| sympy_expand               | 468 ms                                                 | 525 ms: 1.12x slower                                                     |
| genshi_text                | 22.8 ms                                                | 25.8 ms: 1.13x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 66.6 ms: 1.13x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.13x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.01 ms: 1.14x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 188 us: 1.15x slower                                                     |
| django_template            | 34.7 ms                                                | 40.4 ms: 1.17x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 12.6 ms: 1.21x slower                                                    |
| fannkuch                   | 372 ms                                                 | 452 ms: 1.21x slower                                                     |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                                     |
| nbody                      | 89.3 ms                                                | 110 ms: 1.23x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.25x slower                                                    |
| telco                      | 6.53 ms                                                | 8.49 ms: 1.30x slower                                                    |
| mako                       | 11.0 ms                                                | 15.2 ms: 1.38x slower                                                    |
| coverage                   | 71.4 ms                                                | 110 ms: 1.53x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 96.0 ms: 8.89x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250422-3.14.0a7+-986f23a-NOGIL/bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 57.38% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x