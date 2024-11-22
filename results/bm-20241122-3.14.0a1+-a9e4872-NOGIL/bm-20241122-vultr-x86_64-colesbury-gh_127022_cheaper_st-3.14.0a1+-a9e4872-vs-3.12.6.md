# Results vs. 3.12.6

- fork: colesbury
- ref: gh_127022_cheaper_st
- machine: linux-x86_64
- commit hash: a9e4872
- commit date: 2024-11-22
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 411 ms: 1.56x slower                                                      |
| docutils       | 2.64 sec                                               | 3.32 sec: 1.26x slower                                                    |
| html5lib       | 63.6 ms                                                | 102 ms: 1.61x slower                                                      |
| Geometric mean | (ref)                                                  | 1.47x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 903 ms: 1.23x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 373 ms: 1.19x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 474 ms: 1.18x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 936 ms: 1.16x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 640 ms: 1.13x faster                                                      |
| async_tree_none            | 464 ms                                                 | 412 ms: 1.13x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 507 ms: 1.09x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 672 ms: 1.06x faster                                                      |
| async_generators           | 384 ms                                                 | 473 ms: 1.23x slower                                                      |
| coroutines                 | 23.9 ms                                                | 30.1 ms: 1.26x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                      |
| float          | 80.8 ms                                                | 146 ms: 1.80x slower                                                      |
| nbody          | 89.3 ms                                                | 189 ms: 2.12x slower                                                      |
| Geometric mean | (ref)                                                  | 1.56x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                     |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                      |
| regex_v8       | 20.6 ms                                                | 25.6 ms: 1.24x slower                                                     |
| regex_compile  | 142 ms                                                 | 222 ms: 1.56x slower                                                      |
| Geometric mean | (ref)                                                  | 1.16x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                      |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 108 ms: 1.12x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 111 ms: 1.30x slower                                                      |
| json_dumps           | 10.4 ms                                                | 15.2 ms: 1.47x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 3.14 sec: 1.49x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 90.6 ms: 1.54x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 413 us: 1.87x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 615 us: 2.00x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.39x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                     |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 78.8 ms: 1.57x slower                                                     |
| genshi_text     | 22.8 ms                                                | 39.0 ms: 1.71x slower                                                     |
| django_template | 34.7 ms                                                | 63.1 ms: 1.82x slower                                                     |
| mako            | 11.0 ms                                                | 20.9 ms: 1.90x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.75x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 903 ms: 1.23x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 373 ms: 1.19x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 474 ms: 1.18x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 936 ms: 1.16x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 640 ms: 1.13x faster                                                      |
| async_tree_none            | 464 ms                                                 | 412 ms: 1.13x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 507 ms: 1.09x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 672 ms: 1.06x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 3.31 ms: 1.05x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                      |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                      |
| pathlib                    | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                     |
| json                       | 5.02 ms                                                | 5.23 ms: 1.04x slower                                                     |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                     |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                      |
| sqlite_synth               | 2.20 us                                                | 2.43 us: 1.10x slower                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 108 ms: 1.12x slower                                                      |
| scimark_fft                | 342 ms                                                 | 394 ms: 1.15x slower                                                      |
| deepcopy                   | 352 us                                                 | 424 us: 1.21x slower                                                      |
| generators                 | 32.2 ms                                                | 39.2 ms: 1.22x slower                                                     |
| async_generators           | 384 ms                                                 | 473 ms: 1.23x slower                                                      |
| mdp                        | 2.42 sec                                               | 2.99 sec: 1.24x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 25.6 ms: 1.24x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.50 ms: 1.25x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.32 sec: 1.26x slower                                                    |
| coroutines                 | 23.9 ms                                                | 30.1 ms: 1.26x slower                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 6.01 sec: 1.27x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 111 ms: 1.30x slower                                                      |
| pylint                     | 319 ms                                                 | 415 ms: 1.30x slower                                                      |
| dulwich_log                | 78.9 ms                                                | 103 ms: 1.30x slower                                                      |
| deepcopy_memo              | 40.3 us                                                | 52.7 us: 1.31x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 105 ms: 1.37x slower                                                      |
| meteor_contest             | 104 ms                                                 | 142 ms: 1.38x slower                                                      |
| nqueens                    | 80.1 ms                                                | 113 ms: 1.41x slower                                                      |
| spectral_norm              | 110 ms                                                 | 157 ms: 1.42x slower                                                      |
| pycparser                  | 1.17 sec                                               | 1.67 sec: 1.43x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 4.44 us: 1.44x slower                                                     |
| coverage                   | 71.4 ms                                                | 103 ms: 1.45x slower                                                      |
| telco                      | 6.53 ms                                                | 9.51 ms: 1.46x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 15.2 ms: 1.47x slower                                                     |
| fannkuch                   | 372 ms                                                 | 554 ms: 1.49x slower                                                      |
| tomli_loads                | 2.11 sec                                               | 3.14 sec: 1.49x slower                                                    |
| comprehensions             | 19.8 us                                                | 29.8 us: 1.50x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 250 us: 1.53x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 90.6 ms: 1.54x slower                                                     |
| regex_compile              | 142 ms                                                 | 222 ms: 1.56x slower                                                      |
| 2to3                       | 264 ms                                                 | 411 ms: 1.56x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 78.8 ms: 1.57x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.73 ms: 1.59x slower                                                     |
| thrift                     | 791 us                                                 | 1.26 ms: 1.59x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 32.8 ms: 1.60x slower                                                     |
| html5lib                   | 63.6 ms                                                | 102 ms: 1.61x slower                                                      |
| sqlglot_optimize           | 53.3 ms                                                | 90.2 ms: 1.69x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 181 ms: 1.70x slower                                                      |
| genshi_text                | 22.8 ms                                                | 39.0 ms: 1.71x slower                                                     |
| pyflate                    | 448 ms                                                 | 767 ms: 1.71x slower                                                      |
| pprint_safe_repr           | 743 ms                                                 | 1.30 sec: 1.76x slower                                                    |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 2.72 sec: 1.79x slower                                                    |
| logging_format             | 7.35 us                                                | 13.2 us: 1.80x slower                                                     |
| logging_simple             | 6.63 us                                                | 11.9 us: 1.80x slower                                                     |
| float                      | 80.8 ms                                                | 146 ms: 1.80x slower                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 124 ms: 1.81x slower                                                      |
| django_template            | 34.7 ms                                                | 63.1 ms: 1.82x slower                                                     |
| sympy_str                  | 292 ms                                                 | 534 ms: 1.83x slower                                                      |
| unpickle_pure_python       | 221 us                                                 | 413 us: 1.87x slower                                                      |
| chaos                      | 62.8 ms                                                | 119 ms: 1.89x slower                                                      |
| mako                       | 11.0 ms                                                | 20.9 ms: 1.90x slower                                                     |
| richards                   | 45.9 ms                                                | 88.7 ms: 1.93x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 3.25 ms: 1.94x slower                                                     |
| logging_silent             | 109 ns                                                 | 212 ns: 1.95x slower                                                      |
| hexiom                     | 6.17 ms                                                | 12.3 ms: 1.99x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 615 us: 2.00x slower                                                      |
| scimark_sor                | 130 ms                                                 | 261 ms: 2.01x slower                                                      |
| richards_super             | 51.9 ms                                                | 106 ms: 2.05x slower                                                      |
| sqlglot_parse              | 1.36 ms                                                | 2.79 ms: 2.06x slower                                                     |
| raytrace                   | 299 ms                                                 | 626 ms: 2.09x slower                                                      |
| go                         | 139 ms                                                 | 292 ms: 2.10x slower                                                      |
| nbody                      | 89.3 ms                                                | 189 ms: 2.12x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 243 ms: 2.12x slower                                                      |
| sympy_expand               | 468 ms                                                 | 1.05 sec: 2.24x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 381 ms: 2.29x slower                                                      |
| deltablue                  | 3.45 ms                                                | 8.99 ms: 2.61x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.49 ms: 3.70x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.15x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.49x slower                                                              |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a1+-a9e4872-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.33x