# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.011x faster
- HPT reliability: 91.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 318 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 533 ms: 1.03x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.79 sec: 1.19x slower                                                |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 214 ms: 1.16x slower                                                  |
| nbody          | 89.3 ms                                                | 123 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.2 ms: 1.02x faster                                                 |
| regex_dna      | 168 ms                                                 | 170 ms: 1.01x slower                                                  |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.01x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                |
| pickle_list          | 4.77 us                                                | 4.99 us: 1.05x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 232 us: 1.05x slower                                                  |
| unpickle             | 14.1 us                                                | 15.0 us: 1.07x slower                                                 |
| pickle               | 10.9 us                                                | 12.1 us: 1.11x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.42 us: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.3 ms: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.56 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.5 ms: 1.14x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 57.7 ms: 1.15x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.84x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.89 ms: 1.83x faster                                                 |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 318 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                 |
| deepcopy                   | 352 us                                                 | 291 us: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.8 us: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.5 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| generators                 | 32.2 ms                                                | 30.2 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 124 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 305 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.98 us: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| regex_v8                   | 20.6 ms                                                | 20.2 ms: 1.02x faster                                                 |
| pickle_dict                | 31.8 us                                                | 31.6 us: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                  |
| chaos                      | 62.8 ms                                                | 63.2 ms: 1.01x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| regex_dna                  | 168 ms                                                 | 170 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 303 ms: 1.01x slower                                                  |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| asyncio_tcp                | 519 ms                                                 | 533 ms: 1.03x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                 |
| pyflate                    | 448 ms                                                 | 466 ms: 1.04x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.44 ms: 1.04x slower                                                 |
| pickle_list                | 4.77 us                                                | 4.99 us: 1.05x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 232 us: 1.05x slower                                                  |
| json                       | 5.02 ms                                                | 5.31 ms: 1.06x slower                                                 |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.68 ms: 1.07x slower                                                 |
| unpickle                   | 14.1 us                                                | 15.0 us: 1.07x slower                                                 |
| scimark_fft                | 342 ms                                                 | 365 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.08x slower                                                 |
| nqueens                    | 80.1 ms                                                | 86.3 ms: 1.08x slower                                                 |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 56.4 ns: 1.08x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                  |
| thrift                     | 791 us                                                 | 860 us: 1.09x slower                                                  |
| pickle                     | 10.9 us                                                | 12.1 us: 1.11x slower                                                 |
| richards                   | 45.9 ms                                                | 51.4 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 77.0 ms: 1.13x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 528 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.5 ms: 1.13x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.0 ms: 1.14x slower                                                 |
| django_template            | 34.7 ms                                                | 39.5 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.63 us: 1.15x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.7 ms: 1.15x slower                                                 |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.15x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| pidigits                   | 184 ms                                                 | 214 ms: 1.16x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.42 us: 1.16x slower                                                 |
| logging_format             | 7.35 us                                                | 8.55 us: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.3 ms: 1.17x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.79 sec: 1.19x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 884 ms: 1.19x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.82 sec: 1.20x slower                                                |
| fannkuch                   | 372 ms                                                 | 458 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.49 ms: 1.25x slower                                                 |
| telco                      | 6.53 ms                                                | 8.59 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.45 ms: 1.33x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.56 ms: 1.33x slower                                                 |
| nbody                      | 89.3 ms                                                | 123 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.11 ms: 3.31x slower                                                 |
| logging_silent             | 109 ns                                                 | 529 ns: 4.85x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.50x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8-NOGIL/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 91.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x