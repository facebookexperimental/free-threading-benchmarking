# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.047x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 300 ms: 1.14x slower                                                   |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 69.9 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 547 ms: 2.03x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.88x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.88x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.33x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 538 ms: 1.04x slower                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.79 sec: 1.19x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.3 ms: 1.04x faster                                                  |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| nbody          | 89.3 ms                                                | 138 ms: 1.55x slower                                                   |
| Geometric mean | (ref)                                                  | 1.17x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                  |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                  |
| regex_compile  | 142 ms                                                 | 157 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| unpickle             | 14.1 us                                                | 14.3 us: 1.02x slower                                                  |
| pickle_dict          | 31.8 us                                                | 32.8 us: 1.03x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.14 us: 1.08x slower                                                  |
| pickle               | 10.9 us                                                | 12.1 us: 1.11x slower                                                  |
| json_loads           | 26.5 us                                                | 29.5 us: 1.11x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.39 sec: 1.13x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.36 us: 1.15x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 359 us: 1.17x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 257 us: 1.17x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 70.6 ms: 1.20x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.8 ms: 1.21x slower                                                  |
| django_template | 34.7 ms                                                | 43.4 ms: 1.25x slower                                                  |
| genshi_text     | 22.8 ms                                                | 28.6 ms: 1.26x slower                                                  |
| mako            | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 547 ms: 2.03x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.81 ms: 1.91x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.88x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.88x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.33x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                  |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 73.9 ms: 1.07x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.2 ms: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 77.3 ms: 1.04x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 39.2 us: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| generators                 | 32.2 ms                                                | 32.0 ms: 1.01x faster                                                  |
| unpickle                   | 14.1 us                                                | 14.3 us: 1.02x slower                                                  |
| json                       | 5.02 ms                                                | 5.13 ms: 1.02x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.02x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.15 us: 1.02x slower                                                  |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.89 sec: 1.03x slower                                                 |
| pickle_dict                | 31.8 us                                                | 32.8 us: 1.03x slower                                                  |
| asyncio_tcp                | 519 ms                                                 | 538 ms: 1.04x slower                                                   |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                                   |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.8 us: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                 |
| spectral_norm              | 110 ms                                                 | 117 ms: 1.06x slower                                                   |
| unpack_sequence            | 52.1 ns                                                | 55.2 ns: 1.06x slower                                                  |
| scimark_sor                | 130 ms                                                 | 138 ms: 1.06x slower                                                   |
| pickle_list                | 4.77 us                                                | 5.14 us: 1.08x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.62 sec: 1.08x slower                                                 |
| raytrace                   | 299 ms                                                 | 325 ms: 1.08x slower                                                   |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| html5lib                   | 63.6 ms                                                | 69.9 ms: 1.10x slower                                                  |
| chaos                      | 62.8 ms                                                | 69.2 ms: 1.10x slower                                                  |
| regex_compile              | 142 ms                                                 | 157 ms: 1.11x slower                                                   |
| thrift                     | 791 us                                                 | 875 us: 1.11x slower                                                   |
| pickle                     | 10.9 us                                                | 12.1 us: 1.11x slower                                                  |
| json_loads                 | 26.5 us                                                | 29.5 us: 1.11x slower                                                  |
| pyflate                    | 448 ms                                                 | 499 ms: 1.11x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 159 ms: 1.11x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.38 us: 1.11x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.88 ms: 1.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 839 ms: 1.13x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.39 sec: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                                 |
| 2to3                       | 264 ms                                                 | 300 ms: 1.14x slower                                                   |
| logging_format             | 7.35 us                                                | 8.41 us: 1.14x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.36 us: 1.15x slower                                                  |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 23.7 ms: 1.15x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 88.8 ms: 1.16x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 359 us: 1.17x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 257 us: 1.17x slower                                                   |
| sympy_expand               | 468 ms                                                 | 554 ms: 1.18x slower                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.79 sec: 1.19x slower                                                 |
| scimark_fft                | 342 ms                                                 | 407 ms: 1.19x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 70.6 ms: 1.20x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 60.8 ms: 1.21x slower                                                  |
| richards                   | 45.9 ms                                                | 55.7 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 84.3 ms: 1.23x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.65 ms: 1.24x slower                                                  |
| nqueens                    | 80.1 ms                                                | 99.5 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                                  |
| django_template            | 34.7 ms                                                | 43.4 ms: 1.25x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.6 ms: 1.26x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.26x slower                                                   |
| richards_super             | 51.9 ms                                                | 65.2 ms: 1.26x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.75 ms: 1.31x slower                                                  |
| fannkuch                   | 372 ms                                                 | 501 ms: 1.35x slower                                                   |
| telco                      | 6.53 ms                                                | 8.93 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                  |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                                   |
| nbody                      | 89.3 ms                                                | 138 ms: 1.55x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.17 ms: 3.37x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 97.9 ms: 9.06x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, async_generators
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.047x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.38x