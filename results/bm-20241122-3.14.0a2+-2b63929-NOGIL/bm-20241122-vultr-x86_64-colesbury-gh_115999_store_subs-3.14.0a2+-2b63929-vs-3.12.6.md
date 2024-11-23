# Results vs. 3.12.6

- fork: colesbury
- ref: gh_115999_store_subs
- machine: linux-x86_64
- commit hash: 2b63929
- commit date: 2024-11-22
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 379 ms: 1.44x slower                                                      |
| docutils       | 2.64 sec                                               | 3.21 sec: 1.21x slower                                                    |
| html5lib       | 63.6 ms                                                | 99.7 ms: 1.57x slower                                                     |
| Geometric mean | (ref)                                                  | 1.40x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 874 ms: 1.27x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 898 ms: 1.21x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 467 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 373 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 633 ms: 1.14x faster                                                      |
| async_tree_none            | 464 ms                                                 | 407 ms: 1.14x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 496 ms: 1.12x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 660 ms: 1.08x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| coroutines                 | 23.9 ms                                                | 27.6 ms: 1.15x slower                                                     |
| async_generators           | 384 ms                                                 | 471 ms: 1.23x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 144 ms: 1.61x slower                                                      |
| float          | 80.8 ms                                                | 142 ms: 1.76x slower                                                      |
| Geometric mean | (ref)                                                  | 1.42x slower                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                     |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                      |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                     |
| regex_compile  | 142 ms                                                 | 194 ms: 1.36x slower                                                      |
| Geometric mean | (ref)                                                  | 1.12x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                     |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 103 ms: 1.21x slower                                                      |
| tomli_loads          | 2.11 sec                                               | 2.90 sec: 1.37x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 82.6 ms: 1.40x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 370 us: 1.68x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 561 us: 1.82x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.29x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                     |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.77x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 67.6 ms: 1.35x slower                                                     |
| genshi_text     | 22.8 ms                                                | 33.9 ms: 1.48x slower                                                     |
| django_template | 34.7 ms                                                | 55.6 ms: 1.60x slower                                                     |
| mako            | 11.0 ms                                                | 19.8 ms: 1.80x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.55x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 874 ms: 1.27x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 898 ms: 1.21x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 467 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 373 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 633 ms: 1.14x faster                                                      |
| async_tree_none            | 464 ms                                                 | 407 ms: 1.14x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 496 ms: 1.12x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 660 ms: 1.08x faster                                                      |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                      |
| pathlib                    | 21.5 ms                                                | 20.7 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 95.9 ms: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                      |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                                     |
| sqlite_synth               | 2.20 us                                                | 2.29 us: 1.04x slower                                                     |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                     |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                      |
| deepcopy_memo              | 40.3 us                                                | 44.1 us: 1.09x slower                                                     |
| coroutines                 | 23.9 ms                                                | 27.6 ms: 1.15x slower                                                     |
| scimark_fft                | 342 ms                                                 | 394 ms: 1.15x slower                                                      |
| spectral_norm              | 110 ms                                                 | 129 ms: 1.17x slower                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 5.59 sec: 1.18x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.68 us: 1.20x slower                                                     |
| generators                 | 32.2 ms                                                | 38.6 ms: 1.20x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 103 ms: 1.21x slower                                                      |
| docutils                   | 2.64 sec                                               | 3.21 sec: 1.21x slower                                                    |
| async_generators           | 384 ms                                                 | 471 ms: 1.23x slower                                                      |
| pylint                     | 319 ms                                                 | 393 ms: 1.23x slower                                                      |
| mdp                        | 2.42 sec                                               | 3.03 sec: 1.25x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 99.3 ms: 1.26x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.61 ms: 1.28x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 211 us: 1.29x slower                                                      |
| meteor_contest             | 104 ms                                                 | 135 ms: 1.30x slower                                                      |
| nqueens                    | 80.1 ms                                                | 105 ms: 1.31x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 103 ms: 1.34x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 67.6 ms: 1.35x slower                                                     |
| regex_compile              | 142 ms                                                 | 194 ms: 1.36x slower                                                      |
| pycparser                  | 1.17 sec                                               | 1.60 sec: 1.37x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.90 sec: 1.37x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                     |
| telco                      | 6.53 ms                                                | 8.99 ms: 1.38x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 82.6 ms: 1.40x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 149 ms: 1.40x slower                                                      |
| sqlglot_optimize           | 53.3 ms                                                | 74.9 ms: 1.41x slower                                                     |
| coverage                   | 71.4 ms                                                | 102 ms: 1.43x slower                                                      |
| pprint_safe_repr           | 743 ms                                                 | 1.06 sec: 1.43x slower                                                    |
| fannkuch                   | 372 ms                                                 | 533 ms: 1.43x slower                                                      |
| 2to3                       | 264 ms                                                 | 379 ms: 1.44x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 2.20 sec: 1.45x slower                                                    |
| comprehensions             | 19.8 us                                                | 28.7 us: 1.45x slower                                                     |
| genshi_text                | 22.8 ms                                                | 33.9 ms: 1.48x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 30.8 ms: 1.50x slower                                                     |
| thrift                     | 791 us                                                 | 1.22 ms: 1.54x slower                                                     |
| html5lib                   | 63.6 ms                                                | 99.7 ms: 1.57x slower                                                     |
| django_template            | 34.7 ms                                                | 55.6 ms: 1.60x slower                                                     |
| nbody                      | 89.3 ms                                                | 144 ms: 1.61x slower                                                      |
| pyflate                    | 448 ms                                                 | 728 ms: 1.63x slower                                                      |
| logging_simple             | 6.63 us                                                | 11.0 us: 1.65x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 370 us: 1.68x slower                                                      |
| logging_format             | 7.35 us                                                | 12.4 us: 1.69x slower                                                     |
| sympy_str                  | 292 ms                                                 | 495 ms: 1.70x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.70x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 120 ms: 1.75x slower                                                      |
| float                      | 80.8 ms                                                | 142 ms: 1.76x slower                                                      |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.77x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 203 ms: 1.78x slower                                                      |
| richards                   | 45.9 ms                                                | 82.1 ms: 1.79x slower                                                     |
| logging_silent             | 109 ns                                                 | 196 ns: 1.80x slower                                                      |
| mako                       | 11.0 ms                                                | 19.8 ms: 1.80x slower                                                     |
| hexiom                     | 6.17 ms                                                | 11.2 ms: 1.81x slower                                                     |
| chaos                      | 62.8 ms                                                | 114 ms: 1.81x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 561 us: 1.82x slower                                                      |
| sqlglot_transpile          | 1.67 ms                                                | 3.06 ms: 1.83x slower                                                     |
| scimark_sor                | 130 ms                                                 | 243 ms: 1.87x slower                                                      |
| richards_super             | 51.9 ms                                                | 97.9 ms: 1.89x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.64 ms: 1.95x slower                                                     |
| go                         | 139 ms                                                 | 277 ms: 1.99x slower                                                      |
| raytrace                   | 299 ms                                                 | 599 ms: 2.00x slower                                                      |
| sympy_expand               | 468 ms                                                 | 992 ms: 2.12x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 357 ms: 2.15x slower                                                      |
| deltablue                  | 3.45 ms                                                | 8.53 ms: 2.48x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.42 ms: 3.63x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.18x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.40x slower                                                              |

Benchmark hidden because not significant (3): json, deepcopy, pidigits
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a2+-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.34x