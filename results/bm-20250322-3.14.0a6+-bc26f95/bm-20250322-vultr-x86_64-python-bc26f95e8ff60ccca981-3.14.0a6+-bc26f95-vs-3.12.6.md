# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.067x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 641 ms: 1.73x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 632 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 279 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 524 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 499 ms: 1.04x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                  |
| nbody          | 89.3 ms                                                | 98.6 ms: 1.10x slower                                                  |
| pidigits       | 184 ms                                                 | 210 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                  |
| regex_compile  | 142 ms                                                 | 128 ms: 1.11x faster                                                   |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads         | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                 |
| unpickle            | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| xml_etree_parse     | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| pickle_dict         | 31.8 us                                                | 30.3 us: 1.05x faster                                                  |
| xml_etree_iterparse | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                  |
| xml_etree_process   | 59.0 ms                                                | 60.3 ms: 1.02x slower                                                  |
| pickle_list         | 4.77 us                                                | 4.92 us: 1.03x slower                                                  |
| unpickle_list       | 4.67 us                                                | 4.82 us: 1.03x slower                                                  |
| pickle_pure_python  | 308 us                                                 | 322 us: 1.05x slower                                                   |
| json_loads          | 26.5 us                                                | 27.9 us: 1.05x slower                                                  |
| json_dumps          | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| pickle              | 10.9 us                                                | 12.3 us: 1.13x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.61 ms: 1.20x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.9 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 641 ms: 1.73x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 632 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_none            | 464 ms                                                 | 279 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 524 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                   |
| deepcopy                   | 352 us                                                 | 264 us: 1.33x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.3 us: 1.33x faster                                                  |
| go                         | 139 ms                                                 | 113 ms: 1.23x faster                                                   |
| spectral_norm              | 110 ms                                                 | 92.8 ms: 1.19x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.8 us: 1.18x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.9 ms: 1.18x faster                                                  |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| scimark_sor                | 130 ms                                                 | 115 ms: 1.13x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.74 us: 1.12x faster                                                  |
| pylint                     | 319 ms                                                 | 284 ms: 1.12x faster                                                   |
| raytrace                   | 299 ms                                                 | 267 ms: 1.12x faster                                                   |
| float                      | 80.8 ms                                                | 72.2 ms: 1.12x faster                                                  |
| logging_silent             | 109 ns                                                 | 97.7 ns: 1.12x faster                                                  |
| regex_compile              | 142 ms                                                 | 128 ms: 1.11x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 130 ms: 1.10x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.9 ms: 1.10x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.15 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                 |
| chaos                      | 62.8 ms                                                | 57.8 ms: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.77 us: 1.09x faster                                                  |
| generators                 | 32.2 ms                                                | 29.7 ms: 1.09x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.12 us: 1.08x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 70.9 ms: 1.08x faster                                                  |
| pyflate                    | 448 ms                                                 | 418 ms: 1.07x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                 |
| unpickle                   | 14.1 us                                                | 13.3 us: 1.06x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                   |
| richards                   | 45.9 ms                                                | 43.6 ms: 1.05x faster                                                  |
| pickle_dict                | 31.8 us                                                | 30.3 us: 1.05x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.7 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 499 ms: 1.04x faster                                                   |
| richards_super             | 51.9 ms                                                | 50.0 ms: 1.04x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.33 sec: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 66.4 ms: 1.03x faster                                                  |
| scimark_fft                | 342 ms                                                 | 332 ms: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.88 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 257 ms: 1.03x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.02x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 733 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                  |
| hexiom                     | 6.17 ms                                                | 6.09 ms: 1.01x faster                                                  |
| meteor_contest             | 104 ms                                                 | 103 ms: 1.01x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.51 sec: 1.00x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 52.7 ns: 1.01x slower                                                  |
| nqueens                    | 80.1 ms                                                | 81.8 ms: 1.02x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 60.3 ms: 1.02x slower                                                  |
| pickle_list                | 4.77 us                                                | 4.92 us: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.53 ms: 1.03x slower                                                  |
| unpickle_list              | 4.67 us                                                | 4.82 us: 1.03x slower                                                  |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 322 us: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                  |
| fannkuch                   | 372 ms                                                 | 401 ms: 1.08x slower                                                   |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| nbody                      | 89.3 ms                                                | 98.6 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                  |
| pickle                     | 10.9 us                                                | 12.3 us: 1.13x slower                                                  |
| pidigits                   | 184 ms                                                 | 210 ms: 1.14x slower                                                   |
| telco                      | 6.53 ms                                                | 7.50 ms: 1.15x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.61 ms: 1.20x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.24 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.9 ms: 1.51x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 89.5 ms: 8.29x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (7): thrift, sympy_expand, sqlite_synth, scimark_lu, xml_etree_generate, asyncio_websockets, unpickle_pure_python
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.067x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x