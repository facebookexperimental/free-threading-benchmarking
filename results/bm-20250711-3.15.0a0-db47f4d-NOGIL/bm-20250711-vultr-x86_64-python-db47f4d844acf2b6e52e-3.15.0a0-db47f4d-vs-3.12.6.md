# Results vs. 3.12.6

- fork: python
- ref: db47f4d844acf2b6e52e
- machine: linux-x86_64
- commit hash: db47f4d
- commit date: 2025-07-11
- overall geometric mean: 1.022x slower
- HPT reliability: 93.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 66.3 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 521 ms: 2.13x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.97x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                 |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| nbody          | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 231 us: 1.05x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 340 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.1 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.6 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.4 ms: 1.14x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 57.1 ms: 1.14x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.0 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 521 ms: 2.13x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.97x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.84x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.89 ms: 1.83x faster                                                 |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                  |
| deepcopy                   | 352 us                                                 | 290 us: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 69.2 ms: 1.17x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.7 us: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.4 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.08x faster                                                 |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                  |
| generators                 | 32.2 ms                                                | 30.3 ms: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.04 us: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.1 ms: 1.00x slower                                                 |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 767 ms: 1.03x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.58 ms: 1.04x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.3 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| pyflate                    | 448 ms                                                 | 468 ms: 1.04x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 231 us: 1.05x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.45 ms: 1.05x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.96 us: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                 |
| scimark_fft                | 342 ms                                                 | 363 ms: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                  |
| 2to3                       | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.7 ms: 1.10x slower                                                 |
| logging_format             | 7.35 us                                                | 8.10 us: 1.10x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 340 us: 1.10x slower                                                  |
| thrift                     | 791 us                                                 | 883 us: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| richards                   | 45.9 ms                                                | 51.5 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.8 ms: 1.13x slower                                                 |
| richards_super             | 51.9 ms                                                | 58.9 ms: 1.14x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 77.7 ms: 1.14x slower                                                 |
| django_template            | 34.7 ms                                                | 39.4 ms: 1.14x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.1 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.1 ms: 1.17x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.0 ms: 1.18x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.6 us: 1.19x slower                                                 |
| fannkuch                   | 372 ms                                                 | 458 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.44 ms: 1.24x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.35x slower                                                 |
| nbody                      | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.02x slower                                                 |
| telco                      | 6.53 ms                                                | 175 ms: 26.85x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.022x slower

# HPT report

- Reliability score: 93.70% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x