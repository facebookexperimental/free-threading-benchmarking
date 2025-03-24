# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.143x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| docutils       | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 295 ms: 1.88x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 601 ms: 1.85x faster                                                   |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 449 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 468 ms: 1.53x faster                                                   |
| async_generators           | 384 ms                                                 | 315 ms: 1.22x faster                                                   |
| coroutines                 | 23.9 ms                                                | 20.6 ms: 1.16x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 492 ms: 1.05x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                  |
| nbody          | 89.3 ms                                                | 79.6 ms: 1.12x faster                                                  |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.10 ms: 1.02x faster                                                  |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                 |
| unpickle_list        | 4.67 us                                                | 4.24 us: 1.10x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 202 us: 1.09x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 54.7 ms: 1.08x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 80.0 ms: 1.06x faster                                                  |
| unpickle             | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 294 us: 1.05x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 93.9 ms: 1.03x faster                                                  |
| json_loads           | 26.5 us                                                | 26.1 us: 1.02x faster                                                  |
| pickle_dict          | 31.8 us                                                | 31.5 us: 1.01x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                   |
| pickle_list          | 4.77 us                                                | 4.97 us: 1.04x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| pickle               | 10.9 us                                                | 12.2 us: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.60 ms: 1.20x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.4 ms: 1.18x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 45.6 ms: 1.10x faster                                                  |
| django_template | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| mako            | 11.0 ms                                                | 11.3 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 295 ms: 1.88x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 601 ms: 1.85x faster                                                   |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 449 ms: 1.61x faster                                                   |
| deepcopy                   | 352 us                                                 | 229 us: 1.54x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 468 ms: 1.53x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 27.5 us: 1.47x faster                                                  |
| spectral_norm              | 110 ms                                                 | 78.3 ms: 1.41x faster                                                  |
| comprehensions             | 19.8 us                                                | 14.7 us: 1.35x faster                                                  |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.34 us: 1.32x faster                                                  |
| logging_silent             | 109 ns                                                 | 83.6 ns: 1.30x faster                                                  |
| scimark_sor                | 130 ms                                                 | 100 ms: 1.30x faster                                                   |
| raytrace                   | 299 ms                                                 | 237 ms: 1.26x faster                                                   |
| chaos                      | 62.8 ms                                                | 50.9 ms: 1.23x faster                                                  |
| async_generators           | 384 ms                                                 | 315 ms: 1.22x faster                                                   |
| scimark_fft                | 342 ms                                                 | 282 ms: 1.21x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 56.6 ms: 1.21x faster                                                  |
| generators                 | 32.2 ms                                                | 26.7 ms: 1.21x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 65.6 ms: 1.20x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.88 ms: 1.20x faster                                                  |
| richards                   | 45.9 ms                                                | 38.6 ms: 1.19x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.58 us: 1.19x faster                                                  |
| pylint                     | 319 ms                                                 | 270 ms: 1.18x faster                                                   |
| genshi_text                | 22.8 ms                                                | 19.4 ms: 1.18x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.17x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                 |
| float                      | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 18.7 ms: 1.16x faster                                                  |
| pyflate                    | 448 ms                                                 | 385 ms: 1.16x faster                                                   |
| logging_format             | 7.35 us                                                | 6.32 us: 1.16x faster                                                  |
| coroutines                 | 23.9 ms                                                | 20.6 ms: 1.16x faster                                                  |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| richards_super             | 51.9 ms                                                | 44.8 ms: 1.16x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.14 sec: 1.14x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 125 ms: 1.14x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 100 ms: 1.14x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 67.8 ms: 1.13x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 147 ms: 1.13x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.49 ms: 1.12x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 145 us: 1.12x faster                                                   |
| sympy_str                  | 292 ms                                                 | 260 ms: 1.12x faster                                                   |
| nbody                      | 89.3 ms                                                | 79.6 ms: 1.12x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.4 ms: 1.12x faster                                                  |
| nqueens                    | 80.1 ms                                                | 72.2 ms: 1.11x faster                                                  |
| unpickle_list              | 4.67 us                                                | 4.24 us: 1.10x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 45.6 ms: 1.10x faster                                                  |
| thrift                     | 791 us                                                 | 722 us: 1.10x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 202 us: 1.09x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.07 sec: 1.09x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.04 ms: 1.09x faster                                                  |
| 2to3                       | 264 ms                                                 | 244 ms: 1.08x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 54.7 ms: 1.08x faster                                                  |
| sympy_expand               | 468 ms                                                 | 437 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                 |
| django_template            | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 80.0 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 698 ms: 1.06x faster                                                   |
| unpickle                   | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 492 ms: 1.05x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                 |
| json                       | 5.02 ms                                                | 4.80 ms: 1.05x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 294 us: 1.05x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 93.9 ms: 1.03x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 50.7 ns: 1.03x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.10 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                  |
| json_loads                 | 26.5 us                                                | 26.1 us: 1.02x faster                                                  |
| pickle_dict                | 31.8 us                                                | 31.5 us: 1.01x faster                                                  |
| meteor_contest             | 104 ms                                                 | 103 ms: 1.00x faster                                                   |
| fannkuch                   | 372 ms                                                 | 381 ms: 1.02x slower                                                   |
| mako                       | 11.0 ms                                                | 11.3 ms: 1.03x slower                                                  |
| coverage                   | 71.4 ms                                                | 73.9 ms: 1.03x slower                                                  |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                   |
| pickle_list                | 4.77 us                                                | 4.97 us: 1.04x slower                                                  |
| telco                      | 6.53 ms                                                | 6.89 ms: 1.06x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 998 us: 1.06x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.67 sec: 1.10x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| pickle                     | 10.9 us                                                | 12.2 us: 1.12x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.60 ms: 1.20x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.19 ms: 1.21x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.78x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 87.4 ms: 8.10x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.143x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.16x